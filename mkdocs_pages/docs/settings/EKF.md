# EKF

* **EK3_ENABLE**: 1
This enables EKF3. Enabling EKF3 only makes the maths run, it does not mean it will be used for flight control. To use it for flight control set AHRS_EKF_TYPE=3. A reboot or restart will need to be performed after changing the value of EK3_ENABLE for it to take effect.
* **AHRS_EKF_TYPE**: 3
This controls which NavEKF Kalman filter version is used for attitude and position estimation