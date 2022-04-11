set(srcs
    "./src/common/foc_utils.cpp"
    "./src/common/time_utils.cpp"
    "./src/common/pid.cpp"
    "./src/common/lowpass_filter.cpp"
    "./src/common/base_classes/Sensor.cpp"
    "./src/common/base_classes/CurrentSense.cpp"
    "./src/common/base_classes/FOCMotor.cpp"
    

    "./src/drivers/hardware_specific/esp32_mcu.cpp"
    "./src/drivers/BLDCDriver3PWM.cpp"
    "./src/BLDCMotor.cpp"
    "./src/sensors/MagneticSensorSPI.cpp"
    )

set(includes "./src/common"
             "./src/common/base_classes"
             "./src/drivers"
             "./src/"
             "./src/sensors"
                )

idf_component_register(SRCS "${srcs}"
                    INCLUDE_DIRS ${includes}
                    REQUIRES arduino-esp32)

