## Contents

[Realtime](#realtime-page)  
[Modes](#modes)  
[Records](#records)  
[Faults](#faults)  
[Expert](#expert)  
[Announcements](#announcements)  
[Settings](#settings)  
[Overlay](#overlay)  
[DieBieMS](#diebiems)  



### Realtime Page

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

![|320x482,75%](https://rpasichnyk.github.io/metr-guide/realtime1.mov.gif)

There is an indicator in the bottom which shows currently selected BLE module and connection status, ESC hardware name and firmware version. It blinks every time new packet from VESC is received.

![|300x68,75%](https://rpasichnyk.github.io/metr-guide/status1.mov.gif)

### Modes
TBD
### Records
TBD
### Faults
TBD
### Expert
TBD
### Announcements
TBD
### Settings
TBD

### DieBieMS

[DieBieMS](https://github.com/DieBieEngineering/DieBieMS) is a smart BMS (Battery Management System). If you have DieBieMS connected via CAN bus it will be automatically detected in the Metr App. DieBieMS provides such information as individual cell voltages and state of charge / discharge, consumption based battery percent data.

No extra setup is needed in the Metr App, DieBieMS 
To see individual cell voltages, click Battery percent cell on the Realtime page.

When you plug in the charger, DieBieMS view will automatically open and show charging current / balancing state. Glowing dots on the cells mean they are balancing at the moment.

### Overlay

An easy way to add telemetry to your videos. You can film the video with the camera of your choice and record the telemetry data separately with the metr app. Then you combine them together.

![|600x450,50%](https://rpasichnyk.github.io/metr-guide/overlayvirb.mp4.gif)

Get [GARMIN VIRB® Edit](https://buy.garmin.com/en-US/US/p/573412)  
Open your record in the browser and add `?format=fit` in the address bar. Wait until telemetry file is downloaded

![|600x423,50%](https://rpasichnyk.github.io/metr-guide/formatfit.mp4.gif)

Start GARMIN VIRB® Edit and import your video  
Click Import G-Metrix and use the .fit file that you downloaded  


##  
##  
##  

This guide is written in [Markdown](https://en.wikipedia.org/wiki/Markdown) and is available at

[GitHub](https://rpasichnyk.github.io/metr-guide/)  
[forum.esk8.news](https://forum.esk8.news/t/the-definitive-guide-to-metr-app) (ask your questions here)
