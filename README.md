#  PlatformIO + ESP32 + Azure IoT Arduino demo

# Description

This is a PlatformIO compilable version of the [azure-iot-arduino](https://github.com/Azure/azure-iot-arduino) repository for ESP32. Please refer to this repository for its documentation of samples and configuration options of the Azure IoT SDK et cetera. 

# PlatformIO configs

See `platformio.ini`. Currently, the [platform.local.txt](https://github.com/Azure/azure-iot-arduino/blob/master/examples/esp32/iothub_ll_telemetry_sample/platform.local.txt) is replicated by using `build_flags`. These build flags currently select `-DDONT_USE_UPLOADTOBLOB -DUSE_BALTIMORE_CERT -DUSE_MBEDTLS`. 

# Switching certificates 

Replace `-DUSE_BALTIMORE_CERT` with other defines, as can be found in [the certs.c](https://github.com/Azure/azure-iot-arduino/blob/master/src/certs/certs.c) file of the AzureIoTHub library.