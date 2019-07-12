---
title: "Uninstall Steps"
parent: "ig-one"
menu_order: 3
---

## 1 Introduction

This chapter describes the uninstallation of the APM tool. The optional in this chapter means you need to verify if this option was chosen during the install before undoing it.

## 2 Backup

Did you commit your work to the team server? And did you make a database backup?
![](attachments/ig-one-uninstall-steps/Delete_Module.png)

If you don't have installed an SVN client like Tortoise SVN make a copy of the widgets folder in your project.

## 3 Delete Module APMAgent

Import the module APMAgent in the modeler.
![](attachments/ig-one-uninstall-steps/Commit.png)

## 4 Delete Mansystems customized widgets

Mansystems customized versions of AppStore widgets

* ManTooltip.mpk
* StringFormatter.mpk
* CssSelectorHelperBoolean.mpk
* StyleSheetSwap.mpk
* MicroflowTimer_APM.mpk
* FormatString_APM.mpk
* ChartJS_APM.mpk
* BootstrapTreeViewWidget_APM.mpk
* BooleanSlider_APM.mpk

## 5 Delete permissions

Delete permissions APMAgent.Admin from project security / user roles tab to a selected administrator role. On Edit of the last dialog Mendix will remove the permissions for you.
![](attachments/ig-one-uninstall-steps/Delete_Permissions.png)

**_Note._** _If you added the Debug role, remove it now._

## 6 Delete from navigation

Delete the APM Tools item that calls "APMAgent/USE_ME/IVK_OpenConsole" from navigation.

![](attachments/ig-one-uninstall-steps/Delete_From_Navigation.png)

## 7 Optional: Revert After startup and before shutdown

Remove the call microflow action to APMAgent\USE_ME\AfterStartup from an after startup microflow. This feature is runtime configurable and by default none of the tools are started.
Remove the call microflow action to APMAgent\USE_ME\BeforeShutdown from a before shutdown microflow.
You can find the AfterStartup and BeforeShutdown microflows in the project settings.

![](attachments/ig-one-uninstall-steps/Revert_After_Startup.png)

## 8 Optional: Undo request permissions for the Mendix cloud or on premise runtime

For a Mendix Cloud slot you send an email to Mendix support requesting to undo the added permissions

## 9 Remove user libraries

Remove the APMAgent libraries in the project folder 'userlib':

*   apm
*   com.mendix.ojdbc6.jar
*   com.mendix.postgresql.jdbc4.jar
*   com.mendix.sqljdbc4.jar
*   org.hsqldb.hsqldb.jar
*   org.mariadb.jdbc.jar
*   log4j

## 10 Start the Modeler or the Runtime

Clean deployment and startup.