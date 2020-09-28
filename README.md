<span style="color:red">**[STATUS: IN PROGRESS]**</span>

[Metr App](https://metr.at) is probably™️ the most advanced telemetry app for electric skateboards. As amount of features continued to grow over the years the time has come for the proper guide to explain the basics and some hidden secrets in the app.

This guide will be improving over time and hopefully some day will cover everything the app has to offer. Before you start reading there are two very important things you need to know. In order to use it you must have:

* [VESC®](https://vesc-project.com)-based controller
* [Metr Pro](https://metr.at/shop) bluetooth module

If your skateboard has another controller, the app will not work for you. For example Boosted, Evolve, Mellow, Meepo, WowGo, Backfire have another type of controller and are not compatible.


### Contents

[🐣 First time setup](#heading--firsttime)  
[⚙️ Metr Pro firmware](#heading--metrprofwupdate)  
[📈 Realtime](#heading--realtime)  
[🐌 Modes](#heading--modes)  
[⏺ Records](#heading--records)  
[👤 Account](#heading--account)  
[🛑 Faults](#heading--faults)  
[🎓 Expert](#heading--expert)  
[⚡️ Discharger](#heading--discharger)  
[📣 Announcements](#heading--announcements)  
[⚙️ Settings](#heading--settings)  
[🌉 TCP Bridge](#heading--tcpbridge)  
[🔢 Overlay](#heading--overlay)  
[🔋 DieBieMS](#heading--diebiems)  
[🔋 FlexiBMS](#heading--flexibms)  
[🔋 LLT BMS](#heading--lltbms)  
[🛠 Troubleshooting](#heading--troubleshooting)  

<h3 id='heading--firsttime'>🐣 First time setup</h3>

Follow the instructions at [metr.at/setup](https://metr.at/setup)

<h3 id='heading--metrprofwupdate'>⚙️ Metr Pro firmware</h3>

In order to use all applications latest features it is important that your Metr Pro has the latest firmware. You can check it by going to Settings and clicking on the blue gear near the module name.

<img src="https://rpasichnyk.github.io/metr-guide/fwupdate.gif" width="320">

Click Upgrade and wait until firmware update over BLE is complete.

<h3 id='heading--realtime'>📈 Realtime</h3>

Shows values such as voltage, current, temperature from your VESC at any given time. Each value is displayed in it's own cell. Following cells are available:

* Voltage
* Cell voltage (per cell)
* Battery charge (%)
* Battery current
* Motor current
* ESC temperature
* Motor temperature
* Distance
* Duty cycle (%)
* Amp hours (+regen)
* Watt hours (+regen)
* Speed, GPS speed
* Elevation (above sea level)
* Consumption (Wh/km)

It is possible to arrange/show/hide/resize/recolour cells:

* Long press anywhere on Realtime page to enter Layout Editing mode
* Tap a cell to show / hide
* Drag to change position
* Long press and drag to resize
* Touch colour palette to change colour, long press a colour to expand more colours

<img src="https://rpasichnyk.github.io/metr-guide/realtime1.mp4.gif" width="320">

There is an indicator in the bottom which shows currently selected BLE module and connection status, ESC hardware name and firmware version. It blinks every time new packet from VESC is received.

<img src="https://rpasichnyk.github.io/metr-guide/status1.mp4.gif" width="220">

There are 2 Realtime screens available. You can customize any of them.

<img src="https://rpasichnyk.github.io/metr-guide/realtime2.mp4.gif" width="320">

You can click on small watch icons to select which data will be displayed on the smart watch. Apple watchOS and Android Wear is supported. You can select up to 4 cells.

<img src="https://rpasichnyk.github.io/metr-guide/realtime_watch.mp4.gif" width="320">

<h3 id='heading--modes'>🐌 Modes</h3>

You can setup a number of modes (profiles) to change max speed, acceleration and braking power. The recommended way to create a new mode is to read existing config from VESC and then change values.

<img src="https://rpasichnyk.github.io/metr-guide/mode-new.mov.gif" width="320">

To apply a mode, swipe it to the right. The mode will be automatically applied to all VESCs connected via CAN bus

<img src="https://rpasichnyk.github.io/metr-guide/mode-apply.mov.gif" width="320">

To rename a mode, open it and click on the name

<img src="https://rpasichnyk.github.io/metr-guide/mode-rename.mov.gif" width="320">

You can also share modes

<img src="https://rpasichnyk.github.io/metr-guide/mode-share.png" width="400">

<h3 id='heading--records'>⏺ Records</h3>

Records can be started and stopped automatically (configurable in Settings → Records). If  the app is running in the background it will automatically detect selected BLE module, connect to it and start a new record.

To export raw JSON data open your record in the browser and add `?format=json` in the address bar.

<h3 id='heading--account'>👤 Account</h3>

You can sign in to your account at [https://metr.at/account](https://metr.at/account) and view stats and all records for currently selected Metr Pro module. The sign in is done using public key cryptography instead of a password. You need to have active connection to Metr Pro in order to sign in.

<img src="https://rpasichnyk.github.io/metr-guide/account.mov.gif" width="320">

<h3 id='heading--faults'>🛑 Faults</h3>

All faults that happen to VESC while it's connected to the app are recorded and can be seen in a separate tab

<img src="https://rpasichnyk.github.io/metr-guide/faults.mov.gif" width="320">

<h3 id='heading--expert'>🎓 Expert</h3>

Expert is for expert use only. It allowes to change and tweak all possible configuration parameters on VESC. Both motor configuration and app configuration. It automatically detects all VESCs connected via CAN bus so you can switch between them and change settings. There is a super convenient omnibox to easily search what you want to change

<img src="https://rpasichnyk.github.io/metr-guide/expert-change.mov.gif" width="320">

It is also possible to do motor detection (both BLDC and FOC) in Expert. Click menu → Detect motor

<img src="https://rpasichnyk.github.io/metr-guide/expert-detect.mov.gif" width="320">

Metr app fetches motor and app configuration every time connection is made with Metr Pro and saves a backup. To check history of changes click menu → History.

<img src="https://rpasichnyk.github.io/metr-guide/expert-history.mov.gif" width="320">

For DieBieMS / FlexiBMS too!

<img src="https://rpasichnyk.github.io/metr-guide/expert-historybms.mov.gif" width="320">

<h4 id='heading--discharger'>⚡️ Discharger</h4>

You want to discharge battery pack in some cases, for example before winter. Storing battery discharged will increase its longevity. Sometimes you think about it too late and the weather is already bad to discharge the normal way. Fortunately there is a feature in metr app to help with that. To use discharger, open Expert tab, click menu → Discharger

<img src="https://rpasichnyk.github.io/metr-guide/discharger.mov.gif" width="320">

It uses `foc_openloop` command to discharge battery. Battery current goes through motors, but they are not spinning, just heating.

⏱ Takes several hours to discharge a battery  
🌱 Quiet and about 5x faster than freespin  
🔢 Uses multiple VESCs/motors over CAN bus  
📈 Continuously sends `COMM_ALIVE` packets and monitors realtime data  
🔥 Motor temperature limit 60℃, VESC temperature limit 70℃  
✅ Turns off when reached storage level  

<h3 id='heading--announcements'>📣 Announcements</h3>

Announcements is a very useful feature that literally tells you realtime data without you having to look at it.

<img src="https://rpasichnyk.github.io/metr-guide/announce.png" width="400">

You can customize which kind of data you want to hear and how often.

<h3 id='heading--settings'>⚙️ Settings</h3>

Very importaint, make sure motor settings are configured correctly

<img src="https://rpasichnyk.github.io/metr-guide/settings-motor.png" width="400">

It is recommended to enable Location

<img src="https://rpasichnyk.github.io/metr-guide/settings-location.png" width="400">

and Notifications

<img src="https://rpasichnyk.github.io/metr-guide/settings-notifications.png" width="400">

To switch between metric and imperial go to Settings → Miscellaneous

<img src="https://rpasichnyk.github.io/metr-guide/settings-metric-app.mov.gif" width="320">

And when viewing a record in a browser

<img src="https://rpasichnyk.github.io/metr-guide/settings-metric-web.mov.gif" width="500">

<h3 id='heading--tcpbridge'>🌉 TCP Bridge</h3>

Connect to Metr Pro and start TCP Bridge from Settings tab

<img src="https://rpasichnyk.github.io/metr-guide/tcpbridge.mov.gif" width="320">

Then open VESC Tool and use the same IP address

<img src="https://rpasichnyk.github.io/metr-guide/tcpbridge-vesc_tool.png" width="400">

<h3 id='heading--overlay'>🔢 Overlay</h3>
An easy way to add telemetry to your videos. You can film the video with the camera of your choice and record the telemetry data separately with the metr app. Then you combine them together.

<img src="https://rpasichnyk.github.io/metr-guide/overlayvirb.mp4.gif" width="500">

Get [GARMIN VIRB® Edit](https://buy.garmin.com/en-US/US/p/573412)  
Open your record in the browser and add `?format=fit` in the address bar. Wait until telemetry file is downloaded

<img src="https://rpasichnyk.github.io/metr-guide/formatfit.mp4.gif" width="500">

Start GARMIN VIRB® Edit and import your video  
Click Import G-Metrix and use the .fit file that you downloaded  

<h3 id='heading--diebiems'>🔋 DieBieMS</h3>

[DieBieMS](https://github.com/DieBieEngineering/DieBieMS) is a smart BMS (Battery Management System). If you have DieBieMS connected via CAN bus it will be automatically detected in the Metr App (no extra setup is needed). DieBieMS provides such information as individual cell voltages and state of charge / discharge, consumption based battery percent data.

To see individual cell voltages, click Battery percent cell on the Realtime page.

<img src="https://rpasichnyk.github.io/metr-guide/diebie-showcells.png" width="400">

When you plug in the charger, DieBieMS view will automatically open and show charging current / balancing state. Glowing dots on the cells mean they are balancing at the moment.

<img src="https://rpasichnyk.github.io/metr-guide/diebie-charging.mp4.gif" width="320">

It is possible to configure DieBieMS through the Metr App. When you open Expert page, DieBieMS shows up and you can read / write settings. This is a quick and convenient way to change some settings when you are on the go and don't have access to full DieBieMS Tool.

<img src="https://rpasichnyk.github.io/metr-guide/diebie-expert.mp4.gif" width="320">

<h3 id='heading--flexibms'>🔋 FlexiBMS</h3>

[FlexiBMS](https://github.com/SimosMCmuffin/FlexiBMS_Lite_FW) is similar to DieBieMS except it is a charge-only BMS. Please read the previous section [DieBieMS](#heading--diebiems).

<h3 id='heading--lltbms'>🔋 LLT BMS</h3>

<img src="https://rpasichnyk.github.io/metr-guide/lltbms.jpg" width="400">

[LLT BMS](https://www.lithiumbatterypcb.com/product-category/smart-bms/) comes with it's own BLE module instead of CAN bus. It is possible to pair Metr Pro with LLT BMS using following steps:

1. Make sure you are connected to Metr Pro
2. Navigate to Settings → Battery

<img src="https://rpasichnyk.github.io/metr-guide/lltbms-settings.png" width="400">

3. Click on "Pair with BMS"

<img src="https://rpasichnyk.github.io/metr-guide/lltbms-pair.png" width="400">

4. Select LLT BMS
5. Go back to Realtime tab and click on Battery percent cell. You should see cell information

<img src="https://rpasichnyk.github.io/metr-guide/lltbms-view.png" width="400">


<h3 id='heading--troubleshooting'>🛠 Troubleshooting</h3>

A good advice is to search for information on [esk8.builders forum](https://www.electric-skateboard.builders) and [esk8.news forum](https://forum.esk8.news). Maybe you will find the solution.

If you didn't find anything relevant, could be that you found a bug! The bugs are always there🐛 and once in a while a new one pops out. If you want to report it, please collect the log file from the app. Open Settings and click on "Show Logs" button. Send log file toghether with the bug description, screenshots or video. Log file resets every day so don't forget to collect it after you experienced the problem.

<img src="https://rpasichnyk.github.io/metr-guide/showlogs.png" width="400">

<br/>
<br/>
<br/>

This guide is written in [Markdown](https://en.wikipedia.org/wiki/Markdown) and is available at

[GitHub](https://rpasichnyk.github.io/metr-guide/) (contributions welcome)  
[forum.esk8.news](https://forum.esk8.news/t/the-definitive-guide-to-metr-app-metr-pro) (ask your questions here)
