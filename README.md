
# Log打印
通过Type-C USB 可以查看

# 移植代码
因xiaozhi-esp32更新频繁，可自行前往https://github.com/78/xiaozhi-esp32获取代码，并自行移植

# 小智 AI 聊天机器人

BiliBili 视频介绍 [【ESP32+SenseVoice+Qwen72B打造你的AI聊天伴侣！】](https://www.bilibili.com/video/BV11msTenEH3/?share_source=copy_web&vd_source=ee1aafe19d6e60cf22e60a93881faeba)


### MAX98357功放和MSM261S4030H0R 数字麦克风 

```
接线方式可全局搜索“AUDIO_DEVICE_I2S_GPIO_BCLK”即可查看
```
原理图如下：
![原理图图](docs/SCH_2503原理图_00.jpg)

### 搭建开发环境

- Cursor 或 VSCode
- 安装 ESP-IDF 插件，选择 SDK 版本 5.3 或以上
- Ubuntu 比 Windows 更好，编译速度快，也免去驱动问题的困扰

### 配置项目与编译固件

- ESP32 S3 R8，Flash 8MB
- 配置 OTA Version URL 为 `https://api.tenclass.net/xiaozhi/ota/`
- 配置 WebSocket URL 为 `wss://api.tenclass.net/xiaozhi/v1/`
- 配置 WebSocket Access Token 为 `test-token`
- 配置完成后，编译固件


## 配置 Wi-Fi

打开手机 Wi-Fi，连接上设备热点 `Xiaozhi-xxxx` 后，使用浏览器访问 `http://192.168.4.1`，进入配网页面。

选择你的路由器 WiFi，输入密码，点击连接，设备会在 3 秒后自动重启，之后设备会自动连接到路由器。



