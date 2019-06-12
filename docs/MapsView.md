# Maps View

## Topics in this section:

*   [Viewing a map](#A)
*   [Using the map controls](#B)
*   [What information is displayed when viewing a map for all drivers?](#C)
*   [What icons are shown when viewing a map for all drivers?](#D)
*   [What information is displayed when viewing a map for a single driver?](#E)
*   [What icons are shown when viewing a map for a single driver?](#F)
*   [What information is displayed when viewing a map for all vehicles?](#G)
*   [What icons are shown when viewing a map for all vehicles?](#H)
*   [How do I find the last reported location of a driver or vehicle?](#I)
*   [Why is N/A shown for some icons or table columns?](#J)
*   [What is the meaning of the cluster icons sometimes displayed on the map?](#K)
*   [What is the meaning of the magnifying glass visible for some rows in the table?](#L)
*   [What is a breadcrumb?](#M)

## <a id="A">Viewing a map</a>

The **Mapping** application provides a combination of location and compliance data, giving dispatchers the information they need to quickly and accurately locate fleet assets and make critical decisions.

### To view the location, status, and availability of all drivers:

1.  Select **Drivers** from the **Display** drop-down list.
2.  Select **(all)** from the next drop-down list.
3.  Click the **View Map** button.

### To view the breadcrumb trail (activity and movement) for a single driver:

1.  Select **Drivers** from the **Display** drop-down list.
2.  Select a driver's name from the next drop-down list.
3.  Select the date you wish to view.

    ##### To change the date:

    *   Click the **...** button to pop up the calendar.
    *   Click on the date desired.
4.  Click the **View Map** button.

### To view the last reported location and motion status for all vehicles:

1.  Select **Vehicles** from the **Display** drop-down list.
2.  Select **(all)** from the next drop-down list.
3.  Click the **View Map** button.

## <a id="B">Using the map controls</a>

### Zooming:

*   Click on the zoom control buttons in the upper left corner of the map.
*   Double click on a map location to zoom in and center on that position.
*   Use the mouse scroll wheel movements over the map region.
*   Hold the shift key while clicking and dragging the cursor to define a specific rectangular area to zoom into.
*   Click the **View Map** button to reset the map to the default zoom level.

### Panning:

*   Use the arrow buttons in the upper left corner of the map.
*   Click-and-drag the cursor on the map.

### Changing Map Views and Overlays:

*   Click the plus symbol ![Change views](../ALKMaps/img/layer-switcher-maximize.png) in the upper right corner of the map to:
    *   Change the map between street (**Road**) and hybrid (**Aerial With Labels**) views. The map defaults to street view each time you begin a new browser session.
    *   Show or hide icons (for drivers, vehicles, or a location marker) and overlays (weather and live traffic).

### Show Location Details:

*   Click an icon on the map,

    ##### OR

*   Click a ![Find icon](../Images/MapIcons/system-search.png) [magnifying glass](#M) in the table.

### Hide Location Details:

*   Click the close button ![Close button](../ALKMaps/theme/default/img/close.gif) in the upper right corner of details window,

    ##### OR

*   Click elsewhere on the map.

### Address Search:

*   Enter a full or partial street address and city in the **Address** box.
*   Click the **Search** button.

If multiple location matches are found, the best match will be selected automatically and the map will be centered on that location with a pin marking the address. Click on the pin to display the location returned by the mapping provider.

## <a id="C">What information is displayed when viewing a map for all drivers?</a>

This map shows the following information for all non-deleted drivers in the selected [group filter](GroupFilter.aspx).

*   **Driver** - The driver whose information is shown

    Click a driver's name to display a [breadcrumb trail](#E) for that driver and today's [date](FAQ_General.aspx#A.5).

*   **Vehicle** - The Vehicle ID (if any) associated with the driver's open duty status
*   **Status** - The most recent duty status that has been reported for the driver (aka the "open" duty status)
*   **Availability** - The total hours and minutes (hh:mm) remaining before a driver will be in violation of one or more applicable HOS rules if the driver continues to operate a commercial motor vehicle
    *   This value is calculated using the driver's configured [primary driver type](DriversList.aspx#G).
    *   A **?** is shown next to the this value if it there is not enough history available to calculate the time left for all applicable HOS rules.
*   **Last Update** - The [date](FAQ_General.aspx#A.5) and time of the driver's most recent location update

    #### * **Last Update** date and time is based on your [user preference](UserPreferences.aspx) for time zone.

## <a id="D">What icons are shown when viewing a map for all drivers?</a>

Viewing a map for all drivers shows the current location and estimated availability for each driver. Therefore, various icons are shown to denote the current availiblity status of each driver.

### Icons that may be shown on the map for all drivers:

*   ![In emergency](../Images/MapIcons/availability_exempt_not_off_duty.png) - The driver is currently in an emergency or exempt status
*   ![Not applicable](../Images/MapIcons/availability_NA_not_off_duty.png) - Availabilty is currently not applicable to this driver
*   ![Less than an hour](../Images/MapIcons/availability_critical_not_off_duty.png) - Current availabilty time for this driver is less than an hour
*   ![Less than three hours](../Images/MapIcons/availability_warn_not_off_duty.png) - The driver has less than three hours of available drive time
*   ![More than three hours](../Images/MapIcons/availability_normal_not_off_duty.png) - The driver has more than three hours of available drive time
*   ![Off Duty](../Images/MapIcons/off_duty.png) - This symbol on a availibilty icon (i.e. ![More than three hours and off duty](../Images/MapIcons/availability_normal_off_duty.png)) means that the driver is currently in an off duty status
*   ![Driver Cluster](../Images/MapIcons/driver_cluster1.png) - There is a [cluster](#K) of drivers whose last recorded location is at this point on the map

## <a id="E">What information is displayed when viewing a map for a single driver?</a>

This map shows the [breadcrumb](#M) trail for the selected driver on the selected [date](FAQ_General.aspx#A.5). Breadcrumbs are derived from duty status changes, driver vehicle inspection reports, and periodic vehicle location samples.

*   **Event** - The event type associated with this breadcrumb
*   **Date/Time** - The [date](FAQ_General.aspx#A.5) and time of the breadcrumb

    #### * Breadcrumb dates and times are based on the time zone of the [home terminal](HomeTerminalList.aspx) to which the driver was assigned on the selected date.

*   **Details** - The details associated with this breadcrumb
*   **Vehicle** - The Vehicle ID, if any, associated with this breadcrumb

## <a id="F">What icons are shown when viewing a map for a single driver?</a>

*   ![Driver is off duty](../Images/MapIcons/driver_off_duty.png) - The driver's status was Off Duty at this location
*   ![Driver is on duty](../Images/MapIcons/driver_on_duty.png) - The driver was On-Duty at this location
*   ![Driver is driving](../Images/MapIcons/driver_driving.png) - The driver was reported as driving at this location
*   ![Driver is in sleeper berth](../Images/MapIcons/driver_sleeper_berth.png) - The driver went into sleeper berth at this location
*   ![DVIR with no defects](../Images/NoDefects.png) - A DVIR with no defects was filed at this location
*   ![DVIR with normal defects](../Images/NormalPriorityDVIR.png) - A DVIR with normal defects was filed at this location
*   ![DVIR with high priority defects](../Images/HighPriorityDVIR.png) - A DVIR with high priority defects was filed at this location
*   ![Driver action cluster](../Images/MapIcons/flag_tall.png) - [Several events](#K) for this driver happened on or near this location

## <a id="G">What information is displayed when viewing a map for all vehicles?</a>

The following information is shown for all non-deleted vehicles in the organization.

*   **Vehicle** - Identifies the vehicle
*   **Vehicle Status** - The vehicle's motion status at the time of the last location update
*   **Last Update** - The date and time of the most recent location update received for the vehicle

    #### * **Last Update** date and time is based on your [user preference](UserPreferences.aspx) for time zone.

*   **Driver(s)** - The name(s) of any drivers with an open duty status associated with this vehicle

    #### * Click a driver's name to display today's [breadcrumb trail](#E) for that driver.

## <a id="H">What icons are shown when viewing a map for all vehicles?</a>

*   ![Truck in motion](../Images/MapIcons/truck_moving.png) - Last reported status was in motion
*   ![Truck is stopped](../Images/MapIcons/truck_not_moving.png) - Most recent motion status reported as stopped
*   ![Several trucks](../Images/MapIcons/truck_cluster30.png) - A [cluster](#K) of vehicles have this point as their last reported location

## <a id="I">How do I find the last reported location of a driver or vehicle?</a>

*   View the map for all drivers to see the last location reported for each driver in the table.

    ##### OR

*   View the map for all vehicles to see the last location reported for each vehicle in the table.
*   Click the ![Find icon](../Images/MapIcons/system-search.png) [magnifying glass](#M) to center the map on the corresponding location.

#### * Maps do not automatically refresh when a location update is received. Click the **View Map** button to redisplay the map including any new location data.

## <a id="J">Why is N/A shown for some icons or table columns?</a>

**N/A** indicates that an accurate value cannot be computed or displayed.

### Possible reasons for N/A to be shown for a driver's availability include:

*   **Not enough history** - Availability cannot be calculated until the driver has electronic driver logs for every day in the current [cycle](Glossary.aspx) available for analysis
*   **Conflicts** - Availability cannot be calculated if certain [conflicts](FAQ_DriverLogs.aspx#E.1) exist. These conflicts include [Conflicting Driver Activity](FAQ_DriverLogs.aspx#E.2.1), [Conflicting Vehicle Activity](FAQ_DriverLogs.aspx#E.2.2), and [Gap in Log](FAQ_DriverLogs.aspx#E.2.4)
*   **Time zone change** - Availability cannot be calculated if the driver's [time zone has changed](ViewLog.aspx#I) during the range of dates used for analysis

**N/A** will be shown for a driver's or vehicle's **Last Update** if the mobile logging device has not sent such information to the web server since the device was installed or the driver began using the device.

## <a id="K">What is the meaning of the cluster icons sometimes displayed on the map?</a>

Cluster icons are shown when multiple drivers (![Driver Cluster](../Images/MapIcons/driver_cluster1.png)) or vehicles (![Several trucks](../Images/MapIcons/truck_cluster30.png)) are in the same location; zooming in on the map may separate these clusters into individual icons, depending on the actual distance between the drivers or vehicles. Cluster icons may also be shown when viewing the [breadcrumb trail](#E) for a single driver if multiple breadcrumb events (![Driver action cluster](../Images/MapIcons/flag_tall.png)) were recorded at the same place.

## <a id="L">What is the meaning of the magnifying glass visible for some rows in the table?</a>

If a row is preceded by a ![Find icon](../Images/MapIcons/system-search.png) magnifying glass, the item in that row is associated with a GPS location that can be viewed on the map. Click the magnifying glass to center the map on the corresponding location and show location details.

#### * If there are many rows in the table, you may need to scroll up to see the location detail on the map.

## <a id="M">What is a breadcrumb?</a>

A breadcrumb is simply a point on the map. Breadcrumbs are used to show what events happened at what location. Various symbols are used throughout the map to denote the type of event that happened at each breadcrumb.
