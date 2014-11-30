spark_HC-SR04_ultrasonic_sensor
===============================

Files, code and references for the HC-SR04_ultrasonic_sensor from Dealextreme

Buy it here:
http://www.dx.com/p/hc-sr04-ultrasonic-sensor-distance-measuring-module-133696#.VHr6A6SG9g4

I am using it for Spark Core projects.

You can compile the project using spark-cli:
http://docs.spark.io/cli/


Wiring:

    Spark pin GND --> HC-SR04 GND
    Spark pin VIN --> HC-SR04 VCC !! Spark VIN NOT Spark 3V3 !!
    Spark D2      --> HC-SR04 TRIG
    Spark D4      --> HC-SR04 ECHO

    Also:

    Spark pin D5 --> Green Led anode (+),
    Green Led Cathode (-) --> Spark GND

    Spark pin D6 --> Red Led anode (+),
    Red Led Cathode (-) --> Spark GND

To compile:

    spark cloud compile HC-SR04.ino

To flash it to your core:

  Using cloud:
  spark cloud flash <your-core-id-here> HC-SR04.ino

  Using USB (core must be in dfu mode - http://docs.spark.io/connect/#appendix-dfu-mode-device-firmware-upgrade)
  spark flash <your-core-id-here> HC-SR04.ino


TODO: Separate pulseIn function in a library
