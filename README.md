# Driver samples for Windows 11

These are the official Microsoft Windows Driver Kit (WDK) driver code samples for Windows 11. They provide a foundation for Universal Windows driver support of all hardware form factors, from phones to desktop PCs. Use these samples with Visual Studio 2022 and Windows Driver Kit (WDK) 11.

[Windows Driver Kit documentation](https://docs.microsoft.com/windows-hardware/drivers/)

## Windows 11 driver development

Use Visual Studio 2022 and Windows Driver Kit (WDK) 11 to build, test, and deploy your drivers. With Windows 11, the driver development environment is integrated into Visual Studio. To get started, download the driver development kits and tools for Windows 11.

[Download the WDK, WinDbg, and associated tools](https://developer.microsoft.com/windows/hardware/windows-driver-kit)

### Windows Driver Kit (WDK)

Take a look at the compilation of the new and changed driver-related content for Windows 11. Areas of improvement include camera, print, display, Near Field Communication (NFC), WLAN, Bluetooth, and more.

[Find out what's new in the WDK](https://docs.microsoft.com/windows-hardware/drivers/what-s-new-in-driver-development)

### Universal Windows drivers

Write one driver that runs on Windows 11 for desktop editions, as well as other Windows editions that share a common set of interfaces.

[Getting Started with Universal Windows drivers](https://docs.microsoft.com/windows-hardware/drivers/develop/getting-started-with-universal-drivers)

### Windows Driver Frameworks

The Windows Driver Frameworks (WDF) are a set of libraries that make it simple to write high-quality device drivers.

[WDF driver development guide](https://docs.microsoft.com/windows-hardware/drivers/wdf/)

### Samples

Use the samples in this repo to guide your Windows driver development. Whether you're just getting started or porting an older driver to the newest version of Windows, code samples are valuable guides on how to write drivers.

For information about important changes that need to be made to the WDK sample drivers before releasing device drivers based on the sample code, see the following topic:

[From Sample Code to Production Driver - What to Change in the Samples](https://docs.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/from-sample-code-to-production-driver)

### Build your first driver

If you're writing your first driver, use these exercises to get started. Each exercise is independent of the others, so you can do them in any order.

[Write a UMDF driver based on a template](https://docs.microsoft.com/windows-hardware/drivers/gettingstarted/writing-a-umdf-driver-based-on-a-template)

[Write a KMDF Hello World driver](https://docs.microsoft.com/windows-hardware/drivers/gettingstarted/writing-a-very-small-kmdf--driver)

[Write a KMDF driver based on a template](https://docs.microsoft.com/windows-hardware/drivers/gettingstarted/writing-a-kmdf-driver-based-on-a-template)

[Use GitHub Actions to build a simple driver project](.github/Build-with-GitHub.md)

# Microsoft Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
这是微软官方的 Windows-driver-samples 仓库，是学习 Windows 驱动开发最权威的起点。
一、仓库核心信息

• 官方性：由微软官方维护，代码质量和兼容性有保障。

• 用途：提供与 Visual Studio 和 Windows 驱动工具包 (WDK) 配合使用的驱动示例代码，覆盖从简单到复杂的各种驱动类型。

• 适配性：支持通用 Windows 驱动和桌面专用驱动，可用于从手机到桌面 PC 的各种硬件平台。

二、图中目录分类与用途

从截图可见，该仓库按驱动类型进行了清晰的目录划分：

• .github：GitHub 相关配置文件，如 CI/CD 工作流。

• TrEE：与 TPM（可信平台模块）相关的驱动示例。

• audio：音频设备驱动示例，如声卡驱动。

• avstream：音视频流驱动示例，用于多媒体设备。

• bluetooth：蓝牙设备驱动示例。

• filesys：文件系统驱动示例，包括传统文件系统和过滤驱动。

• general：通用驱动示例，包含你最关心的 Minifilter 驱动模板（如 passThrough、scanner 等），是学习文件系统过滤的最佳入口。

• gnss：全球导航卫星系统驱动示例，如 GPS。

• gpio/samples：通用输入输出引脚驱动示例。

• hid：人体学输入设备驱动示例，如键盘、鼠标。

三、针对你的学习建议

1. Minifilter 入门：直接进入 general/minifilters 目录，这里有官方提供的最简模板，如 passThrough，可以直接编译运行，观察文件操作拦截效果。

2. 编译环境：确保安装了匹配 Windows 版本的 Visual Studio 和 WDK，然后打开对应 .sln 工程文件进行编译。

3. 调试与测试：使用 fltmc 命令加载编译好的 Minifilter 驱动，并通过 ProcMon 等工具验证其行为。
