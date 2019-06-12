# Violations Report

## Topics in this section:

*   [What is the purpose of the Violations report?](#A)
*   [What information is contained in the report?](#B)
*   [When is a violation reported?](#C)
*   [Why is N/A shown for some columns?](#D)
*   [Why is the same rule listed multiple times for the same driver?](#E)

## Related topics:

*   [How does the HOS application calculate availability and violations?](FAQ_DriverLogs.aspx#G.1)
*   [Why hasn't a violation been reported for a driver, even though the Availability Report shows that the driver's availability is 00:00?](FAQ_DriverLogs.aspx#G.2)

## <a id="A">What is the purpose of the Violations report?</a>

The **Violations Report** is intended to aid supervisors and compliance personnel in determining whether a driver has violated any applicable hours of service rules. These rules are based on the driver's assigned [driver type](FAQ_DriverLogs.aspx#A.2).

### To view violations for one or more drivers:

1.  Select a driver's name, or **(all)**, from the **Driver** drop-down list.
2.  Select the range of dates for which you wish to view any violations.

    ##### To change a date:

    *   Click the **...** button to pop up the calendar.
    *   Click on the desired date.
3.  _If country selection has been enabled for your organization,_ choose the [driver type](FAQ_DriverLogs.aspx#A.2) to use for calculations.
    *   Select **Use Primary Driver Type** to calculate using each selected driver's configured [primary driver type](DriversList.aspx#G).
    *   Select **Use US Driver Type** to calculate using each selected driver's configured US driver type, if any. Drivers for whom a US driver type has not been defined will be excluded from the report.
    *   Select **Use Canada Driver Type** to calculate using each selected driver's configured Canada driver type, if any. Drivers for whom a Canada driver type has not been defined will be excluded from the report.
4.  Click the **View Violations** button.

#### * If country selection has not been enabled for your organization, each driver's configured [primary driver type](DriversList.aspx#G) will be used. Country selection can be configured on the [Organization Detail](OrganizationDetail.aspx#D) page.

## <a id="B">What information is contained in the report?</a>

*   **Driver** - The driver's name
*   **Rule** - The HOS rule that was violated
*   **Start** - The earliest date and time that the driver operated in violation of the rule within the range of dates selected

    Click on the date link to display the [Driver Logs](ViewLog.aspx) page for the driver and date shown.

*   **End** - The latest date and time that the driver operated in violation of the rule within the range of dates selected
*   **Time Driving in Violation** - The total hours and minutes (hh:mm) that the driver operated in violation of the rule within the range of dates selected
*   **Comments** - An icon may appear in this column to indicate additional information regarding the violation calculations. Click or hover over the icon to show this information.

If the driver's [time zone has changed](ViewLog.aspx#I), the **Violations Report** will be unable to calculate cycle duty violations for some period of time immediately following the time zone change. In this case, the **Start** and **End** columns will reflect the range of dates and times during which cycle duty violations cannot be computed.

#### * All [dates](FAQ_General.aspx#A.5) and times in the **Violations Report** are based on the time zone of the driver log on which the violation began.

## <a id="C">When is a violation reported?</a>

A violation is reported if a driver operates a commercial motor vehicle in excess of the hours of service limits established for the driver's [driver type](FAQ_DriverLogs.aspx#A.2). If a driver runs out of driving time _**but does not drive**_ after time has expired, a violation generally will not be reported. Canada's **Daily Off Duty** rule (which establishes a minimum off duty requirement, rather than a maximum driving or duty limit) is the only rule for which a violation may be reported even though the driver has stopped driving.

Violations are calculated only for **Driving** ([D](FAQ_DriverLogs.aspx#A.1.D)) statuses for which the end time is known. This is to prevent false reports in the case that a driver has stopped driving, but the driver's next subsequent status change has not yet been communicated to the web server.

## <a id="D">Why is N/A shown for some columns?</a>

**N/A** indicates that an accurate value cannot be computed or displayed for a driver.

### Possible reasons for N/A to be shown include:

*   **Not enough history** - Some values cannot be calculated until the driver has electronic driver logs for every day in the current [cycle](Glossary.aspx) available for analysis.
*   **Conflicts** - Some values cannot be calculated if certain [conflicts](FAQ_DriverLogs.aspx#E.1) exist.

    ##### These conflicts include:

    *   [Conflicting Driver Activity](FAQ_DriverLogs.aspx#E.2.1)
    *   [Conflicting Vehicle Activity](FAQ_DriverLogs.aspx#E.2.2)
    *   [Gap in Log](FAQ_DriverLogs.aspx#E.2.4)
*   **Time zone change** - Some values cannot be calculated if the driver's [time zone has changed](ViewLog.aspx#I) during the range of dates used for analysis.

If **N/A** appears for one or more columns for a particular driver, click on the icon in the **Comments** column on that row for more information.

## <a id="E">Why is the same rule listed multiple times for the same driver?</a>

If a driver broke the same rule multiple times within the range of dates selected for the report, each instance may be reported as a separate violation.

For example, if a driver exceeded his **Work Shift Driving** limit two days in a row, but took enough consecutive hours off duty between the two days to start a new work shift, two separate **Work Shift Driving** violations will be reported, one for each day. If, however, the driver did not take enough hours off duty to start a new work shift, the driving on day two will be added to the **Work Shift Driving** violation reported on day one, lengthening the **Time Driving in Violation** for the existing violation.