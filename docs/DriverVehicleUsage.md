# Driver Vehicle Usage Report

## Topics in this section:

*   [What is the purpose of the Driver Vehicle Usage Report?](#A)
*   [What information is displayed in the report?](#B)
*   [Why can't I view driver vehicle usage for more than one week at a time?](#C)
*   [Why do certain drivers' names link to other pages, but other drivers' names do not?](#D)
*   [I suspect that someone drove a vehicle on a particular date, but the report returns no results. Why?](#E)

## <a id="A">What is the purpose of the Driver Vehicle Usage Report?</a>

The Driver Vehicle Usage Report is intended to help organizations determine what vehicles a particular driver has used, or what drivers have been using a particular vehicle. The report retrieves this information from drivers' records of duty status (aka [driver logs](ViewLog.aspx)).

### To view the report for a particular driver:

1.  Select a name from the **Driver** drop-down list.
2.  Leave the **Vehicle ID** box blank.
3.  Select a start [date](FAQ_General.aspx#A.5) for the report.

    ##### To change the date:

    *   Click the **...** button to pop up the calendar.
    *   Click on the date desired.
4.  Select **Day** to view information for the selected date only, or **Week** to view information for up to seven days after the selected date.
5.  Click the **View** button.

### To view the report for a particular vehicle:

1.  Select (all) from the **Driver** drop-down list.
2.  Enter the Vehicle ID in the **Vehicle ID** box.
3.  Select a start date for the report.

    ##### To change the date:

    *   Click the **...** button to pop up the calendar.
    *   Click on the date desired.
4.  Select **Day** to view information for the selected date only, or **Week** to view information for up to seven days after the selected date.
5.  Click the **View** button.

## <a id="B">What information is displayed in the report?</a>

*   **Vehicle ID** - Identifies the vehicle
*   **Date** - A date on which the vehicle was used
*   **Driver(s)** - The driver(s) who are known to have used the vehicle on the corresponding date

## <a id="C">Why can't I view driver vehicle usage for more than one week at a time?</a>

The Driver Vehicle Usage Report searches all records of duty status (aka [driver log](ViewLog.aspx)) for the selected date range, looking for duty statuses associated with a vehicle. The greater the date range, the more system intensive the search. Restricting the date range ensures that your report will load faster, meaning better web application performance for all users.

## <a id="D">Why do certain drivers' names link to other pages, but other drivers' names do not?</a>

A driver's name will link to the driver's record of duty status (aka [driver log](ViewLog.aspx)) only if the driver has not been deleted. If you wish to view the driver log for a driver who has been deleted, you must first [restore the deleted driver](DriversList.aspx#D).

## <a id="E">I suspect that someone drove a vehicle on a particular date, but the report returns no results. Why?</a>

If the driver who used the vehicle failed to sign in to the HOS application, no duty status changes may have been recorded for that driver in that vehicle on that date. Check the [Conflicts Report](Conflicts.aspx) for any [Unidentified Driver](FAQ_DriverLogs.aspx#E.2.9) conflicts for the same date.
