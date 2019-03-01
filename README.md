# Jia's Fork of DXU Firmware

This is my modification of the [DXU](https://github.com/yyh1002/DXU)'s firmware from yyh1002's dual extruder design for Ultimaker 2+.
Following are the changes so far:

* Integrated Tinkergnome 18.10
* Made configuration changes for DWMaker Extended
  * Change Z range to 305
  * Change max temperature to 290
  * Change max bed temperature to 135
  * Lower max acc to ~~1700.0~~ 2000.0
  * Lower max jerk to 10.0
  * Lower bang-bang check interval to 4s
  * Limited Y axis to 222 for metal slider block.
  * Adjust all material diameter to 1.75.
* Ported the retraction after insert material from the original firmware.
* Port User Function from Marlin for preheat chamber etc...
* Add temperature hysteresis to the fan on/off logic.
* Introduce T flag for M301 command for choosing PID setting.
* Optimize tool change behavior.
* Print tinkergnome related settings
* Porting marlin PR#2432 for higher temperature
* Restore PID filter back to 0.95 for quicker response.
* Make M500 and M501 store/restore tinkergnome settings as well.