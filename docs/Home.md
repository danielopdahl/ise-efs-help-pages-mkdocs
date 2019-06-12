# Home

The Home page summarizes important information and provides shortcuts to critical features.

## <a id="A">Driver Portal</a>

#### * This section is visible only if the HOS application is enabled and the viewer is a [driver](DriversList.aspx).

This section provides a driver with the means to view and to change the driver's duty status without signing in to a mobile logging device.

To change your duty status, click the **Change My Status** button to display the [Change My Status](ChangeMyStatus.aspx) page.

## <a id="B">Home Page Summary</a>

This section displays counts for the following items. Each count is a button that when clicked upon, runs and displays the corresponding report.

*   [Provisioned Devices](DevicesList.aspx) - Displays the total number of devices for this organization with a status of Provisioned.

    #### * This button is visible only if the viewer has a [user role](UserRoleList.aspx) with View Only or View/Modify access to the Devices feature.

*   [Conflicts](Conflicts.aspx) - Displays the number of unresolved conflicts on a driver's record of duty status (aka [driver log](ViewLog.aspx)) in the last 15 days. Conflicts must be resolved before drivers can download their driver logs to a mobile logging device.

    #### * This button is visible only if the HOS application is enabled, and the viewer has a [user role](UserRoleList.aspx) with View Only or View/Modify access to the HOS Reports feature.

*   [Unidentified Driver](Conflicts.aspx) - Displays the number of unassigned Driving statuses in the last 15 days that were recorded but not [assigned to a selected driver](ConflictResolution.aspx#B) or [marked as Won't Assign](ConflictResolution.aspx#C).

    #### * This button is visible only if the HOS application is enabled, and the viewer has a [user role](UserRoleList.aspx) with View Only or View/Modify access to the HOS Reports feature.

*   [Uncertified Logs](CertificationReport.aspx) - Displays the number of recent [driver logs](ViewLog.aspx) that must be certified or recertified by the driver.

    #### * This button is visible only if the HOS application is enabled and the viewer is a [non-ELD Exempt](DriversList.aspx#G) driver or has a [user role](UserRoleList.aspx) with View Only or View/Modify access to the HOS Reports feature.

### Points to remember about counts shown on the Home Page:

*   For a non-driver user role, the number of **Conflicts** and **Uncertified Logs** shown, represent the total items for the drivers that are in the currently selected [group filter](GroupFilter.aspx).
*   The number of **Uncertified Logs** shown on a driver's home page automatically reflect only that driver's [uncertified logs](CertificationReport.aspx).
