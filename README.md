# Update 01 - WeServe February 27, 2018

This document summarizes the steps used to resolve key comments provided by DPS on 2/6 and finalized on 2/12.

# Map Services

New map services are to be published. These changes will address several street sweep and pothole repair tools comments as well as map comments.


## Map Documents

All new map documents are stored here on the development server E:\SupportServices\MapDocuments\WeServe\ws

* ws_LabelsStreetMaint.mxd - This provides street maintenance zone labels to the street sweep map. Labels include a definition query supplied by DPS. 
* ws_LabelsStreetSweep.mxd - This provides street sweep zone labels to the street sweep map. Labels include a definition query supplied by DPS. 
* ws_StreetMaintZone.mxd  - This service was updated with a definition query to remove NOT IN SERVICE AREA zones from this service.  
* ws_StreetMaintZone_Other.mxd - This service was updated with a definition query to only display NOT IN SERVICE AREA zones from this service.
* ws_SweepZones.mxd - This provides a definition query to remove scheduled and no sweep zones.
* ws_SweepZones_Other.mxd - This provides a definition query to display scheduled and no sweep zones.



## Data Sources

All map and new map services display information from these tables. Definition queries are in place to control what information is displayed through the map service.

* GEP.WW.TBL_STREET_MAINT_ZONES
* GEP.WW.TBL_STREET_SWEEP_ZONES



## REST Services

All services have map services enabled only with default settings.

* \ws\ws_LabelsStreetMaint
* \ws\ws_LabelsStreetSweep 
* \ws\ws_SweepZones 
* \ws\ws_SweepZone_Other
* \ws\ws_StreetMaintZone
* \ws\ws_StreetMaintZone_Other

# Configuration Updates

**\Views\Accounts\Index.cshtml -** Label for route / zone management was updated. Now it says “Zones / Routes”
Please add Zone / on these two lines.

* Line 97: <li><strong>Zone / Route Management</strong></li>
* Line 204: Zone / Route<br /><span class="badge">@Roles.GetUsersInRole(approle + "_routes").Length.ToString()</span>


**\App_Data\Configs\Potholetracker.siteconfig - **Updated map services configuration to utilize new map services.


**\App_Data\Configs\Potholetracker.siteconfig - **Updated map services configurations to utilize new map services.


## Event Names

Event names on development environment were modified to follow current naming convention. See DPS_SnowEventNames.xlsx for details on event renaming. 


# Documentation

User documentation provided is focused on DPS and DoT.

## DPS User Guides

1) Landing Page User Guide

2) Warrior Watch Map User Guide

3) Warrior Watch Dashboard User Guide

4) Residential Sweeping User Guide

5) Pothole Repair User Guide

## User Videos

User videos are produced to document Warrior Watch and We Serve features. 

**Warrior Watch\**
WW_VehicleManagement.m4v
WW_AddressSearch.m4v
WW_AuxiliaryRoutes.m4v
WW_EventManagement.m4v
WW_LiveTrucks.m4v
WW_LiveTrucks-1.m4v
WW_MapTools.m4v
WW_NewsTicker.m4v
WW_Reports.m4v
WW_RouteStatus.m4v
WW_SearchHistory.m4v
WW_UserManagement.m4v

**WeServe\**



## DoT User Guides

1) Map Services

2) Geoevent Configuration

3) WW Database - Stored Procedures

4) Geoprocessing and Standard Reports

5) Internal WeServe Application Configuration

6) WeServe Landing Page Configuration

7) Public Configuration

8) Performance Monitor Configuration


