---
title: "Create & Test a Native Mobile App"
parent: "native-mobile"
menu_order: 10
description: A how-to for creating a native mobile Mendix app and viewing it on a mobile device.
tags: ["native", "mobile", "developer", "test"]
---

## 1 Introduction

To use Mendix Studio Pro's native app capabilities, you can either start using a Blank app or download the Native Mobile Quickstart app. This how-to uses the latter, because it is optimized to quickly build a native mobile app. Out of the box this app gives you a native page, a native phone profile to enable native device navigation, a native layout with menus, and native widgets and actions which leverage device capabilities.

The Native Mobile Quickstart app also includes four modules:

* **Administration** – helps you manage users
* **Atlas UI Resources package** – allows for app styling
* **Nanoflow Commons** – helps model out client-side logic
* **Native Mobile Actions** – contains JavaScript actions specific to native mobile apps

## 2 Prerequisites {#prerequisites}

Before starting this how-to, make sure you have completed the following prerequisites:

* Have a mobile device to test your native app 
* For information on browser and device requirements, see [System Requirements](/refguide/system-requirements)
* If you wish to use an emulator for Android mobile testing, install a product such as [Bluestacks](https://www.bluestacks.com/nl/index.html) or [Genymotion](https://www.genymotion.com/) (your emulator must have Google Play services supported)

## 3 Creating a New Project Based on the Quickstart App{#quickstartapp}

{{% todo %}}[add Apple App Store link to MakeItNative app]{{% /todo %}}

For details on making an app using the Native Mobile Quickstart app template, download the [Make It Native](https://play.google.com/store/apps/details?id=com.mendix.developerapp) app. Using the Make It Native app to view the changes to your app, see the sections below.

### 3.1 Starting a Quickstarter App Project

To start a new app based on a template, follow these steps:

1.  Open Mendix Studio Pro. Select **File** > **New Project** , and then select the Native Mobile Quickstart app: 

	{{% image_container width="500" %}}![mobile quickstart app](attachments/getting-started-with-native-mobile/native-mobile-quickstart.png){{% /image_container %}}

2.  Next, click **Use this starting point**:

	![starting point button](attachments/getting-started-with-native-mobile/use-this-starting-point.png)

3.  Click **Create app** to close the dialog box:

	{{% image_container width="500" %}}![create app button](attachments/getting-started-with-native-mobile/create-app.png){{% /image_container %}}

4.  Click **Run Locally** to see the app in action:

	![run locally button](attachments/getting-started-with-native-mobile/run-locally.png)

5.  After running your app, you may see a Windows Security Alert dialog box. Accept the permissions selected by default and click **Allow access** to close the dialog box: 

	{{% image_container width="500" %}}![firewall dialog box](attachments/getting-started-with-native-mobile/firewall-dialog.png){{% /image_container %}}

6.  If asked to create database **'default'**, click **Yes**:

	{{% image_container width="500" %}}![database dialog box](attachments/getting-started-with-native-mobile/database-dialog.png){{% /image_container %}}

At this point you have a running native app. To view your app on a mobile device, however, you need to download the Make It Native app.

### 3.2 Downloading the Make It Native App

To view your app on a mobile device, you must install the Make It Native app. The sections below describe two options for doing this.

{{% todo %}}[replace screenshot below with two app store screens when they get new logos?]{{% /todo %}}

#### Option 1: Use the App Store for Your Device

Search for the Make It Native app in the App Store or download it from [Google Play](https://play.google.com/store/apps/details?id=com.mendix.developerapp) and install it to your mobile device:

{{% image_container width="500" %}}![native app on googleplay](attachments/getting-started-with-native-mobile/make-it-native-googleplay.png){{% /image_container %}}

#### Option 2: Using Mendix Studio Pro

{{% todo %}}[The two app store buttons mentioned below do not exist yet. Update with pic later.]{{% /todo %}}

Alternatively, you can navigate to the Make It Native app using Mendix Studio Pro: 

1. In Mendix Studio Pro, click the drop-down menu next to the **View button**, and then click **View in the Mendix App**.
2. This will bring up a dialog box. In the **Native mobile** tab, click either **Go to play store** or **Go to app store** to be brought to the Google Play or Apple App Store pages for the Make It Native app.
3. In the iOS or Android app store, you can download the Make It Native app to your device of choice.

### 3.3 Viewing Your App on Your Testing Device

Viewing your app on a mobile device will allow you to test native features and other aspects of your app. This section is written for mobile devices, but you may use an Android emulator mentioned in the [Prerequisites](#prerequisites) section above. To view your app, follow these steps:

1. Locate your app's QR code in Mendix Studio Pro by clicking the drop-down menu next to the **View** button, then selecting **View in the Mendix App** and navigating to the **Native mobile** tab. Here you will see your test app's QR code.
2. Start the Make It Native app by tapping its icon on your device.
3.  Tap the  **Scan a QR Code** button:

	{{% image_container width="500" %}}![Scan QR Code](attachments/getting-started-with-native-mobile/scan-qr.png){{% /image_container %}}

4. If prompted, grant the app permission to access your device's camera.
5. Point your mobile device's camera at the QR code. It will automatically launch your test app on your mobile device.

{{% alert type="warning" %}}

Your mobile device has to be on the same network as your development machine for the Make It Native app to work. If this is the case and the connection still fails, make sure that communication between devices is allowed in the Wi-Fi access point.

{{% /alert %}}

Now you can see your app on your device. While this is just a template app, whenever you make changes you will be able to view them live on your Make It Native app.

You may notice an **Enable dev mode** toggle on the Make It Native app home page. Turning this toggle on will give you more detailed warning messages during error screens, as well as additional functionality on the developer app menu.

{{% image_container width="500" %}}![enable dev mode](attachments/getting-started-with-native-mobile/enable-dev-mode.png){{% /image_container %}}
	
{{% todo %}}[link to future debug doc - For more information on debugging, see Debugging A Native Mobile App]{{% /todo %}}

### 3.4 Viewing Changes to Your App on Your Testing Device {#viewingchanges}

To see how changes made in Mendix Studio Pro are displayed live on your testing device, make a small change to your app.

1.  Put a text widget on your app's home page. Then, write some text into it. In this example, "Native rules!" has been added: 

	![new studio pro text](attachments/getting-started-with-native-mobile/new-text-studiopro.png)

2.  Click **Run Locally** to automatically update the running app on your device, and see your new text:

	![new app text](attachments/getting-started-with-native-mobile/new-text-app.png)
	
	When you click **Run Locally**, your app will automatically reload while keeping state. 

Should you get an error screen while testing your app, there are easy ways to restart it: 

* Tap your test app with three fingers to restart your app
* With the **Enable dev mode** toggle turned on, hold a three-fingered tap to bring up the developer app menu – here you can access **ADVANCED SETTINGS** and **ENABLE REMOTE JS DEBUGGING** 

{{% todo %}}[(link to future debug doc at the end of the last bullet above)]{{% /todo %}}

## 4 Read More

* [Build Pluggable Widgets](../extensibility/pluggable-widgets)
* [Native Styling](/refguide/native-styling-refguide)