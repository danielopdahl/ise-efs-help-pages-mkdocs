# Frequently Asked Questions - Group Filter

## Group Filter

*   [What is the purpose of the Group Filter?](#A)
*   [What Group Filter selections may be visible?](#B)
*   [When and where are changes to my current Group Filter selection applied?](#C)

## <a id="A">What is the purpose of the Group Filter?</a>

The **Group Filter** drop-down list appears in the upper right corner of the page. Its function is to control which drivers' records you can view at any given time.

The larger the organization, the more likely it is that multiple application users will attempt to display data for drivers at the same time. By permitting application users to display data for relatively small groups of drivers rather than all drivers at once, web server performance is improved and users are better able to find the information most relevant to them.

**Group Filters** work in conjunction with page-specific filters and report parameters. If you select a particular group from the **Group Filter** drop-down list and then select the **(all)** option from the **Driver** drop-down list in a report, information will be returned for all drivers in the selected group rather than all drivers in the organization.

## <a id="B">What Group Filter selections may be visible?</a>

*   **ALL** - Select this option to view records for all drivers that you have been granted access to.
*   **Home Terminals** - Select from the [home terminals](HomeTerminalList.aspx) listed to view records for only those drivers currently assigned to the selected home terminal.
*   **Driver Groups** - Select from any [driver groups](DriverGroupList.aspx) listed to view records for only those drivers currently assigned to the selected driver group.

    #### * Only those driver groups that you personally have created will be available for you to select.

## <a id="C">When and where are changes to my current Group Filter selection applied?</a>

When you change your current **Group Filter** selection, the new selection is applied on your next page (re)load. Your selection will be remembered the next time you sign in to application, and will not change unless you change it or your [Home Terminal Access](UserDetail.aspx#B) is changed.

The **Group Filter** is applied to any page that has a **Driver** drop-down list, controlling which drivers appear in the drop-down list and in the corresponding results list or table.
