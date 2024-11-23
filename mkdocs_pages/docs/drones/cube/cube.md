# Куб

CUAV V5+ Autopilot Pixhack PX4 APM Flight Controller

![](CUAV V5+.jpg){: style="width:50%"}

<image >
# Прошивка

ArduPilot 4.5.7

## WiFi

ssid: DroneBridge ESP32
pass: 12345678

## Frame class and type

Setup -> Mandatory Hardware -> Frame Type -> X

## GPS

<span style="color:red">Настроить до калибровки компаса!</span>

[NEO 3 Pro GPS](../../settings/equipment/GPS/NEO_3_Pro_GPS.md)

## OLED Dosplay

NTF_DISPLAY_TYPE:1 (ssd1306)

<span style="color:red">**требуется перезагрузка!**</span>

## Compass

Setup -> Mandatory Hardware -> Compass

## Accel Clibration

Setup -> Mandatory Hardware -> Accel Clibration -> Calibrate Accel

<span style="color:red">**требуется перезагрузка!**</span>

## Gyro

Setup -> Mandatory Hardware -> Accel Clibration -> Calibrate Level

## Battery Monitor

Setup -> Mandatory Hardware ->  Initial Tune Params

Airscrew size in inch: 10 (размер пропа в дюймах)
Battery cell count: 3

Нажать кнопку "Calculate"

После чего программа расчитает следующие параметры и предложит записать их в полётный контроллер:

* [ATC_ACCEL_P_MAX](https://ardupilot.org/copter/docs/parameters.html#atc-accel-p-max-acceleration-max-for-pitch): Acceleration Max for Pitch
* [ATC_ACCEL_R_MAX](https://ardupilot.org/copter/docs/parameters.html#atc-accel-r-max-acceleration-max-for-roll): Acceleration Max for Roll
* [ATC_RAT_PIT_FLTD](https://ardupilot.org/copter/docs/parameters.html#atc-rat-pit-fltd-ac-attitudecontrol-multi-pitch-axis-rate-controller-derivative-frequency-in-hz) (AC_AttitudeControl_Multi): Pitch axis rate controller derivative frequency in Hz
* [ATC_RAT_PIT_FLTT](https://ardupilot.org/copter/docs/parameters.html#atc-rat-pit-fltt-ac-attitudecontrol-heli-pitch-axis-rate-controller-target-frequency-in-hz) (AC_AttitudeControl_Heli): Pitch axis rate controller target frequency in Hz
* [ATC_RAT_RLL_FLTD](https://ardupilot.org/copter/docs/parameters.html#atc-rat-rll-fltd-ac-attitudecontrol-multi-roll-axis-rate-controller-derivative-frequency-in-hz) (AC_AttitudeControl_Multi): Roll axis rate controller derivative frequency in Hz
* [ATC_RAT_RLL_FLTT](https://ardupilot.org/copter/docs/parameters.html#atc-rat-rll-fltt-ac-attitudecontrol-heli-roll-axis-rate-controller-target-frequency-in-hz) (AC_AttitudeControl_Heli): Roll axis rate controller target frequency in Hz
* [ATC_RAT_YAW_FLTD](https://ardupilot.org/copter/docs/parameters.html#atc-rat-yaw-fltd-ac-attitudecontrol-heli-yaw-axis-rate-controller-derivative-frequency-in-hz) (AC_AttitudeControl_Heli): Yaw axis rate controller derivative frequency in Hz
* [ATC_RAT_YAW_FLTE](https://ardupilot.org/copter/docs/parameters.html#atc-rat-yaw-flte-ac-attitudecontrol-heli-yaw-axis-rate-controller-error-frequency-in-hz) (AC_AttitudeControl_Heli): Yaw axis rate controller error frequency in Hz
* [ATC_RAT_YAW_FLTT](https://ardupilot.org/copter/docs/parameters.html#atc-rat-yaw-fltt-ac-attitudecontrol-multi-yaw-axis-rate-controller-target-frequency-in-hz) (AC_AttitudeControl_Multi): Yaw axis rate controller target frequency in Hz
* [BATT_ARM_VOLT](https://ardupilot.org/copter/docs/parameters.html#batt-arm-volt-required-arming-voltage): Required arming voltage
* [BATT_CRT_VOLT](https://ardupilot.org/copter/docs/parameters.html#batt-crt-volt-critical-battery-voltage): Critical battery voltage
* [BATT_LOW_VOLT](https://ardupilot.org/copter/docs/parameters.html#batt-low-mah-low-battery-capacity): Low battery voltage
* [INS_ACCEL_FILTER](https://ardupilot.org/copter/docs/parameters.html#ins-accel-filter-accel-filter-cutoff-frequency): Accel filter cutoff frequency
* [INS_GYRO_FILTER](https://ardupilot.org/copter/docs/parameters.html#ins-gyro-filter-gyro-filter-cutoff-frequency): Gyro filter cutoff frequency
* [MOT_BAT_VOLT_MAX](https://ardupilot.org/copter/docs/parameters.html#mot-bat-volt-max-battery-voltage-compensation-maximum-voltage): Battery voltage compensation maximum voltage
* [MOT_BAT_VOLT_MIN](https://ardupilot.org/copter/docs/parameters.html#mot-bat-volt-min-battery-voltage-compensation-minimum-voltage): Battery voltage compensation minimum voltage
* [MOT_THST_EXPO](https://ardupilot.org/copter/docs/parameters.html#mot-thst-expo-thrust-curve-expo): Thrust Curve Expo
* [MOT_THST_HOVER](https://ardupilot.org/copter/docs/parameters.html#mot-thst-hover-thrust-hover-value): Thrust Hover Value

## Initial Tune Params
