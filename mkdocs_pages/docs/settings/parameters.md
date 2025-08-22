# Complete Parameter List

[Complete Parameter List](https://ardupilot.org/copter/docs/parameters.html)

## AHRS

**Attitude Heading Reference System** (AHRS)

Системы определения положения и ориентации для определения положения, курса и местоположения.

## PSC

**Position Controller** (SC)

Those parameters set how the vehicle responds to navigation commands (for example to make it more aggressive).

## ATC

**Attitude Control (ATC)**

## HUD

**HUD (Head-Up Display)** — это индикатор на лобовом стекле.

Это прозрачный дисплей, который проецирует самую важную летную и боевую информацию прямо на стекло кабины пилота. Его главная цель — позволить пилоту получать критически важные данные, не опуская голову и не отводя глаз от воздушной обстановки и цели.

Основные элементы на HUD:

* Искусственный горизонт: Показывает крен и тангаж самолета относительно земли.
* Скорость (AirSpeed): Текущая воздушная скорость.
* Высота (Altitude): Высота полета.
* Курс (Heading): Направление полета.
* Угол атаки (AoA - Angle of Attack): Критически важен для взлета и посадки.
* Вектор скорости (Velocity Vector / Flight Path Marker): Показывает, куда на самом деле летит самолет (его фактическую траекторию).

## PILOT_ACCEL_Z: Pilot vertical acceleration

[PILOT_ACCEL_Z](https://ardupilot.org/copter/docs/parameters.html#pilot-accel-z-pilot-vertical-acceleration)

## PILOT_SPEED_UP: Pilot maximum vertical speed ascending

[PILOT_SPEED_UP](https://ardupilot.org/copter/docs/parameters.html#pilot-speed-up)

The maximum vertical ascending velocity the pilot may request in cm/s

## PILOT_SPEED_DN: Pilot maximum vertical speed descending

[PILOT_SPEED_DN](https://ardupilot.org/copter/docs/parameters.html#pilot-speed-dn)

The maximum vertical descending velocity the pilot may request in cm/s.  If 0 PILOT_SPEED_UP value is used.

> Не работает в режиме Stabilize

## LAND_SPEED: Land speed

[LAND_SPEED](https://ardupilot.org/copter/docs/parameters.html#land-speed-land-speed)

The descent speed for the final stage of landing in cm/s

| Increment | Range     | Units                  |
| --------- | --------- | ---------------------- |
| 10        | 30 to 200 | centimeters per second |

## LAND_SPEED_HIGH: Land speed high

[LAND_SPEED_HIGH](https://ardupilot.org/copter/docs/parameters.html#land-speed-high-land-speed-high)

The descent speed for the first stage of landing in cm/s. If this is zero then WPNAV_SPEED_DN is used

| Increment | Range    | Units                  |
| --------- | -------- | ---------------------- |
| 10        | 0 to 500 | centimeters per second |
