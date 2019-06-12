# Availability Report

## Topics in this section:

*   [What is the purpose of the Availability Report?](#A)
*   [What information is displayed in the report?](#B)
*   [Why is N/A shown for some columns?](#D)
*   [Why is a question mark shown for Driving Time Left?](#E)
*   [What does the View Map button do?](#F)

## Related topics:

*   [What are the duty status abbreviations used throughout the HOS application?](FAQ_DriverLogs.aspx#A.1)
*   [How does the HOS application calculate availability and violations?](FAQ_DriverLogs.aspx#G.1)

## <a id="A">What is the purpose of the Availability Report?</a>

The **Availability Report** is intended to aid dispatchers and other office personnel in making an informed decision whether a driver is available to operate a commercial motor vehicle (CMV). Availability calculations are based on drivers' recent electronic driver logs and the hours of service rules for their assigned [driver type](FAQ_DriverLogs.aspx#A.2).

### To view availability for one or more drivers:

1.  Select a driver's name or (all) from the **Driver** drop-down list.
2.  _If country selection has been enabled for your organization,_ choose the [driver type](FAQ_DriverLogs.aspx#A.2) to use for calculations.
    *   Select **Use Primary Driver Type** to calculate using each selected driver's configured [primary driver type](DriversList.aspx#G).
    *   Select **Use US Driver Type** to calculate using each selected driver's configured US driver type, if any.
    *   Select **Use Canada Driver Type** to calculate using each selected driver's configured Canada driver type, if any.
3.  Click the **View Availability** button.

#### * If country selection has not been enabled for your organization, each driver's configured [primary driver type](DriversList.aspx#G) will be used. Country selection can be configured on the [Organization Detail](OrganizationDetail.aspx#B) page.

### Points to remember when viewing availability:

*   The [driver type](FAQ_DriverLogs.aspx#A.2) **must** correctly reflect the types of activities in which the driver is engaged at the moment. If the wrong driver type is assigned, the **Availability Report** cannot give a true indication of the driver's availability to drive.
*   The accuracy of availability calculations is dependent on the on the timeliness and completeness of information received by the web server. If a driver has forgotten to record a duty status change, or if a change has been made but not yet communicated to the web server, the **Availability Report** may not give a true indication of the driver's availability to drive.
*   Some calculations require analysis of the last eight full days of log data for _each driver included in the report_. Therefore, a report for multiple drivers can take significantly longer to generate than a report for just one driver.

#### * To minimize load time for the **Availability Report**, change your [Group Filter](GroupFilter.aspx) selection to a particular [home terminal](HomeTerminalList.aspx) or [driver group](DriverGroupList.aspx), rather than all drivers in the organization. Reports for small groups of drivers take less time to load than reports for large groups of drivers.

## <a id="B">What information is displayed in the report?</a>

*   **Driver** - The driver's name

    #### * All non-deleted drivers in the selected [group filter](GroupFilter.aspx) will be included in the **Availability Report**, excluding those with a HOS EXEMPT [driver type](FAQ_DriverLogs.aspx#A.2).

*   **Open Status** - The driver's last reported [duty status](FAQ_DriverLogs.aspx#A.1)
*   **Status Start** - The start [date](FAQ_General.aspx#A.5) and time of the driver's open duty status

    #### * This date and time is based on the [time zone of the driver log](FAQ_General.aspx#A.2) on which the duty status started.

*   **Status Location** - The starting location for the driver's open duty status
*   **Driving Time Left** - The total hours and minutes (hh:mm) remaining that a driver may continue to operate a [CMV](Glossary.aspx) without violating one or more hours of service limits

    This value is equal to the lowest of the values calculated for all applicable HOS rules.

*   **Work Shift Driving** - The remaining hours and minutes (hh:mm) that a driver may operate a [CMV](Glossary.aspx) during the current work shift
*   **Work Shift Rest Break** - The remaining hours and minutes (hh:mm) that a driver may be on duty before a rest break of at least 30 minutes is required to continue to operate a [CMV](Glossary.aspx) during the current work shift

    #### * This rule applies only to certain property-carrying drivers operating in US interstate commerce.

*   **Work Shift Duty** - The remaining hours and minutes (hh:mm) in the driver's current work shift after which the driver may no longer operate a [CMV](Glossary.aspx), even if they have **Work Shift Driving** time remaining
*   **Work Shift Elapsed** - The remaining hours and minutes (hh:mm), including off duty time, in the driver's current work shift after which the driver may no longer operate a [CMV](Glossary.aspx), even if they have **Work Shift Driving** time remaining

    #### * This rule applies only to drivers operating in Canada.

*   **Daily Driving** - The remaining hours and minutes (hh:mm) that a driver may operate a [CMV](Glossary.aspx) during the current 24 hour log period

    #### * This rule applies only to drivers operating in Canada.

*   **Daily Duty** - The remaining hours and minutes (hh:mm) that a driver may be on duty during the current 24 hour log period, after which the driver may no longer operate a [CMV](Glossary.aspx), even if they have **Daily Driving** time remaining

    #### * This rule applies only to drivers operating in Canada.

*   **Daily Off Duty** - The remaining hours and minutes (hh:mm) that a driver may be on duty during the current 24 hour log period, after which the driver must be relieved from duty until the next log period in order to satisfy mandatory and daily off duty rules

    #### * This rule applies only to drivers operating in Canada.

*   **Cycle Duty** - The overall remaining hours and minutes (hh:mm) that a driver may be on duty during the driver's [cycle](Glossary.aspx), after which the driver must not operate a [CMV](Glossary.aspx) . This overall value considers all cycle-related HOS rules that can limit cycle duty (e.g., cycle on duty, cycle elapsed, cycle on duty between off duty, cycle switching, cycle off duty periods, well service off duty periods and well service switching)

    #### * Most of these rules apply only to drivers operating in Canada.

*   **Cycle Off Duty Periods** - The remaining hours and minutes (hh:mm) that a driver may be on duty based on the cycle off duty periods HOS rule after which the driver must not operate a [CMV](Glossary.aspx).

    #### * This rule applies only to drivers operating in Canada.

*   **Gain Time At** - The next [date](FAQ_General.aspx#A.5) and time when **Driving Time Left** will increase, provided that the driver remains in the same duty status
*   **Projected Driving Time** - The anticipated **Driving Time Left** at the date and time shown in the **Gain Time At** column, provided that the driver remains in the same duty status

    #### * This date and time is based on the time zone of the driver's current [home terminal](HomeTerminalList.aspx).

*   **Comments** - An icon may appear in this column to indicate additional information regarding the availability calculations. Click or hover over the icon to show this information.

## <a id="D">Why is N/A shown for some columns?</a>

**N/A** indicates that an accurate value cannot be computed or displayed for a driver.

### Possible reasons for **N/A** to be shown include:

*   **Driver has no driver type for the selected country** - If country selection is enabled and **Use US Driver Type** or **Use Canada Driver Type** is selected, values will not be shown if the driver has no driver type defined for the selected country.
*   **Rule does not apply to driver type** - A value will not be shown if the corresponding rule is not applicable to the driver's [driver type](FAQ_DriverLogs.aspx#A.2). For example, **Daily Driving**, **Daily Duty** and **Daily Off Duty** may be shown as **N/A** for US driver types; **Work Shift Rest Break** will be shown as **N/A** for driver types (including all Canada driver types) that are not subject to a rest break rule.
*   **Rule does not apply at this time of day** - A value will not be shown for **Daily Driving**, **Daily Duty** and **Daily Off Duty** if it is impossible for the driver to violate the rule before the end of the current 24 hour log period.
*   **Not enough history** - Some values cannot be calculated until the driver has sufficient electronic driver log information available for analysis.
*   **Unable to determine start of work shift** - Some values cannot be calculated unless the driver has recently had a rest period of sufficient length (typically, ten hours for property carriers or eight hours for passenger carriers) to signal the beginning of a new work shift
*   **Conflicts have been detected** - Some values will not be calculated if certain [conflicts](FAQ_DriverLogs.aspx#E.1) exist that could affect the accuracy of the calculation. Such conflicts include [Conflicting Driver Activity](FAQ_DriverLogs.aspx#E.2.1), [Conflicting Vehicle Activity](FAQ_DriverLogs.aspx#E.2.2) and [Gap in Log](FAQ_DriverLogs.aspx#E.2.4).
*   **Time zone change** - Some values cannot be calculated if the driver's [time zone has changed](ViewLog.aspx#I) during the range of dates used for analysis.

#### * If **N/A** appears for one or more columns for a particular driver, click on the icon in the **Comments** column on that row to see more information.

## <a id="E">Why is a question mark shown for Driving Time Left?</a>

A question mark (?) means that the system cannot confidently calculate **Driving Time Left** due to incomplete information. The number shown should be considered a "best guess" calculation based on the information that is available to the system; it is **NOT** guaranteed to be accurate. Drivers and support personnel should refer to the driver's paper records of duty status for a complete and accurate determination of driving time left.

## <a id="F">What does the View Map button do?</a>

Clicking the **View Map** button displays the [Maps View](MapsView.aspx) page using the same parameters selected for the **Availability Report**. If **(all)** is selected in the **Driver** drop-down list, the map will show the last known locations of all drivers in the selected [group filter](GroupFilter.aspx); if a single driver is selected, the map will show the movements of that driver on the current day.

#### * This button is visible only if the Mapping application is enabled and the viewer has a [user role](UserRoleList.aspx) with View Only or View/Modify permission to the **Telemetry Data** feature.