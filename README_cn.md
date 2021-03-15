# 涂鸦嵌入式扫地机 SDK

## 介绍

涂鸦扫地机 SDK 是基于涂鸦 IoTOS 系统针对扫地机设备的软件开发包。该 SDK 封装了设备与涂鸦云，涂鸦APP的通信，以及针对扫地机设备的所需要的接口。开发者不需要关心通信层的实现，专注于其业务开发。

* 支持 WIFI 或 蓝牙配网。
* 提供标准的 C 语言库，头文件，以及文档说明。
* 提供丰富的针对扫地机业务的 API 接口。
* 用此 SDK 开发基于 LINUX 平台的扫地机产品。

## 快速上手

  从仓库目录 **Library/<SDK 版本>** 下根据工具链下载 SDK 开发包。如果该目录下没有所需要平台的 SDK ，请联系涂鸦服务人员，提供工具链，涂鸦会及时上传其所需的 SDK 开发包。

  开发者需要适配 WIFI hal 接口。 适配接口位于 demos 下的 tuya_iot_wifi_net.c 中的函数簇。

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