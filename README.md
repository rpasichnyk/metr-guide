[Metr App](https://metr.at) is probably™️ the most advanced telemetry app for electric skateboards. As amount of features continued to grow over the years the time has come for the proper guide to explain the basics and some hidden secrets in the app.

This guide will be improving over time and hopefully some day will cover everything the app has to offer. Before you start reading there are two very important things you need to know. In order to use it you must have:

* [VESC®](https://vesc-project.com)-based controller
* [Metr Pro](https://metr.at/shop) bluetooth module

If you scateboard has another controller, the app will not work for you. For example Meepo, WowGo, Backfire have another type of controller and are not compatible.


### Contents

[First time setup](#heading--firsttime)  
[Realtime](#heading--realtime)  
[Modes](#heading--modes)  
[Records](#heading--records)  
[Faults](#heading--faults)  
[Expert](#heading--expert)  
[Announcements](#heading--announcements)  
[Settings](#heading--settings)  
[Overlay](#heading--overlay)  
[DieBieMS](#heading--diebiems)  
[Troubleshooting](#heading--troubleshooting)  

<h3 id='firsttime'>🐣 First time setup</h3>

Follow the instructions at [metr.at/setup](https://metr.at/setup)

<h3 id='realtime'>📈 Realtime</h3>

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

<img src="https://rpasichnyk.github.io/metr-guide/realtime1.mp4.gif" width="330">

There is an indicator in the bottom which shows currently selected BLE module and connection status, ESC hardware name and firmware version. It blinks every time new packet from VESC is received.

<img src="https://rpasichnyk.github.io/metr-guide/status1.mp4.gif" width="220">

<h3 id='heading--modes'>🐌 Modes</h3>
TBD
<h3 id='heading--records'>⏺ Records</h3>
TBD  
To export raw JSON data open your record in the browser and add `?format=json` in the address bar.
<h3 id='heading--faults'>🛑 Faults</h3>
TBD
<h3 id='heading--expert'>🎓 Expert</h3>
TBD
<h3 id='heading--announcements'>📣 Announcements</h3>
TBD
<h3 id='heading--settings'>⚙️ Settings</h3>
TBD
<h3 id='heading--overlay'>🔢 Overlay</h3>
An easy way to add telemetry to your videos. You can film the video with the camera of your choice and record the telemetry data separately with the metr app. Then you combine them together.

<img src="https://rpasichnyk.github.io/metr-guide/overlayvirb.mp4.gif" width="500">

Get [GARMIN VIRB® Edit](https://buy.garmin.com/en-US/US/p/573412)  
Open your record in the browser and add `?format=fit` in the address bar. Wait until telemetry file is downloaded

<img src="https://rpasichnyk.github.io/metr-guide/formatfit.mp4.gif" width="500">

Start GARMIN VIRB® Edit and import your video  
Click Import G-Metrix and use the .fit file that you downloaded  

<h3 id='heading--diebiems'>🔋 DieBieMS</h3>

[DieBieMS](https://github.com/DieBieEngineering/DieBieMS) is a smart BMS (Battery Management System). If you have DieBieMS connected via CAN bus it will be automatically detected in the Metr App. DieBieMS provides such information as individual cell voltages and state of charge / discharge, consumption based battery percent data.

No extra setup is needed in the Metr App, DieBieMS 
To see individual cell voltages, click Battery percent cell on the Realtime page.

When you plug in the charger, DieBieMS view will automatically open and show charging current / balancing state. Glowing dots on the cells mean they are balancing at the moment.

<h3 id='heading--troubleshooting'>🛠 Troubleshooting</h3>

A good advice is to search for information on [esk8.builders forum](https://www.electric-skateboard.builders) and [esk8.news forum](https://forum.esk8.news). Maybe you will find the solution.

If you didn't find anything relevant, could be that you found a bug! The bugs are always there🐛 and once in a while a new one pops out. If you want to report it, please collect the log file from the app. Open Settings and click on "Show Logs" button. Send log file toghether with the bug description, screenshots or video. Log file resets every day so don't forget to collect it after you experienced the problem.

<img src="https://rpasichnyk.github.io/metr-guide/showlogs.png" width="400">

<br/>
<br/>
<br/>

This guide is written in [Markdown](https://en.wikipedia.org/wiki/Markdown) and is available at

[GitHub](https://rpasichnyk.github.io/metr-guide/) (contributions welcome)  
[forum.esk8.news](https://forum.esk8.news/t/the-definitive-guide-to-metr-app) (ask your questions here)
