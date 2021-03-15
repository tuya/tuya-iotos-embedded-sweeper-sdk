# 涂鸦嵌入式扫地机 SDK

## 介绍

涂鸦扫地机 SDK 是基于涂鸦 IoTOS 系统针对扫地机设备的软件开发包。该 SDK 封装了设备与涂鸦云，涂鸦APP的通信，以及针对扫地机设备的所需要的接口。开发者不需要关心通信层的实现，专注于其业务开发。

* 支持 WIFI 或 蓝牙配网。
* 提供标准的 C 语言库，头文件，以及文档说明。
* 提供丰富的针对扫地机业务的 API 接口。
* 用此 SDK 开发基于 LINUX 平台的扫地机产品。

## 快速上手

  从仓库目录 **Library/<SDK 版本>** 下根据工具链下载 SDK 开发包。如果该目录下没有所需要平台的 SDK ，请联系涂鸦服务人员或工单，提供工具链，涂鸦会及时上传其所需的 SDK 开发包。


## SDK 目录接口

```
├── build_app.sh
├── CHANGELOG.md
├── demos
│   └── demo_soc_dev_wifi
│       ├── include
│       ├── Makefile
│       └── src
│           ├── tuya_iot_soc_dev_entry.c
│           └── tuya_iot_wifi_net.c
├── platforms
├── README.md
└── sdk
    ├── include
    │   ├── aes_inf.h
    │   ├── cJSON.h
    │   ├── hal
    │   │   ├── driver
    │   │   │   ├── tuya_hal_bt.h
    │   │   │   ├── tuya_hal_i2c.h
    │   │   │   ├── tuya_hal_rtc.h
    │   │   │   ├── tuya_hal_storge.h
    │   │   │   ├── tuya_hal_wifi.h
    │   │   │   └── tuya_hal_wired.h
    │   │   ├── system
    │   │   │   ├── tuya_hal_fs.h
    │   │   │   ├── tuya_hal_memory.h
    │   │   │   ├── tuya_hal_mutex.h
    │   │   │   ├── tuya_hal_network.h
    │   │   │   ├── tuya_hal_output.h
    │   │   │   ├── tuya_hal_semaphore.h
    │   │   │   ├── tuya_hal_system.h
    │   │   │   └── tuya_hal_thread.h
    │   │   ├── tuya_os_adapter_error_code.h
    │   │   └── tuya_os_adapter.h
    │   ├── mem_pool.h
    │   ├── mix_method.h
    │   ├── tuya_cloud_com_defs.h
    │   ├── tuya_cloud_error_code.h
    │   ├── tuya_cloud_types.h
    │   ├── tuya_cloud_wifi_defs.h
    │   ├── tuya_iot_com_api.h
    │   ├── tuya_iot_config.h
    │   ├── tuya_iot_sweeper_api.h
    │   ├── tuya_iot_wifi_api.h
    │   ├── ty_cJSON.h
    │   ├── uni_log.h
    │   ├── uni_network.h
    │   ├── uni_queue.h
    │   ├── uni_thread.h
    │   └── uni_time.h
    └── lib
        ├── libtuya_iot.a
        └── libtuya_iot.a.stripped
```

开发者需要适配 WIFI hal接口，接口路径为 demos/src/tuya_iot_wifi_net.c 。

SDK 路径下 lib 为 SDK 静态库， include 目录为头文件路径，这些添加到开发者项目中。

### 编译 demo

 ```
    ./build_app.sh demos/demo_soc_dev_wifi/ demo_soc_dev_wifi 1.0.0
 ```

在 output 下会生成扫地机应用程序。

## 版本变更记录
查看该仓库 Library/<SDK 版本>/iot_release_note.txt

## 技术支持

您可以通过以下方法获得涂鸦的支持:
- 开发者中心：https://developer.tuya.com/cn/
- 帮助中心: https://support.tuya.com/en/help
- 技术支持工单中心: [https://service.console.tuya.com](https://service.console.tuya.com/)