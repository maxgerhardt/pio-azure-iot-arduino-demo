#  PlatformIO + ESP32 + Azure IoT Arduino demo

# Description

This is a PlatformIO compilable version of the [azure-iot-arduino](https://github.com/Azure/azure-iot-arduino) repository for ESP32. Please refer to this repository for its documentation of samples and configuration options of the Azure IoT SDK et cetera. 

# PlatformIO configs

See `platformio.ini`. Currently, the [platform.local.txt](https://github.com/Azure/azure-iot-arduino/blob/master/examples/esp32/iothub_ll_telemetry_sample/platform.local.txt) is replicated by using `build_flags`. These build flags currently select `-DDONT_USE_UPLOADTOBLOB -DUSE_BALTIMORE_CERT -DUSE_MBEDTLS`. 

# Switching certificates 

Replace `-DUSE_BALTIMORE_CERT` with other defines, as can be found in [the certs.c](https://github.com/Azure/azure-iot-arduino/blob/master/src/certs/certs.c) file of the AzureIoTHub library.

# Compiling 

Simply clone the project and run `pio run` on it. If you've only installed PlatformIO as a VSCode plugin, use the PlatformIO home screen plus the "Open Project" button to simply open the project. Compilation should result in 


```
Advanced Memory Usage is available via "PlatformIO Home > Project Inspect"
RAM:   [=         ]  12.1% (used 39712 bytes from 327680 bytes)
Flash: [=======   ]  69.1% (used 905311 bytes from 1310720 bytes)
esptool.py v2.6
===================================== [SUCCESS] Took 24.58 seconds =====================================
```