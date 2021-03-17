# Tuya Embedded Sweeper SDK

[English](README.md) | [中文版](README_cn.md)

## Overview

Tuya Sweeper SDK is a software development kit for sweepers based on Tuya IoTOS system. The SDK encapsulates the communication between the device, the Tuya IoT Platform, and Tuya apps, as well as the required APIs for the sweepers. You do not need to care about the implementation of the communication layer, but focus on the development.

* Support pairing through Wi-Fi or Bluetooth.
* Provide standard C language library, header files, and documentation.
* Provide abundant APIs for the sweepers.
* Develop sweeper products for the Linux platform by using this SDK.

## Get started

Download the SDK from the repository directory **Library/<SDK version>** according to the tool chain. If there is no SDK for the required platform in this directory, please provide the tool chain for Tuya customer service or submit a technical ticket. Tuya will upload the required SDK timely.


## SDK directory

```
├── build_app.sh
├── CHANGELOG.md
├── demos
│   └── demo_soc_dev_wifi
│       ├── include
│       ├── Makefile
│       └── src
│           ├── tuya_iot_soc_dev_entry.c
│           └── tuya_iot_wifi_net.c
├── platforms
├── README.md
└── sdk
    ├── include
    │   ├── aes_inf.h
    │   ├── cJSON.h
    │   ├── hal
    │   │   ├── driver
    │   │   │   ├── tuya_hal_bt.h
    │   │   │   ├── tuya_hal_i2c.h
    │   │   │   ├── tuya_hal_rtc.h
    │   │   │   ├── tuya_hal_storge.h
    │   │   │   ├── tuya_hal_wifi.h
    │   │   │   └── tuya_hal_wired.h
    │   │   ├── system
    │   │   │   ├── tuya_hal_fs.h
    │   │   │   ├── tuya_hal_memory.h
    │   │   │   ├── tuya_hal_mutex.h
    │   │   │   ├── tuya_hal_network.h
    │   │   │   ├── tuya_hal_output.h
    │   │   │   ├── tuya_hal_semaphore.h
    │   │   │   ├── tuya_hal_system.h
    │   │   │   └── tuya_hal_thread.h
    │   │   ├── tuya_os_adapter_error_code.h
    │   │   └── tuya_os_adapter.h
    │   ├── mem_pool.h
    │   ├── mix_method.h
    │   ├── tuya_cloud_com_defs.h
    │   ├── tuya_cloud_error_code.h
    │   ├── tuya_cloud_types.h
    │   ├── tuya_cloud_wifi_defs.h
    │   ├── tuya_iot_com_api.h
    │   ├── tuya_iot_config.h
    │   ├── tuya_iot_sweeper_api.h
    │   ├── tuya_iot_wifi_api.h
    │   ├── ty_cJSON.h
    │   ├── uni_log.h
    │   ├── uni_network.h
    │   ├── uni_queue.h
    │   ├── uni_thread.h
    │   └── uni_time.h
    └── lib
        ├── libtuya_iot.a
        └── libtuya_iot.a.stripped
```

You need to adapt to the Wi-Fi `hal` interface. The path is `demos/src/tuya_iot_wifi_net.c`.

The `lib` under the SDK path is the SDK static library, and the `include` directory is the header file path. These are added to the project.

## Build a demo

 ```
    ./build_app.sh demos/demo_soc_dev_wifi/ demo_soc_dev_wifi 1.0.0
 ```
 
 The sweeper application program will be generated in the `output` directory.
 
## Version history

For more information about the version history, see `Library/<SDK version>/iot_release_note.txt` of this repository.

## Support

You can get support from Tuya with the following methods:

- Tuya Developer Webiste:https://developer.tuya.com/en/
- Tuya Smart Help Center: https://support.tuya.com/en/help
- Technical Support Council: https://service.console.tuya.com


