# Android串口示例

本项目提供了一个用于在Android设备上进行串口通信的Java API。

## 概述

Android串口API允许直接与Android设备上的串口进行通信。该API对于需要串口通信的应用程序至关重要，通常用于嵌入式系统、工业自动化及其他硬件接口应用。

## 项目归档

原始项目可以在Google Code Archive中找到：
- [Android Serial Port API - Google Code Archive](https://code.google.com/archive/p/android-serialport-api/)

### 下载源码

在此下载源码归档：
- [source-archive.zip](source-archive.zip)

## 设置与配置

要在Android模拟器中启用串口支持，请使用以下命令：

```bash
emulator.exe -avd Pixel_3_API_28 -writable-system -qemu -serial COM2 -no-snapshot-load
```

模拟器启动后，按照以下步骤配置设备以进行串口通信：

1. 以root身份启动ADB：
   ```bash
   adb root
   ```

2. 设置SELinux为宽松模式：
   ```bash
   adb shell setenforce 0
   ```

3. 调整串口的权限：
   ```bash
   adb shell chmod 666 /dev/ttyS1
   ```