# 1) Landing Page User Guide

undefinedThis document provides a summary of the functionality introduced with the WeServe landing page.


# Overview

WeServe consists of a landing page providing access to Division of Infrastructure Management web applications and is access from this URL: http://qw3giswwint1vm/weserve.

## Infrastructure applications

The following links are provided to internal staff through the WeServe landing page. Separate help documents are available for Warrior Watch, Residential Sweeping, and Pothole Repair.

* Warrior Watch
* Residential Sweeping
* Pothole Repair
* Roadside Mowing (Coming soon)
* Lucity
* ReCollect


undefined**Figure 1: **WeServe Landing page.

### Links to Outside Resources

* OHGO
* Buckeye Traffic
* [Accuweather.com](http://accuweather.com/) Columbus Forecast
* [Weather.com](http://weather.com/)

### Photo Gallery Carousel

* Scrolling images of DPS staff.
* Please submit a help ticket to DoT GIS staff to update the configuration file to add / remove images.

### Weathermap

* [Weather.gov](http://weather.gov/) national forecast map (updated automatically).

### Security

Please note each of the internal sites provided by WeServe have separate user permissions. Please work with DPS administration and DoT staff to confirm any access / permission issues to the sites.


# Configuration

*Please note DoT Staff will have permissions to modify the landing page configuration.* 


## Core Services Application Configuration

To add, remove, or configure core service applications please adjust the Title, Logo, URL, Browser Configuration, and Description.

Please note, logos are stored at the root of the landing page directory (C:\inetpub\wwwroot\weserve\LandingPage)

```
# These apps appear at the top of the landing page as large icons.
# Possible values:
#    Title
#    Logo        (name of image file in LandingPage directory)
#    Url
#    Browser        ("IE")
#    Disabled    (set to true to temporarily disable the app)
ExternalApps: [
    {
        Title: "Lucity"
        Logo: "LUCITY.png"
        Url: "http://qw3lucity1vm.columbus.local/LucityWeb"
        Browser: "IE"
        Description: "View/manage city assets and work orders."
    }
```

**Example:** Configuration settings for Lucity core services application.


## External Links

To add, remove, or configure links to external sites please provide the title and url.

```
# These links appear in the middle of the page as small buttons.
# Possible values:
#    Title
#    Url
ExternalLinks: [
    {
        Title: "OHGO"
        Url: "http://www.ohgo.com/dashboard/columbus"
```

**Example:** Configuration for OHGO external link.


## Image Carousel

To add, remove, or configure images included in the carousel edit the configuration settings. Please note the the site loads images in the order they are listed in the configuration file.

undefined
**Optional Information:**

* Title
* Description


**Required Information:**

* Image file name

```
# These items appear in the scrolling carousel at the bottom of the page.
# Possible values, all are optional:
#    Title        (large text)
#    Description (caption under title)
#    Image        (name of image file in LandingPage directory)
#    Url            (send the user somewhere when clicked)
#    Html        (raw HTML to display in the item, for instance a table)
Carousel: [
    {
        Title: "Welcome to <i>WeServe</i>!"
        Description: "This page will guide you to important division resources."
        Image: "aIMG_1513.jpg"
    }
```

**Example: **Configuration for first image.

