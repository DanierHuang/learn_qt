# QT大纲设计
# 第一章 QT简介和安装
Qt 是一个跨平台的 C++ 应用程序开发框架，最初由 Trolltech 公司开发，现在由 The Qt Company 维护。它广泛用于开发图形用户界面（GUI）应用程序，同时也支持非图形用户界面（非 GUI）应用程序的开发。Qt 提供了丰富的 API 和工具集，帮助开发者快速创建高性能、跨平台的应用程序。

## QT 简介

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234249979618.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234249979618.png)

不用关注基础功能的实现细节，超丰富的类库

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234253396804.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234253396804.png)

代码跨平台， 一次编码，任意部署

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723425723899.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723425723899.png)

性能优秀， QT对于图像绘制，网络通信等基础服务做了很大提升 

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234258864407.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234258864407.png)

以下是我基于QT开发的医疗血液分析界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234262768768.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234262768768.png)

每个图显示28W个点，为了解决实时计算，拖动编辑，以及大量点的绘制等痛点，开发中经过详细调研，最终决定选型QT作为开发框架进行产品设计

关于QT安装，Linux 环境安装和 将来移植到Arm环境的安装所选择的安装源并不相同

## 使用场景和应用案例



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234248955974.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234248955974.png)

据统计，目前已有超过10亿台设备和应用程序基于QT构建并稳定运行。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234255109424.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234255109424.png)

## Windows环境安装

### 版本选择

QT的安装分为Windows和Linux, 这两种我们都会介绍，为了快速开发和调试，我们先介绍如何在Windows环境安装编译，关于Linux安装，以及Arm版本的程序发布流程会放在之后的章节介绍。

大家可以去QT官网下载免费个人版本

[https://www.qt.io/zh-cn/](https://www.qt.io/zh-cn/)

选择download try 下载

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234277938053.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234277938053.png)

这样下载的是最新版本的，现在是QT6以上的版本，而我们为了版本统一，对标企业(很多企业追求稳定性选择QT5)，所以选择QT 5.12.4版本作为学习。

QT历史版本的下载地址[https://download.qt.io/archive/qt/](https://download.qt.io/archive/qt/)

QT对5.15以及以上版本已经停止提供离线安装包，

但是，5.15以及以上版本都支持在线安装。比如我们可以选择5.15.2
![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234298005299.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234298005299.png)

Qt5.15以下版本可直接在Index of /archive/qt中下载离线安装包

为了下载QT历史版本，大家可以通过如下连接选择5.12.4下载

[https://download.qt.io/archive/qt/5.12/5.12.4/](https://download.qt.io/archive/qt/5.12/5.12.4/)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234292624800.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234292624800.png)

因为官网下载速度较慢,或者国内网络环境大家无法打开5.15以下的版本，那么我给大家准备了网盘和连接

链接: https://pan.baidu.com/s/1g48NtJopGlX_wSEpuF2t4Q?pwd=7h54 

提取码: 7h54 

### 注册qt官方账号

因为无论qt的离线安装还是在线安装，安装程序都需要执行qt账号认证，所以大家要去qt官网注册一个账号

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234309629681.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234309629681.png)

点击这个红框里的小人，跳转到登录和注册界面[https://login.qt.io/login](https://login.qt.io/login)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234312669948.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234312669948.png)

接下来我们点击注册[https://login.qt.io/register](https://login.qt.io/register)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723431524875.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723431524875.png)

点击注册后弹出注册成功界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234317502390.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234317502390.png)

但是需要去邮箱激活

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234320172745.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234320172745.png)

点击激活连接，跳转到Qt 认证界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234323323916.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234323323916.png)

接下来点击Confirm按钮，就可以提交验证了。

接下来执行登录就可以了。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234325901833.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234325901833.png)

### 安装qt

双击离线安装包qt-opensource-windows-x86-5.12.4.exe进行安装

![https://cdn.llfc.club/1723628633083.jpg](https://cdn.llfc.club/1723628633083.jpg)

点击next进入登录页面，输入之前注册的账号和密码

![https://cdn.llfc.club/1723629034581.jpg](https://cdn.llfc.club/1723629034581.jpg)

然后开始正式安装

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236290941410.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236290941410.png)

选择安装目录

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236291605079.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236291605079.png)

选择组件，大家选择全选

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236292889980.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236292889980.png)

接受许可

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723629499333.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723629499333.png)

默认点击下一步

![https://cdn.llfc.club/1723629588158.jpg](https://cdn.llfc.club/1723629588158.jpg)

进行安装

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236296411299.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236296411299.png)

安装时间看电脑性能

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172362978655.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172362978655.png)

## Linux环境安装(扩展内容)

### 准备资源

关于Linux安装，仍需要去[Index of /archive/qt/5.12/5.12.4](https://download.qt.io/archive/qt/5.12/5.12.4/)网站下载linux对应的版本。

可选择qt-opensource-linux-x64-5.12.4.run版本，

目前我已经下载好

通过网盘分享的文件：qt-opensource-linux-x64-5.12.4.run
链接: https://pan.baidu.com/s/1Tj0897xX3l2lQM_pUGgowQ?pwd=6666 提取码: 6666 

### 安装

将下载好的 qt-opensource-linux-x64-5.12.4.run 拖放到Home目录

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266283852451.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266283852451.png)

设置对应 .run 文件的权限，让其可被执行

``` bash
sudo chmod +x qt-opensource-linux-x64-5.12.4.run
```

可以通过双击 `.run` 文件或通过命令行`sudo ./qt-opensource-linux-x64-5.12.4.run`来启动安装。

``` bash
sudo ./qt-opensource-linux-x64-5.12.4.run
```

安装过程和之前windows类似，输入账号和密码即可

安装完成后不要着急创建qt项目，还需要安装gcc和g++以及依赖的编译库

``` bash
sudo apt-get install g++
sudo apt-get install build-essential
sudo apt-get install libgl1-mesa-dev
sudo apt-get install libglu1-mesa-dev freeglut3-dev
sudo apt-get install cmake
sudo apt-get install automake libtool autoconf make
```

接下来为opengl创建软连接

``` bash
locate libGL
sudo ln -s /usr/lib/x86_64-linux-gnu/libGL.so.1 /usr/lib/libGL.so
```

因为Linux QT默认需要clang编译，这里我们也要安装下clang

``` bash
sudo apt-get install clang
```

接下来我们和windows类似新建一个项目，名字叫做test_qt_pro

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266322923952.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266322923952.png)

我们点击Projects选项，选择管理套件，这个kits就是我们编译要用到的

![https://cdn.llfc.club/image-20240918120849824.png](https://cdn.llfc.club/image-20240918120849824.png)

构建套件可以看到一个是自动检测的(auto-detected)，一个是手动添加的，手动添加的(zackgcc)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266326342649.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266326342649.png)

可以看到自动检测的编译器采用的是clang，而我们刚才已经手动安装了clang

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726633470138.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726633470138.png)

我们可以手动配置

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266337771070.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17266337771070.png)

然后我们运行程序，就可以看到弹出QT界面了



## 移植Qt程序到ARM平台(扩展内容)

### 通用安装32位交叉编译工具

想要发布程序到ARM平台，需要在Linux系统中安装交叉编译的工具，32位交叉编译工具为gcc-arm-linux-gnueabihf.

可以去下面两个网址下载最新版本或者指定版本

[https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads)

或者

[http://releases.linaro.org/components/toolchain/binaries/](http://releases.linaro.org/components/toolchain/binaries/)

我们在ubuntu环境，直接用apt-get 安装即可

使用如下命令进行arm-linux-gcc的安装：

``` bash
sudo apt-get install gcc-arm-linux-gnueabihf
```

使用如下命令进行arm-linux-g++的安装：

``` bash
sudo apt-get install g++-arm-linux-gnueabihf
```

如果要卸载时使用如下命令进行移除，arm-linux-gcc的卸载：

``` bash
sudo apt-get remove gcc-arm-linux-gnueabihf
```

arm-linux-g++的卸载：

``` bash
sudo apt-get remove g++-arm-linux-gnueabihf
```

安装完成后可通过

``` bash
arm-linux-gnueabihf-gcc --version
```

以及

``` cpp
arm-linux-gnueabihf-g++ --version
```

查看是否安装成功

安装成功显示

``` bash
arm-linux-gnueabihf-g++ (Ubuntu/Linaro 7.5.0-3ubuntu1~18.04) 7.5.0
Copyright (C) 2017 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

可通过下面命令查看具体安装在哪个目录了

``` bash
zack@ubuntu:~$ which arm-linux-gnueabihf-g++
/usr/bin/arm-linux-gnueabihf-g++
```

我们写一个helloworld.cpp，里面实现输出

``` bash
#include<iostream>
int main(){
	std::cout << "Hello World!"<<std::endl;
}
```

然后用arm-linux-gnueabihf-g++编译生成可执行文件

``` bash
arm-linux-gnueabihf-g++ ./helloworld.cpp  -o helloworld
```

接下来查看这个可执行文件

``` bash
zack@ubuntu:~$ file helloworld
helloworld: ELF 32-bit LSB shared object, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux-armhf.so.3, for GNU/Linux 3.2.0, BuildID[sha1]=d31246ef67f692baf53fb50b0af33f0f45e3400d, not stripped
```

可以看到helloworld是arm结构的对象, 且为32位

### 通用安装64位交叉编译工具

64位交叉编译工具为 aarch64-linux-gnu-gcc, 输入查看版本

``` bash
zack@ubuntu:~$ aarch64-linux-gnu-gcc -v

Command 'aarch64-linux-gnu-gcc' not found, but can be installed with:
sudo apt install gcc-aarch64-linux-gnu
```

进行安装

``` bash
sudo apt install gcc-aarch64-linux-gnu
```



### 拓展知识

`aarch64-linux-gnu-gcc` 和 `arm-linux-gnueabihf-gcc` 是两个不同的交叉编译器，主要区别在于它们所针对的目标架构和处理器类型。以下是它们的主要区别：

1. **目标架构**

- **aarch64-linux-gnu-gcc**：

  - 这是一个针对 **ARM 64位架构**（也称为 AArch64 或 ARMv8-A）的交叉编译器。
  - 它用于编译能够在 64 位 ARM 处理器上运行的程序，例如最新的 ARM 处理器（如 ARM Cortex-A53、Cortex-A72 等）。

- **arm-linux-gnueabihf-gcc**：

  - 这是一个针对 **ARM 32位架构**（ARMv7 和更早版本）的交叉编译器。
  - 它用于编译能够在 32 位 ARM 处理器上运行的程序，例如较旧的 ARM Cortex-A 系列处理器。

  

2. **数据宽度**

- **aarch64**：

  - 支持 64 位数据宽度，能够处理更大的内存空间和更高效的计算。

- **arm**：

  - 支持 32 位数据宽度，最大可以寻址 4GB 的内存。

  

3. **ABI（应用程序二进制接口）**

- **aarch64**：
  - 使用 AArch64 ABI，支持新的指令集和特性。
- **arm**：
  - 使用 ARM EABI（Embedded Application Binary Interface），支持 ARMv7 和更早版本的特性。



4. **适用场景**



- **aarch64-linux-gnu-gcc**：
  - 适用于开发需要在 64 位 ARM 设备（如 Raspberry Pi 3 及以上版本、某些服务器、嵌入式设备等）上运行的应用程序。
- **arm-linux-gnueabihf-gcc**：
  - 适用于开发需要在 32 位 ARM 设备上运行的应用程序（如 Raspberry Pi 2 及以下版本、许多嵌入式系统等）。



**总结**

简而言之，`aarch64-linux-gnu-gcc` 是用于 64 位 ARM 架构的交叉编译器，而 `arm-linux-gnueabihf-gcc` 是用于 32 位 ARM 架构的交叉编译器。选择哪个编译器取决于你的目标硬件平台和应用程序的需求。

### 本项目交叉编译工具(后期再讲)

本项目交叉编译工具采用`cortexa7hf-neon-poky-linux-gnueabi`,飞凌和正点原子采用这个交叉编译工具。将飞凌提供的

`fsl-imx-x11-glibc-x86_64-meta-toolchain-qt5-cortexa7hf-neon-toolchain-4.1.15-2.0.0.sh`脚本放入ubuntu系统

执行，具体参考这篇文章

[https://blog.csdn.net/zhang_xiaoqiang/article/details/118876398](https://blog.csdn.net/zhang_xiaoqiang/article/details/118876398)

安装好编译工具和qt环境后

接下来配置qt环境

**1 设置环境变量**

要想使用交叉编译环境，需要在qtcreator 运行前设置环境变量，再运行qtcreator程序。

``` bash
# 切换到超级用户
sudo su
# 配置临时环境变量
source /opt/fsl-imx-x11/4.1.15-2.0.0/environment-setup-cortexa7hf-neon-poky-linux-gnueabi
# 启动qt
/home/zack/Qt5.12.4/Tools/QtCreator/bin/qtcreator.sh
```

还有第二种方式，为了方便，我修改了qtcreator.sh文件

``` bash
#!/bin/sh
# 新增写入环境变量
source /opt/fsl-imx-x11/4.1.15-2.0.0/environment-setup-cortexa7hf-neon-poky-linux-gnueabi
```

因为source 是bash环境的命令，sh和bash是不同的shell，sh中没有source命令，所以启动QT就要用

``` bash
sudo bash /home/zack/Qt5.12.4/Tools/QtCreator/bin/qtcreator.sh
```

这么做有一个不好的地方，就是每次启动只能通过命令行启动了，不能直接启动qt。

二者自己权衡，为了方便第二种方式新增了脚本，start_qt.sh脚本，直接运行可启动qt

``` bash
#!/bin/bash
sudo bash /home/zack/Qt5.12.4/Tools/QtCreator/bin/qtcreator.sh 
```

启动方式

``` bash
./start_qt.sh
```

**2 配置qt交叉编译环境**

执行上述脚本后，弹出Qt Creator程序界面,我们通过界面选项配置Qt交叉编译环境.

首先进入 Qt Creator 的 Tools->Options->Kits->Compilers：

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267105532686.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267105532686.png)

点击Add，选择gcc，进一步选择c, 然后进入添加界面，这一步我们添加编译c文件的交叉工具.

更改 Name 文本框内容为 pokygcc，

添加 Compiler path 对应文本框内容为：`/opt/fsl-imx-x11/4.1.15-2.0.0/sysroots/x86_64-pokysdk-linux/usr/bin/arm-poky-linux-gnueabi/arm-poky-linux-gnueabi-gcc`

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267111378587.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267111378587.png)

设置完成后点击 Apply, 完成配置。

同样，点击Add，配置g++ arm编译工具

更改 Name 文本框内容为 pokyg++，

添加 Compiler path 对应文本框内容为：`/opt/fsl-imx-x11/4.1.15-2.0.0/sysroots/x86_64-pokysdk-linux/usr/bin/arm-poky-linux-gnueabi/arm-poky-linux-gnueabi-g++`

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267114124811.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267114124811.png)

点击Apply配置完成。

**3 配置Qt verions**

所谓配置Qt Versions就是配置qmake路径

进入 Qt Versions 界面，点击 Add，选择路径： `/opt/fsl-imx-x11/4.1.15-2.0.0/sysroots/x86_64-pokysdk-linux/usr/bin/qt5/qmake`

Versions name 更改为 pokyqt5，然后点击 Apply

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726711611211.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726711611211.png)

**4 Kits配置**

进入 Kits 界面，点击 Add： 

Name 更改为 pokyarm； 

Device type 选择 `Generic Linux Device`；

 Sysroot 路径：`/opt/fsl-imx-x11/4.1.15-2.0.0/sysroots`；

 Compiler 选择：pokygcc和pokyc++；

 Qt version 选择：Qt5.6.2(pokyqt5)；

 Qt mkspec 为 linux-oe-g++； 

配置好之后，点击 Apply

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267119598766.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267119598766.png)

至此，Qt Creator环境配置完成，我们还需要安装一些其他Qt相关的库，这些库Qt会调用，不安装的话可能会出现一些报错信息.

我们之前已经安装了 这些库，如果同学未安装可以按如下方式安装

``` bash
# 切换到超级用户
sudo su
# 安装opengl库
apt-get install libgl1-mesa-dev
# 安装automake工具
apt-get install automake libtool autoconf make
```

**5 修改配置**

修改qmake.conf，防止编译产生警告

``` bash
vim /opt/fsl-imx-x11/4.1.15-2.0.0/sysroots/cortexa7hf-neon-poky-linux-gnueabi/usr/lib/qt5/mkspecs/linux-oe-g++/qmake.conf 

```

将这一行注释

``` bash
#include(../oe-device-extra.pri)
```

然后保存，退出。 至此我们的 Qt Creator 交叉编译环境就正式搭建完了，我们可以来开发在开发板上运行的 Qt 应用 了.

我们随便打开一个Qt Creator项目，比如选择analogclock项目，然后点击Projects设置编译工具，默认是没有我们手动添加的编译工具的，我之前手动添加了gcc，以及pokyarm，我们点击加号把他们加进来

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726712930320.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726712930320.png)

然后点击Manage Kits 管理并选择我们要使用的编译套件，这里选择pokyarm, 点击apply

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267130342267.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267130342267.png)

同样qt versions切换为我们对应的arm qmake

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267132359262.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267132359262.png)

在Debug按钮选择pokyarm编译套件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267134053368.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267134053368.png)

然后点击rebuild可生成arm文件，但是会报错opengl的问题，网上可参考这个解决

[https://www.cnblogs.com/GregTse/p/12031645.html](https://www.cnblogs.com/GregTse/p/12031645.html)



## QT项目构成

### 创建并运行项目

我们打开QT Creator创建一个QT项目

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236064451570.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236064451570.png)

选择Qt Widgets Application

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236065552244.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236065552244.png)

然后选择项目所在位置和项目名称，这个大家自己选择

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236068802838.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236068802838.png)

点击下一步，会看到选择构建套件的选项，这个构建套件就是我们编译项目所选择的编译器，列表中列出了我安装的编译器，大家使用Mingw即可。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723607192504.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723607192504.png)

再次点击下一步,进入项目主界面设置

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236080242300.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236080242300.png)

我们选择了QMainWindow作为基类，创建MainWindow作为主界面类

点击下一步，因为我们创建的是独立的项目，不需要作为子项目添加到别的项目中

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236081552820.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236081552820.png)

点击完成项目创建成功

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236084642553.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236084642553.png)

qt项目在编译前，我们需要配置一下编译器，点击Debug图标(小电脑)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236101516714.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236101516714.png)

选择自己安装好的编译器即可

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236102426756.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236102426756.png)

然后点击绿色的小三角运行，可以看到弹出了我们的QT窗口

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236104055442.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236104055442.png)

### 动手操作

带着大家动手创建一个项目

### 项目结构

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236169372519.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236169372519.png)

一个完整的QT项目基本包含：

- 项目名称：HelloWorld
- 项目配置文件：pro
- 头文件列表：Headers
- 源文件列表：Sources
- UI文件列表：Forms
- 资源列表：Resources

## QT 助手

QT为我们提供了丰富的查询文档，我们可以通过QT Assistant查询。QT Assistant在QT安装目录下,根据版本号和编译器类型，查看bin目录下可看到

D:\Qt\Qt5.12.4\5.12.4\mingw73_64\bin\assistant.exe

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236171901662.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236171901662.png)

点击这个assistant.exe，可弹出文档界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236180314204.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236180314204.png)

我们可以通过 索引-查找 功能自己搜索要学习的QT类

## 总结

1. QT项目基本构成有哪些
   - 项目名称：HelloWorld
   - 项目配置文件：pro
   - 头文件列表：Headers
   - 源文件列表：Sources
   - UI文件列表：Forms
   - 资源列表：Resources
2. QT Assistant有什么作用？(查文档)



# 第二章 QT基础

## QT模块简介

我们开发会设计很多功能，比如网络，图形界面等，QT帮我们将这些功能集成在了不同的模块，总体来说分为基础模块和附加模块。基础模块在安装qt creator的时候会自动安装。附加模块需要手动选择安装。



- 基础模块

![https://cdn.llfc.club/1723076863252%281%29.jpg](https://cdn.llfc.club/1723076863252%281%29.jpg)


- 附加模块

![https://cdn.llfc.club/1723077113030.jpg](https://cdn.llfc.club/1723077113030.jpg)

## QT的容器类

和C++ 一样， QT也有自己的容器类, 包括顺序容器和关联容器

- 顺序容器
    - QList
    - QVector
    - QStack
    - QQueue

- 关联容器
    - QMap
    - QSet
    - QMultiMap
    - QHash

### QList

#### 列表初始化

QList为Qt独有的列表类型，支持任何位置的插入以及根据下标访问，同时支持迭代器操作，支持根据迭代器删除，根据下标删除

使用QList要包含头文件<QList>, 使用QList要指定存储的类型

``` cpp
    //存储int类型的QList
    QList<int> int_list;
    //存储string类型的QList
    QList<std::string> str_list;
```

QList可通过列表进行初始化构造

``` cpp
   //通过列表初始化
    QList<int> num_list = {0,1,2,3,4,5,6,7,8,9};
```

#### 插入操作

QList插入操作,可在指定位置插入数据，也可在前后插入数据

``` cpp
//在指定位置前插入数据
void  insert(int i, const T &value);
//在指定迭代器位置前插入数据
QList::iterator insert(QList::iterator before, const T &value);
//在尾部插入
void append(const T &value);
void push_back(const T &value);
//头部插入
void prepend(const T &value);
void push_front(const T &value);
```

练习：

1 初始化QList数据为{0，1，2，3，4，5，6，7，8，9}，

2 在下标为2的元素之前插入数据100

3 并分别用prepend和push_back在尾部插入1024和2048，

4 然后用prepend和push_front在头部分别插入1023，2023

5 通过迭代器遍历在找到的第一个数据4之前插入22.

6 打印QList数据查看结果


提示：

QList迭代器操作和标准C++一样，可通过for,while等循环遍历

``` cpp
for(auto iter = num_list.begin(); iter != num_list.end(); iter++){

}
```

QT环境下可通过qDebug()输出日志信息，用法类似于std::cout,使用时要包含<QDebug>

``` cpp
#include <QDebug>
```

答案：

``` cpp
void list_insert(){
    //存储int类型的QList
    QList<int> int_list;
    //存储string类型的QList
    QList<std::string> str_list;
    //通过列表初始化
    QList<int> num_list = {0,1,2,3,4,5,6,7,8,9};
    //在下标为2的元素前面
    num_list.insert(2,100);
    //在num_list尾部插入1024
    num_list.append(1024);
    //在num_list尾部插入2048
    num_list.push_back(2048);
    //在num_list头部插入1023
    num_list.push_front(1023);
    //在num_list头部插入2023
    num_list.prepend(2023);

    for(auto iter = num_list.begin(); iter != num_list.end(); iter++){
        if(*iter == 4){
            num_list.insert(iter,22);
            break;
        }
    }

    qDebug() << "num_list is " << num_list;
}
```

#### 删除操作

erase操作可以删除某个迭代器所指向的元素, 删除后返回下一个元素的迭代器

``` cpp
QList::iterator erase(QList::iterator pos)
```

演示代码

``` cpp
void erase_demo(){
    QList<int> num_list = {0,1,2,3};
    //第一个元素的迭代器
    auto first = num_list.begin();
    //返回第二个元素的迭代器
    auto second = num_list.erase(first);
    qDebug()<< "second value is " << *second;
}
```

erase可以删除某个区间的元素，从begin迭代器开始，到end迭代器结束(不包括end)，删除后返回end指向的元素的迭代器

``` cpp
QList::iterator erase(QList::iterator begin, QList::iterator end)
```

演示代码

``` cpp
void erase_between(){
    QList<int> num_list = {0,1,2,3};
    //第一个元素的迭代器
    auto first = num_list.begin();
    //迭代器偏移2个元素指向元素2
    auto second = first+2;
    //删除0~2的数据，不包括2
    auto next_iter = num_list.erase(first, second);
    //next_iter 指向的元素为2
    qDebug()<< "next_iter value is " << *next_iter;
}
```

也可通过removeAt删除指定索引的元素

``` cpp
void removeAt(int i)
```

演示代码

``` cpp
void remove_demo(){
    QList<int> num_list = {0,1,2,3};
    //删除下标为1的元素
    num_list.removeAt(1);
    qDebug() << "num_list is " << num_list;
}
```

**练习**

1 初始化一个QList,数据为{0,1,2,3,4,5,6,7,8,9}

2 通过一次遍历删除其中的偶数元素

3 打印查看结果

答案:

``` cpp
void list_erase(){
    //通过列表初始化
    QList<int> num_list = {0,1,2,3,4,5,6,7,8,9};
    for(auto iter = num_list.begin(); iter != num_list.end();){
        //如果为偶数则删除，因为删除会自动返回下一个元素的迭代器
        if(*iter % 2 == 0){
            iter = num_list.erase(iter);
            continue;
        }

        //如果为奇数，则让迭代器自增，指向下一个元素
        iter++;
    }

    qDebug() << "num_list is " << num_list;
}
```

#### 遍历方式

QT的容器也支持和C++ stl标准容器一样的遍历方式,除了迭代器方式，还可以通过C++ 11 的for写法

``` cpp
void list_forc11(){
    QList<int> num_list = {0,1,2,3,4,5,6,7,8,9};
    //c++11 方式遍历
    for(auto & num: num_list){
        qDebug() << num ;
    }
}
```

QT提供了类似C++11的遍历方式foreach

``` cpp
void list_foreach(){
    QList<int> num_list = {0,1,2,3,4,5,6,7,8,9};
    //QT提供的foreach方式遍历
    foreach(auto &num, num_list){
        qDebug() << num ;
    }
}
```

#### clear清空容器

Qt的容器都包含clear操作,和size操作

``` cpp
//清空容器
void clear();
//返回容器大小，返回的是存储元素的个数
int size() const
```

clear会清空容器存储的元素，但是容器所占用的空间不会被回收。

大家学习过std::vector，其中 包含size和capacity的概念，size表示vector中元素的个数，clear会清空vector，将size设置为0. 但是vector的capacity不会减少，也就是vector占用的空间不会减少。

我们以QList的清空为例

``` cpp
void list_clear(){
    QList<int> list = {1,3,4,7,8,2};
    //清空list
    list.clear();
}
```

#### swap 操作

Qt的容器都包含swap操作，实现容器内部数据交换的功能。

``` cpp
void swap();
```

小技巧：

我们知道clear操作只能清空容器存储的数据，但是无法回收内存。

我们可以利用swap将我们要回收的容器L1和一个空的容器L2做交换，而空容器L2会因为交换存储L1的数据，L1变为空。

L2会在生命周期结束后自动析构回收内存。可以看看这个例子

``` cpp
void list_swap(){
    QList<int> list = {1,3,4,7,8,2};
    //定义一个空的list
    QList<int> empty_list;
    //将list和empty_list交换，list空间快速被释放。
    list.swap(empty_list);
    //empty_list会随着析构回收内存
}
```



### QVector

QVector和std::vector用法类似，在QT6之后的版本QList和QVector功能上进行了合并，所以大家学会了QList就足够了。

还是看一下QVector用法当作复习

``` cpp
void vector_use(){
    QVector<int> num_vec;
    //向末尾插入元素100
    num_vec.push_back(100);
    //头部插入99
    num_vec.push_front(99);
    //向末尾插入元素为1024
    num_vec.append(1024);
    //删除头部元素
    num_vec.pop_front();
    //删除尾部元素
    num_vec.pop_back();
    //清空vector
    num_vec.clear();
}
```

vector其余的用法和QList类似，不做赘述。

### QStack

QStack顾名思义是栈容器，就是先进后出的容器。其继承自QVector,使用时需包含头文件<QStack>

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236934464041.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17236934464041.png)

大家可以把栈容器想象成一个收纳箱，我们把要收纳的物品放到箱子里，取出的时候从上面取。

它的公有成员函数主要有四个

``` cpp
// 弹出栈顶元素
T  pop()
// 元素t入栈
void push(const T &t)
// 交换两个栈元素
void swap(QStack<T> &other)
//返回栈顶元素(注意未弹出栈)
T &  top()
//返回栈顶元素，重载版本返回常量引用
const T &top() const
//判断栈是否为空
bool empty(); 
```

练习：

有这样一组数字{6,1,0,5,2,9}，要求：

1 将这组数列中每个元素在合适的时机入栈

2 栈顶元素出栈前打印栈顶元素，并且出栈

3 保证打印的数据顺序为从小到大

提示：

例如数列为 7，2，4，那么入栈顺序为7，2，打印栈顶元素为2，并弹出2，接着4入栈，打印栈顶元素为4，并弹出4，打印栈顶元素为7，并弹出7.

示意图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723696912859.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723696912859.png)

答案：

``` cpp
void stack_sort(){
    QList<int> list = {6,1,0,5,2,9};
    qDebug() << "利用栈顺序输出元素";
    QStack<int> stack;
    for(auto iter = list.begin(); iter != list.end(); iter++){
        //判断如果栈为空则入栈
        if(stack.empty()){
            //qDebug() << "元素 " << *iter << " 入栈";
            stack.push(*iter);
            continue;
        }
        //判断如果要插入的元素比栈顶元素小则入栈
        if(*iter < stack.top()){
            //qDebug() << "元素 " << *iter << " 入栈";
            stack.push(*iter);
            continue;
        }

        //如果要插入的元素比栈顶元素大，则打印栈顶元素，并弹出栈顶元素,直到比栈顶元素小为止
        while(!stack.empty() && *iter > stack.top()){
            //元素比栈顶元素大则打印栈顶元素并出栈
                qDebug() << "元素 " << stack.top() <<" 出栈";
                stack.pop();
        }

        //qDebug() << "元素 " << *iter << " 入栈";
        stack.push(*iter);
    }
    qDebug()<< "剩余栈元素";
    //list遍历结束，可能栈中有元素，比如入list中存储的3,2,1
    while(!stack.empty()){
        qDebug() << "元素 " << stack.top() <<" 出栈";
        stack.pop();
    }
}
```

### Queue

Queue是队列结构，其继承自QList,使用需包含<QQueue>,队列是先进先出的结构，例如我们排队等公交,站在队首的人优先出队并上车。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237045873710.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237045873710.png)

基本成员函数包括如下

``` cpp
// 从队首弹出元素
T  dequeue()
// 将元素放入队尾
void enqueue(const T &t)
// 返回队首元素，不弹出
T & head()
// 返回队首元素，不弹出，返回值为常量引用
const T & head() const
// 交换两个队列内容
void  swap(QQueue<T> &other)
// 判断队列为空
bool isEmpty() const

```

**练习**：

将一个数字序列{6，7，2，1，3，5，8，0，9}中的数字依次入队，全部入队后，依次出队，打印四次出队后的队列信息

### QMap

QMap和C++的std::map用法类似，功能主要包括插入,删除，查找等。使用时需包含<QMap>头文件

#### insert插入

将<key, value>插入map。

``` cpp
QMap::iterator insert(const Key &key, const T &value)
```

当map中存在某个key1值，对应的value值为value1,再次插入相同的key值<key1, value1> ，则将原来的value1更新为最新的value2。

案例：

``` cpp
void map_insert(){
    //存储学生名字和年龄的map
    QMap<QString, int> students_map;
    //李雷今年23
    students_map.insert("LiLei", 23);
    //李雷年龄更新为24
    students_map.insert("LiLei",24);
    qDebug()<< students_map;
}
```

打印students_map可以看到map中仅有一个元素，key为LiLei，value为24.

``` cpp
QMap(("LiLei", 24))
```



#### insertMulti插入重复key

insertMulti支持插入的key为重复的<key,value>数据，如果key已经在map中存在，则额外再插入一条数据。

我们看下面的例子

``` cpp
void map_multi_insert(){
    //存储学生名字和年龄的map
    QMap<QString, int> students_map;
    //李雷今年23
    students_map.insertMulti("LiLei", 23);
    //班里还有一个叫李雷的学生，今年24岁
    students_map.insertMulti("LiLei",24);
    qDebug()<< students_map;
}
```

我们打印students_map，可以看到存在两条数据，两条数据的key都是LiLei, 但是value不同

``` bash
QMap(("LiLei", 24)("LiLei", 23))
```

#### 判空操作

QMap的判空操作和Queue,QStack,QList等一样，都是通过isEmpty

``` cpp
// 判断map是否为空
bool isEmpty() const
```

#### 查找操作

QMap 支持根据key查找map中的元素，如果找到返回找到元素的迭代器，如果未找到则返回无效的迭代器end

``` cpp
//根据key查找对应数据，返回迭代器
QMap::iterator find(const Key &key)
//根据key查找对应数据，返回常量迭代器，当map为常量时会调用这个重载版本
QMap::const_iterator find(const Key &key) const

```

例如，我们在QMap中插入一条数据<"LiLei", 23>， 先查找key为“LiLei”的数据，是可以找到的，如果查找key为“HanMeiMei”，是无法找到的，find的返回值为一个无效的迭代器，指向map的end。

所以每次我们使用find之后要判断查找的返回的迭代器是否有效，有效才访问数据。

看下面这个例子

``` cpp
void map_find(){
    QMap<QString, int> students_map;
    //插入<"LiLei",23>数据
    students_map.insert("LiLei",23);
    //查找key为"LiLei"的数据
    auto iter = students_map.find("LiLei");
    if(iter != students_map.end()){
        qDebug()<<"find key LiLei, value is " << iter.value();
    }else{
        qDebug()<<"find key LiLei failed ";
    }

    //查找key为"HanMeiMei"的数据
    iter = students_map.find("HanMeiMei");
    if(iter != students_map.end()){
         qDebug()<<"find key HanMeiMei, value is " << iter.value();
    }else{
        qDebug()<<"find key HanMeiMei failed ";
    }
}
```

上面的程序输出

``` bash
find key LiLei, value is  23
find key HanMeiMei failed 
```



#### 重载的[]运算符

QMap和std::map一样，也重载了[]运算符，[]运算符的参数为要查找key，返回值为value的引用

``` cpp
// 根据key查找map返回
T & operator[](const Key &key)
const T  operator[](const Key &key) const
```

**注意**

当key不存在的时候，会根据T的默认构造函数构造一个value插入到map中

代码示例

``` cpp
void map_operator_find(){
    QMap<QString, int> students_map;
    //根据key查找，返回value
    auto value = students_map["Zack"];
    qDebug() << "value is " << value;
    qDebug() << "students_map is " << students_map;
}
```

上面的代码输出

``` cpp
value is  0
students_map is  QMap(("Zack", 0))
```



#### 获取值

我们知道使用重载的[]运算符，根据key获取value时，如果key不存在则会默认插入一条数据，这在一定情况下会产生误差。

我们可以通过value函数根据key获取value， 当key不存在的时候会返回一个value的默认值，如果value是基础类型则返回基础类型的默认值(int 为0， QString 为 “” 等)，如果value为自定义的类类型，则调用默认构造函数返回。

我们可以为value函数第二个参数传递一个值，当key不存在的时候返回我们传递的值

``` cpp
const T value(const Key &key, const T &defaultValue = T()) const;
```

**注意**

当key不存在的时候不会向QMap中插入数据。

示例

``` cpp
void map_value(){
    QMap<QString, int> students_map;
    students_map.insert("Bob",29);
    //根据key查找，返回value
    auto zk_val = students_map.value("Zack");
    qDebug() << "zack value is " << zk_val;

    auto bob_val = students_map.value("Bob");
    qDebug() << "apple value is " << bob_val;

    auto lion_val = students_map.value("Lion",30);
    qDebug() << "lion_val value is " << lion_val;

    qDebug() << "students_map is " << students_map;
}
```

输出

``` cpp
zack value is  0
apple value is  29
lion_val value is  30
students_map is  QMap(("Bob", 29))
```

#### contains

QMap提供了contains函数，用来判断是否存在某个键的记录

``` cpp
bool contains(const Key &key) const
```

示例代码

``` cpp
void map_contains(){
    QMultiMap<QString, int> multiMap;
    multiMap.insert("zack",25);
    //判断是否存在
    bool b_exist = multiMap.contains("zack");
    if(b_exist){
        qDebug()<< "map中存在key为zack的记录";
    }else{
        qDebug()<< "map中不存在key为zack的记录";
    }
}
```

代码输出

``` cpp
map中存在key为zack的记录
```



#### 删除操作

QMap的删除操作支持两种方式：

``` cpp
//根据迭代器删除，删除pos指向的元素
QMap::iterator erase(QMap::iterator pos);
//根据key值删除，删除map中键为key的数据
int remove(const Key &key)
```

示例代码

``` cpp
void map_del(){
    QMap<QString, int> students_map;
    //插入<"LiLei",23>数据
    students_map.insert("LiLei",23);
    //插入<"HanMeiMei",29>
    students_map.insert("HanMeiMei",29);
    //根据key删除,删除key为"HanMeiMei"的数据
    students_map.remove("HanMeiMei");
    //先查找key为"LiLei"的数据，返回迭代器
    auto iter = students_map.find("LiLei");
    //判断迭代器是否有效
    if(iter == students_map.end()){
        return;
    }
    //根据迭代器删除数据
    students_map.erase(iter);
    qDebug()<< "students_map is " << students_map;
}
```

上面的程序输出

``` cpp
students_map is  QMap()
```

说明两个方式都可以删除数据。

练习：

统计一个字符串列表中，每个字符串出现的个数

字符串列表为{"Zack","Ella","Alice","Zack","Ella","Richard","Ella"}

要求将字符串和出现的个数存储到QMap中, 打印QMap数据



答案：

``` cpp
void calc_words(){
    QList<QString> words = {"Zack","Ella","Alice","Zack",
                            "Ella","Richard","Ella"};
    QMap<QString, int> word_map;
    for(auto &word : words){
        //根据[]运算符重载规则，如果word_map中不存在word，则value会被初始化为0
        //如果存在则自增
        word_map[word]++;
    }
    qDebug() << "word_map is " << word_map;
}
```

### QMultiMap

`QMultiMap` 是 Qt 提供的一个多重映射容器类，它允许一个键对应多个值。与 `QMap` 类似，`QMultiMap` 也是基于平衡二叉树实现的，因此键值对是按键排序的。`QMultiMap` 的键和值都可以是任意类型，只要键类型支持比较操作。

#### 插入键值对

QMultiMap插入相同的key不会修改之前的数据，会新增记录

``` cpp
void multi_map_insert(){
    QMultiMap<QString, int> multiMap;
    //插入键值对，key为apple
    multiMap.insert("apple", 1);
    //允许插入相同的key，
    //不会修改之前apple的value，会新增一条
    multiMap.insert("apple", 2);
    //插入键值对
    multiMap.insert("banana", 3);
    qDebug() << "multimap is " << multiMap;
}
```

上面代码输出

``` cpp
multimap is  QMap(("apple", 2)("apple", 1)("banana", 3))
```

#### 访问值

QMultiMap支持返回指定key对应的所有value值，以列表形式返回

``` cpp
QList<T> values(const Key &key) const

```

代码示例

``` cpp
QList<int> appleValues = multiMap.values("apple");  // 返回 [1, 2]
int firstAppleValue = multiMap.value("apple");      // 返回 1（第一个值）
```

#### 删除键值对

QMultiMap可通过remove操作删除所有建为key的键值对，返回删除的个数

``` cpp
int QMap<Key, T>::remove(const Key &akey)
```

案例

``` cpp
multiMap.remove("apple");  // 删除所有键为 "apple" 的项
```

也可以根据<key,value>键值对删除指定的项

``` cpp
int remove(const Key &key, const T &value);
```

案例

``` cpp
    //删除key为apple，value为2的项
    multiMap.remove("apple",2);
```



#### 遍历QMultiMap

QMultiMap的遍历和QMap一样

``` cpp
QMultiMap<QString, int>::iterator it;
for (it = multiMap.begin(); it != multiMap.end(); ++it) {
    qDebug() << it.key() << ": " << it.value();
}
```

### QSet

`QSet` 是 Qt 提供的一个集合容器类，用于存储唯一的元素。与 `QList` 或 `QVector` 不同，`QSet` 不允许重复的元素，并且提供了高效的插入、删除和查找操作。`QSet` 的元素类型需要支持哈希函数和相等比较操作。使用时需包含 <QSet>头文件

#### 插入元素

通过insert将T类型的数据value插入集合

``` cpp
QSet::iterator insert(const T &value)

```

示例

``` cpp
 // 定义一个 QSet
 QSet<QString> set;
 // 插入元素
 set.insert("apple");
 set.insert("banana");
```

还可以通过<< 操作符实现插入

示例

``` cpp
//插入cherry，date
set << "cherry" << "date";
```

####  判断元素是否存在

``` cpp
bool contains(const T &value) const
```

示例

``` cpp
// 检查元素是否存在
 if (set.contains("apple")) {
     qDebug() << "'apple' exists in the set.";
 }
```

####  删除元素

删除元素和QMap类似，通过remove操作

``` cpp
bool remove(const T &value);
```

示例

``` cpp
// 删除元素
set.remove("banana");
```

#### 遍历

我们可以通过迭代器遍历QSet中的元素

``` cpp
 // 遍历 QSet
 QSet<QString>::iterator it;
 for (it = set.begin(); it != set.end(); ++it) {
     qDebug() << *it;
 }
```

### QHash

`QHash` 是 Qt 提供的一个基于哈希表的数据容器类，用于存储键值对。与 `QMap` 类似，`QHash` 也允许通过键快速查找值，但 `QHash` 的查找、插入和删除操作的平均时间复杂度为 O(1)，因此在处理大量数据时通常比 `QMap` 更高效。`QHash` 的键和值可以是任意类型，只要键类型支持哈希函数和相等比较操作。使用时需包含 <QHash> 头文件

#### 插入键值对

QHash的插入操作和QMap一样，通过insert将key和value插入即可，当然也可以通过重载的[]进行插入

示例：

``` cpp
// 定义一个 QHash
 QHash<QString, int> hash;

 // 插入键值对
 hash.insert("apple", 1);
 hash["banana"] = 2;
 hash.insert("cherry", 3);
```

#### 访问值

QHash根据key获取value的方式和QMap一样

``` cpp
// 访问值
 int appleValue = hash.value("apple");
 qDebug() << "Value for 'apple':" << appleValue;  // 输出 1

 int bananaValue = hash["banana"];
 qDebug() << "Value for 'banana':" << bananaValue;  // 输出 2
```

#### 判断和删除key

QHash判断key是否存在，以及删除key的操作，和QMap一样

示例

``` cpp
 // 检查键是否存在
 if (hash.contains("banana")) {
     qDebug() << "'banana' exists in the hash.";
 }

 // 删除键值对
 hash.remove("apple");
```

#### 遍历

QHash同样支持迭代器遍历

``` cpp
// 遍历 QHash
 QHash<QString, int>::iterator it;
 for (it = hash.begin(); it != hash.end(); ++it) {
     qDebug() << it.key() << ": " << it.value();
 }

 // 获取 QHash 的大小
 qDebug() << "Size of hash:" << hash.size();
```

## QVariant 万能类型

`QVariant` 是 Qt 提供的一个通用数据类型容器，可以存储不同类型的数据。它类似于 C++ 的 `std::any` 或 `boost::any`，能够在运行时存储和转换多种类型的数据。`QVariant` 在需要处理多种数据类型的场景中非常有用，例如数据库操作、动态属性系统等。使用时需包含<QVariant>

``` cpp
#include <QVariant>
```

###  创建QVariant对象

通过直接赋值，可将不同类型的数据存储到QVariant

``` cpp
QVariant var1 = 42;                   // 存储整数
QVariant var2 = 3.14;                 // 存储浮点数
QVariant var3 = "Hello, QVariant!";   // 存储字符串
QVariant var4 = QString("Hello!");    // 也可以存储 QString
```

### 访问存储的值

QVaraint提供了一系列转化操作，将QVariant类型转化为基本类型和QT支持的类型

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723776499822.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723776499822.png)

示例

``` cpp
// 访问存储的值
int intValue = var1.toInt();
double doubleValue = var2.toDouble();
QString strValue = var3.toString();

qDebug() << "intValue:" << intValue;         // 输出 42
qDebug() << "doubleValue:" << doubleValue;   // 输出 3.14
qDebug() << "strValue:" << strValue;         // 输出 "Hello, QVariant!"
```

### 检测类型

可通过QVariant的type()函数返回QVariant存储的类型

``` cpp
QVariant::Type QVariant::type() const
```

可通过QVariant的canConvert函数判断是否能转化为某个类型

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237768914960.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237768914960.png)

示例：

``` cpp
if(var1.type() == QVariant::Int){
     qDebug() << "var1 is an integer.";
}

if(var2.canConvert<float>()){
    qDebug() << "var2 can convert to float.";
}

if(var3.canConvert<QString>()){
    qDebug() << "var3 can convert to QString.";
}
```

###  存储自定义类型

可通过QVariant的成员函数setValue将一个自定义类型的值设置到QVariant类型的变量里，如果这个类型不支持QVariant存储，则会产生编译错误

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237780418871.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237780418871.png)

**示例**：

我们用QVariant存储Qt的Qpoint对象，QPoint是Qt提供的2D点数据类型。

``` cpp
QVariant v5;
v5.setValue(QPoint(3,4));
```

如果我们存储自己定义的类Student对象，会编译失败, 我们先演示这个错误并带着大家解决

先定义Student类

``` cpp
class Student
{
public:
    Student();
    Student(QString name, int num);
    int _num;
    QString _name;
};
```

实现构造函数

``` cpp
//无参构造
Student::Student():_num(0),_name("")
{

}
//有参构造
Student::Student(QString name, int num):_num(num),_name(name)
{

}
```

接下来我们用QVariant存储1个Student对象

``` cpp
QVariant v5;
v5.setValue(QPoint(3,4));

Student s1("Zack",1001);
QVariant student_var;
student_var.setValue(s1);
```

编译上面代码会报错

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237793562135.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237793562135.png)

这段错误的意思是Qt的元对象系统不识别我们的Student类型，无法通过QVariant来存储。元对象详细的知识会在之后讲解，接下来我们提供问题的解决方案。

**首先在Student头文件里包含<QMetaType>头文件，然后在Student类下调用Q_DECLARE_METATYPE(Student)**

``` cpp
#include <QMetaType>

class Student
{
public:
    Student();
    Student(QString name, int num);
    int _num;
    QString _name;
};
//声明Student为元对象类型
Q_DECLARE_METATYPE(Student)
```

**然后在要存储之前将Student类型注册到元对象系统中**

``` cpp
qRegisterMetaType<Student>("Student");
```

**再次运行程序通过！**

QVariant有一个静态成员fromValue可以将一个自定义类型构造为QVariant类型返回，其功能和setValue类似

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237783349583.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237783349583.png)

**示例**

``` cpp
//通过fromValue将自定义类型转化为QVariant类型
auto s2_val = QVariant::fromValue(Student("Ella",1002));
```



### 访问自定义类型

我们学会了用QVariant存储任意数据类型，接下来我们可通过value()函数取出我们存储的数据

``` cpp
T QVariant::value() const
```

**官方说明**

返回QVaraint存储的数据，可通过canConver()判断QVariant能否转化为某个具体类型，如果不能，则返回一个该类型默认构造的值。

**示例**

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237812229370.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237812229370.png)

v无法转化为MyCustomStruct类型，所以c2会是MyCustomStruct默认构造的结果。

**练习**

用QVariant类型的变量存储一个Student对象，然后再将QVariant转化为Student类型。

**答案**

``` cpp
//注册Student为元对象类型
qRegisterMetaType<Student>("Student");
//这时存储就没问题了
Student s1("Zack",1001);
QVariant student_var;
student_var.setValue(s1);
//转换为Student对象
auto var_to_s1 = student_var.value<Student>();
qDebug()<<"var_to_s1 name is " << var_to_s1._name
       << " num is " << var_to_s1._num;
//通过fromValue将自定义类型转化为QVariant类型
auto s2_val = QVariant::fromValue(Student("Ella",1002));
//转换为Student对象
auto var_to_s2 = s2_val.value<Student>();
qDebug()<<"var_to_s1 name is " << var_to_s2._name
       << " num is " << var_to_s2._num;
```

### 获取存储类型

``` cpp
auto type_name = s2_val.typeName();
qDebug() << "s2_val store type is " << type_name;
```

### 判断QVariant是否为空

``` cpp
if (var.isNull()) {
    // var 为空
}
```

### 清空QVariant

``` cpp
var.clear();
```

## QString

`QString` 是 Qt 框架中用于处理字符串的类。它提供了丰富的功能来创建、操作和处理字符串。`QString` 支持 Unicode，可以方便地处理国际化文本.

使用时需包含<QString>头文件

### 创建QString

可以通过将一个字面值常量字符串赋值给QString

``` cpp
QString str1 = "Hello, QString!";
```

也可以利用QString的构造函数，传入字面值常量进行构造

``` cpp
QString str2("Hello, QString!");
```

也可以通过一个Utf-8编码的字符串初始化QString

``` cpp
QString str3 = QString::fromUtf8("你好，QString！");
```

### 字符串连接

因为QString重载了+运算符，所以拼接两个字符串可以直接相加。

另外QString也提供了append的方式，将要追加的字符串添加到QString后面

``` cpp
QString str4 = str1 + " " + str2;
str1.append(" How are you?");
```

### 字符串比较

QString重载了==运算符，可以比较两个字符串是否相等

也可以通过compare的方式比较两个字符串是否相等

``` cpp
if (str1 == str2) {
    // 字符串相等
}
if (str1.compare(str2) == 0) {
// 字符串相等
}
```

###  字符串长度

``` cpp
int length = str1.length();
```

### 根据索引返回字符

QString可以根据指定下标返回字符, 返回的是QChar类型，QChar和C++的char用法没有太大区别

``` cpp
QChar ch = str1.at(0);  // 获取第一个字符
```

### 查找子串

indexOf可以查找子串，找到了返回子串第一个字符所在的索引，未找到则返回-1

``` cpp
int index = str1.indexOf("Qt");
if (index != -1) {
    // 找到子字符串
}
```

### 替换子串

通过replace替换子串

``` cpp
str1.replace("Qt", "QString");
```

### 截取子串

``` cpp
 // 从索引 0 开始截取 5 个字符
QString subStr = str1.mid(0, 5); 
```

### 拆分字符串

可通过split切割字符串，split传入字符串，将按照传入的字符串进行切割，返回一个QStringList。

QStringList大家可以理解为QList<QString>即可，用法二者相同

``` cpp
QStringList list = str1.split(" ");
```

### 去除空白字符串

trimmed会去除掉字符串中的空格，将字符串连接起来

``` cpp
QString trimmedStr = str1.trimmed();
```

### 格式化字符串

字符串可以通过arg操作将参数填充到样式字符串并返回一个新的字符串

``` cpp
QString formattedStr = QString("The value is %1").arg(42);
```

### 练习

有字符串"zero4BeginHello World! Hello Heima! I love Heima!End"，将字符串Begin和End中间的字符串按照空格切割，统计并打印出现的单词个数

### 答案

``` cpp
void calc_words(){
    //初始化一个字符串
    QString wordstr = "zero4BeginHello World! Hello Heima! I love Heima!End";
    //获取"Begin"在字符串中的索引
    int begin = wordstr.indexOf("Begin");
    //如果未找到Begin则返回
    if(begin == -1){
        return;
    }
    //begin向后偏移"Begin"字符串长度，保证从"Begin"之后截取
    begin += strlen("Begin");
    //获取"End"在字符串中的索引
    int end = wordstr.indexOf("End");
    //如果未找到end则返回
    if(end == -1){
       return;
    }

   //截取获取Begin和End中的字符串
   wordstr = wordstr.mid(begin,end-begin);
   qDebug()<< "wordstr is " << wordstr;
   //定义一个map统计单词个数
   QMap<QString,int> counter_map;
   //按照空格切分字符串，返回一个
   auto words_lsit = wordstr.split(" ");
   for(auto & word: words_lsit){
       //先将word去空格，因为字符串中可能有连续多个空格
       word = word.trimmed();
       //trimmed会将空格清除掉，所以判断word是否为空
       if(word.isEmpty()){
           continue;
       }
       //统计单词个数
       counter_map[word]++;
   }

   //打印单词出现的个数
   for(auto iter = counter_map.begin(); iter != counter_map.end(); iter++){
       //格式化字符串
       auto format_count = QString("单词%1出现%2次").arg(iter.key())
               .arg(iter.value());
        qDebug() << format_count;
   }
}
```

## QFile

`QFile` 是 Qt 框架中用于文件操作的类，提供了丰富的功能来读取、写入和操作文件。

使用时需包含头文件

``` cpp
#include <QFile>
#include <QTextStream>
```

QFile为文件操作的类

QTextStream为文本流类，用来绑定一个文本文件，可以更方便的读写文件

文件读写分为文本文件读写和二进制文件读写，

文本文件（text file，textfile，flatfile）: 一般指只有字符原生编码构成的[二进制](https://www.bing.com/search?q=二进制 wikipedia&form=WIKIRE)计算机文件，能够被最简单的[文本编辑器](https://www.bing.com/search?q=文本编辑器 wikipedia&form=WIKIRE)直接读取。

常见的文本文件，cpp等源码文件，txt, doc, md, json以及大部分文本编辑器能直接读取的文件。

二进制文件:  以二进制方式存储的文件，除文本文件外，我们接触到的大部分都是二进制文件。

常见的二进制文件，exe可执行文件, jpeg,jpg等图片文件等。

我们先从文本文件读写开始介绍

### 定义文件

我们在打开文件之前，需要用QFile先指定一个文件

``` cpp
//用QFile绑定一个文件
QFile file("example.txt");
```

### 打开文本文件

可通过open函数打开文本文件，选项为QIODevice::ReadOnly和QIODevice::Text的并集

QIODevice::ReadOnly表示只读

QIODevice::Text表示打开的是文本文件

``` cpp
//用QFile绑定一个文件
QFile file("example.txt");
//以读的方式打开文件
if (!file.open(QIODevice::ReadOnly | QIODevice::Text)) {
    qDebug() << "无法打开文件";
    return;
}
```

因为我们的程序运行目录没有example.txt，所以上面的程序会输出**无法打开文件**

当文件不存在时我们可以以写的方式创建该文件,  上面的代码可以完善为

``` cpp
//用QFile绑定一个文件
QFile file("example.txt");
//以读的方式打开文件
if(!file.open(QIODevice::ReadOnly|QIODevice::Text)){
    qDebug() << "无法打开文件";
    qDebug() << "开始创建文件";
    //以写的方式打开文件
    if(!file.open(QIODevice::WriteOnly|QIODevice::Text)){
        qDebug() << "创建文件失败";
        return;
    }
}
```

### 向文件写入文本

打开文件后，我们需要用一个QTextStream绑定打开的文件，这样可以实现读写

``` cpp
//用QTextStream绑定file
QTextStream out(&file);
//向out写就是向文件写
out << "Hello, QFile!" << endl;
out << "This is a test file." << endl;
//写完关闭文件
file.close();
```

此时我们运行程序，程序输出

``` cpp
无法打开文件
开始创建文件
```

在程序的运行目录创建一个example.txt文件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237982926112.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17237982926112.png)

打开example.txt文件可以看到文件内容

``` bash
Hello, QFile!
This is a test file.
```

### 从文件中读取文本

如果存在文件example.txt，则从文件中读取

QTextStream 有成员函数atEnd用来判断是否读取到文件末尾

``` cpp
bool QTextStream::atEnd() const
```

读取文件内容并打印

``` cpp
//打开成功则读取文本内容
QTextStream in(&file);
//判断文本流是否读取到文件末尾
while(!in.atEnd()){
    //每次读取一行
    auto line = in.readLine();
    qDebug() << line;
}
//读完关闭文件
file.close();
```

程序会输出

``` bash
"Hello, QFile!"
"This is a test file."
```

**练习**

以只读方式打开文件example.txt，如果文件不存在则创建这个文件，并向文件中写入两行数据，如果文件存在，则读取这个文件，并按行打印读取内容。

### 读写方式打开文件

我们可以用读写方式打开一个文件，这样如果文件不存在则自动创建了。

``` cpp
void file_rw(){
    //用QFile绑定一个文件
    QFile file("example.txt");
    //以读的方式打开文件
    if(!file.open(QIODevice::ReadWrite|QIODevice::Text)){
        return;
    }
    file.close();
}
```

如果文件不存在则创建，并且想以追加的方式打开

``` cpp
void file_append(){
    //用QFile绑定一个文件
    QFile file("example.txt");
    //以读的方式打开文件
    if(!file.open(QIODevice::ReadWrite|QIODevice::Append|QIODevice::Text)){
        return;
    }
    file.close();
}
```

### 打开二进制文件

打开二进制文件，只需要设置打开的模式即可，因为是二进制文件，所以不要指定QIODevice::Text

下面我们以读写的方式打开

``` cpp
void write_binary(){
    QFile file("binary.dat");
    if(!file.open(QIODevice::ReadWrite)){
        qDebug() << "无法以只读的方式打开文件";
        return;
    }

    file.close();
}
```

###  向文件写入二进制数据

QFile有成员函数write，可直接向文件中写数据

``` cpp
inline qint64 write(const QByteArray &data);
```

参数为QByteArray, QByteArray是Qt提供的字节数组，常用于一些二进制数据的存储，比如以后给大家讲网络编程时网络传输的字节流，图片的二进制数据，文件的二进制数据等。

我们可以将要写入的数据放入QByteArray中, 然后调用write函数将QByteArray数据写入文件

``` cpp
//将二进制文件放入字节数组
QByteArray data;
data.append(0x01);
data.append(0x02);
data.append(0x03);
//向文件写入二进制数据
file.write(data);
//关闭文件描述符
file.close();
```

执行上述程序会创建文件binary.dat并写入二进制数据

打开文件看到数据

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238038926033.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238038926033.png)

notepad++可以安装插件查看，点击安装

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238037594832.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238037594832.png)

安装后，点击插件View in HEX

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238040723653.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238040723653.png)

此时能看到二进制数据

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238040461426.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17238040461426.png)



练习：

向binary.dat中写入一些二进制数据

### 从文件读取二进制数据

QFile的成员函数readAll能一次性读取文件内容, 

QFile继承自QFileDevice， QFileDevice又继承自QIODevice

readAll是QIODevice的成员函数，所以QFile继承QIODevice也包含了readAll函数

``` cpp
QByteArray QIODevice::readAll()
```

打开binary.dat并读取其中的二进制数据打印出来

``` cpp
void read_binary(){
    QFile file("binary.dat");
    if (!file.open(QIODevice::ReadOnly)) {
        qDebug() << "无法打开文件进行读取";
        return;
    }
    QByteArray data = file.readAll();
    for (char byte : data) {
        qDebug() << "字节:" << static_cast<int>(byte);
    }
    file.close();
}
```

**练习**

以二进制方式打开一张图片，然后用二进制的方式保存为另一个图片文件

**答案**

``` cpp
void copy_pic(){
    QFile file("src.png");
    //以读的方式打开源文件
    if(!file.open(QIODevice::ReadOnly)){
        qDebug() << "无法打开文件进行读取";
        return;
    }
    // 读取二进制数据
    QByteArray data = file.readAll();
    file.close();
    QFile copy_file("copy.png");
    // 以写的方式打开二进制文件
    if(!copy_file.open(QIODevice::WriteOnly)){
        qDebug() << "无法打开文件进行写入";
        return;
    }
    // 写入数据
    copy_file.write(data);
    // 关闭文件描述符
    copy_file.close();
}
```

###  判断文件是否存在

QFile有一个静态成员函数exists，用来判断某个文件是否存在

``` cpp
[static] bool QFile::exists(const QString &fileName)
```

**示例**

``` cpp
if (QFile::exists("example.txt")) {
    qDebug() << "文件存在";
} else {
    qDebug() << "文件不存在";
}
```

### 删除文件

QFile有一个静态成员函数remove,  删除指定文件

``` cpp
[static] bool QFile::remove(const QString &fileName)
```

**示例**

``` cpp
if (QFile::remove("example.txt")) {
    qDebug() << "文件已删除";
} else {
    qDebug() << "无法删除文件";
}
```

### 重命名文件

QFile有一个静态成员函数rename，删除指定文件

``` cpp
[static] bool QFile::rename(const QString &oldName, const QString &newName)
```

**示例**

``` cpp
if (QFile::rename("example.txt", "new_example.txt")) {
    qDebug() << "文件已重命名";
} else {
    qDebug() << "无法重命名文件";
}
```

### 获取文件信息

QFileInfo是获取文件信息的类，通过QFile构造一个QFileInfo变量即可, 使用时需包含<QFileInfo>

``` cpp
QFileInfo::QFileInfo(const QFile &file)
```

**示例**

``` cpp
void file_info(){
    QFile file("example.txt");
    QFileInfo file_info(file);
    qDebug() << "文件名称:" << file_info.fileName();
    qDebug() << "文件大小:" << file_info.size() << "字节";
    qDebug() << "文件路径:" << file_info.absoluteFilePath();
}
```

## QTimer类(待补充)

`QTimer` 是 Qt 提供的一个定时器类，继承自 `QObject`。它允许应用程序在事件循环中安排定时事件，当定时器达到设定的时间间隔后，会触发 `timeout()` 信号。通过连接该信号到相应的槽（Slot），可以实现定时执行特定操作。

主要特点：



- **周期性执行**：设置一个时间间隔，定时器每隔该间隔触发一次。
- **单次执行**：定时器在达到指定时间间隔后只触发一次。
- **集成事件循环**：与 Qt 的事件循环紧密集成，保证定时操作的可靠性。

### 周期性定时器

周期性定时器会在每个时间间隔到达时连续触发，适用于需要定期执行的任务。



**步骤：**



1. 创建 `QTimer` 对象。
2. 连接 `timeout()` 信号到相应的槽函数。
3. 设置时间间隔（以毫秒为单位）。
4. 启动定时器。

**演示案例**

``` cpp
class MyTicker : public QObject
{
    Q_OBJECT
public:
    explicit MyTicker(QObject *parent = nullptr):QObject(parent){
        // 创建定时器
        QTimer *timer = new QTimer(this);

        // 连接 timeout 信号到槽函数
        connect(timer, &QTimer::timeout, this, &MyTicker::onTimeout);

        // 设置时间间隔为1000毫秒（1秒）
        timer->start(1000);
    }

signals:

public slots:
    //定时器每次到时间后执行的槽函数
    void onTimeout(){
        // 定时器触发时执行的代码
        qDebug("定时器触发");
    }
};

```

在main函数中创建一个MyTicker，

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MyTicker ticker;

    MainWindow w;
    w.show();

    return a.exec();
}
```

启动程序后会看到控制台不断输出日志

``` cpp
定时器触发
定时器触发
定时器触发
定时器触发
```

### 单次定时器



单次定时器在指定的时间间隔后只触发一次，适用于需要延迟执行某个操作的场景。



**方法：**



- 使用 `QTimer::singleShot()` 静态函数。

我们自定义一个类，在构造函数里构造一个单次触发的定时器

``` cpp
#include <QObject>
#include <QTimer>
class MySingleShot : public QObject
{
    Q_OBJECT
public:

    MySingleShot(QObject *parent = nullptr) : QObject(parent)
    {
        // 设定延迟时间为2000毫秒（2秒），触发一条消息
        QTimer::singleShot(2000, this, SLOT(onSingleShot()));
    }

signals:

public slots:
    void onSingleShot() {
        // 单次定时器触发时执行的代码
        qDebug("单次定时器触发");
    }
};
```

接下来在main函数中调用

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    
    MySingleShot singleshot;

    MainWindow w;
    w.show();

    return a.exec();
}
```

运行程序后能看到单次触发的定时器只触发了一次。

### 企业中的应用

在 Qt 中，可以使用 `QThread::sleep()` 函数来使当前线程暂停指定的秒数。这个函数是静态的，属于 `QThread` 类。以下是使用 `QThread::sleep()` 的一个简单示例：

``` cpp
#include <QCoreApplication>
#include <QThread>
#include <QDebug>

int main(int argc, char *argv[])
{
    QCoreApplication a(argc, argv);

    qDebug() << "Sleeping for 3 seconds...";
    QThread::sleep(3);  // 暂停3秒
    qDebug() << "Awake!";

    return a.exec();
}
```

请注意，使用这些函数会阻塞当前线程，因此在 GUI 应用程序中使用时要小心，因为它们会导致界面无响应。如果需要在 GUI 应用程序中进行延迟操作，通常可以使用 `QTimer` 来实现。

``` cpp
void Delay_MSec(unsigned int msec)
{
    //定义一个新的事件循环
    QEventLoop loop;
    //创建单次定时器，槽函数为事件循环的退出函数
    QTimer::singleShot(msec, &loop, SLOT(quit()));
    //事件循环开始执行，程序会卡在这里，直到定时时间到，本循环被退出
    loop.exec();
}
```



### 拓展知识

**QTimer 的常用函数**



- **start(int msec)**：启动定时器，时间间隔为 `msec` 毫秒。如果定时器已经在运行，则重启定时器。
- **start()**：启动已经设置了时间间隔的定时器。
- **start(int msec, QObject \*receiver, Pointer to member function)**：启动单次定时器，并在超时时调用指定的槽。
- **stop()**：停止定时器。
- **isActive()**：检查定时器是否处于活动状态。
- **singleShot(int msec, const QObject \*receiver, Pointer to member function)**：启动一个单次定时器。
- **setInterval(int msec)**：设置定时器的时间间隔。
- **interval() const**：获取定时器的时间间隔。



## 元对象系统

Qt 的元对象系统（Meta-Object System）是 Qt 框架的核心特性之一，它支持信号与槽机制、动态属性、反射等功能。元对象系统使得 Qt 能够实现许多高级功能，如动态类型信息、对象树管理、事件处理等。

使用元对象系统需要注意：

- QObject 类是所有使用元对象系统的类的基类。
- 必须在一个类的开头部分插入宏 Q_OBJECT，这样这个类才可以使用元对象系统的特性。

### 信号与槽机制

信号与槽机制是 Qt 的核心特性之一，用于对象之间的通信。信号是由对象发出的事件，槽是处理这些事件的函数。这一节仅作演示说明元对象系统支持信号槽机制，具体的信号和槽知识后续介绍。

#### 定义信号与槽

在类中使用 `signals` 和 `slots` 关键字定义信号和槽：

**切记元对象系统的类必须继承或间接继承自QObject，类的声明里包含Q_OBJECT**

``` cpp
#include <QObject>
#include <QDebug>

class MyObject : public QObject
{
    Q_OBJECT

public:
    MyObject(QObject *parent = nullptr) : QObject(parent) {}
//定义信号
signals:
    void mySignal(int value);
//定义槽函数
public slots:
    void mySlot(int value) {
        qDebug() << "Slot called with value:" << value;
    }
};
```

#### 连接信号与槽

使用QObject::connect 函数将信号连接到槽：

``` cpp
int main(int argc, char *argv[])
{
    QCoreApplication app(argc, argv);

    MyObject obj;
    //连接信号和槽
    QObject::connect(&obj, &MyObject::mySignal, &obj, &MyObject::mySlot);
	//发送信号
    emit obj.mySignal(42); // 发出信号

    return app.exec();
}
```

上述代码输出

``` cpp
Slot called with value: 42
```

### 属性系统

对于元对象类，我们可以通过Qt的属性系统允许在运行时查询和操作对象的属性，这些操作在开发中用的不多，可以了解一下即可。

#### 定义属性

使用 `Q_PROPERTY` 宏定义属性：

我们在MyObject类的声明中添加属性定义

``` cpp
 Q_PROPERTY(int myProperty READ myProperty WRITE setMyProperty NOTIFY myPropertyChanged)
```

上面定义了几个属性：

1.  定义了myProperty属性，为int类型成员变量
2.  定义了myPropery属性 ，为READ函数类型
3.  定义了setPropery属性， 为WRITE函数类型
4.  定义了myPropertyChanged属性,   为NOTIFY类型，也就是信号类型

#### 定义成员函数

接下来定义这些函数和成员, 函数名字需要和Q_PROPERTY中定义的一样

``` cpp
class MyObject : public QObject
{
    Q_OBJECT
    Q_PROPERTY(int myProperty READ myProperty WRITE setMyProperty NOTIFY myPropertyChanged)

public:
    MyObject(QObject *parent = nullptr) : QObject(parent), m_myProperty(0) {}
	//读函数，返回成员m_myPropery的值
    int myProperty() const { return m_myProperty; }
    //写函数, 设置m_myProperty成员
    void setMyProperty(int value) {
        if (m_myProperty != value) {
            m_myProperty = value;
            emit myPropertyChanged(m_myProperty);
        }
    }

signals:
    //信号
    void myPropertyChanged(int value);

private:
    //成员变量
    int m_myProperty;
};
```

#### 属性访问和设置

可在主函数中设置属性值

``` cpp
MyObject obj;
//设置属性值为42
obj.setMyProperty(42);
```

因为我们的MyObject继承了QObject，且类的内部声明了Q_OBJECT, 所以可以将MyObject对象转化为元对象

``` cpp
//返回元对象
const QMetaObject *metaObject = obj.metaObject();
```

元对象可以根据属性名字返回属性所在的索引，因为我们之前定义的属性名为myProperty, 这里获取属性名myProperty所在的索引

``` cpp
//根据属性名字返回属性所在的索引
int propertyIndex = metaObject->indexOfProperty("myProperty");
```

我们可以根据属性索引获取具体的属性对象, 在打印这个属性对象的名字和数值

``` cpp
QMetaProperty metaProperty = metaObject->property(propertyIndex);
//分别打印属性
qDebug() << "Property name:" << metaProperty.name();
qDebug() << "Property value:" << metaProperty.read(&obj).toInt();
qDebug() << "Property value:" << obj.property(metaProperty.name()).toInt();
```

上面的代码输出

``` bash
Property name: myProperty
Property value: 42
Property value: 42
```

#### 动态属性

Qt 允许在运行时动态添加和获取属性：

``` cpp
obj.setProperty("dy_pro",1024);
qDebug() << "dynamic_property is " << obj.property("dy_pro").toInt();
```

上面的代码输出

``` bash
dynamic_property is  1024
```

### 对象树管理

Qt 的对象树管理是通过 `QObject` 类的父子关系实现的。每个 `QObject` 对象可以有一个父对象和多个子对象，这种层次结构被称为对象树。对象树管理提供了一种方便的方式来管理对象的生命周期和层次结构。

#### 核心概念

1. **父对象和子对象**：
   - 每个 `QObject` 对象可以有一个父对象和多个子对象。父对象负责管理子对象的生命周期，当父对象被销毁时，所有子对象也会被销毁。
2. **树状结构**：
   - `QObject` 对象的父子关系形成了一棵树。根对象没有父对象，所有其他对象都有一个唯一的父对象。
3. **自动销毁**：
   - 当一个对象被销毁时，它的所有子对象也会被自动销毁。这种机制有助于避免内存泄漏。



我们可以构造如下图的对象树

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240410098255.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240410098255.png)

#### 代码演示

我们可以定义一个类TreeObj表示对象树的类

``` cpp
class TreeObj: public QObject
{
    Q_OBJECT
public:
    TreeObj(const QString& name, QObject* parent = nullptr)
        : QObject(parent){
        setObjectName(name);
    }

    ~TreeObj(){
        qDebug() << QString("call %1 destruction ").arg(objectName());
    }
};
```

1. setObjectName 为QObject的函数，主要用来设置对象名称。
2. TreeObj构造函数接受一个字符串和父节点，字符串表示对象名称，父节点用来构造基类QObject。

我们写一个函数，构造一个父节点Parent，在父节点下面构造Child1和Child2，然后又在Child1下构造Grandchild1和Grandchild2.

``` cpp
void object_tree(){
    auto parent = new TreeObj("Parent");
    auto child1 = new TreeObj("Child1",parent);
    auto child2 = new TreeObj("Child2",parent);
    auto grand_child1 = new TreeObj("Grandchild1",child1);
    auto grand_child2 = new TreeObj("Grandchild2",child1);
    qDebug() << QString("parent has %1 children  ")
                .arg(parent->children().count());
    qDebug() << QString("child1 has %1 children  ")
                .arg(child1->children().count());
}
```

上面的函数输出

``` cpp
"parent has 2 children  "
"child1 has 2 children  "
```

因为三个对象都是new出来的，按道理应该手动delete回收，但是有元对象系统，我们只需要delete最上层的父节点，他的所有子节点，以及子节点的孩子都会被回收

``` cpp
delete parent;
```

执行删除后，程序输出如下

``` bash
"call Parent destruction "
"call Child1 destruction "
"call Grandchild1 destruction "
"call Grandchild2 destruction "
"call Child2 destruction "
```

可以看到所有子节点自动被回收了，因为对象树机制自动管理子节点的生命周期会随着父节点的结束而结束。

### 类型转换

qobject_cast 是 Qt 框架提供的一个类型转换函数，专门用于在 QObject 类及其派生类之间进行安全的类型转换。它类似于 C++ 标准库中的 dynamic_cast，但仅适用于 QObject 类型。

qobject_cast 使用 Qt 的元对象系统（Meta-Object System）来进行运行时检查(包括信号，属性等)，以确保转换的安全性。如果转换失败，它会返回 nullptr。

``` cpp
void qobject_cast(){
    BaseClass *base = new DerivedClass;
    //基类指针转化为子类指针
     DerivedClass *derived = qobject_cast<DerivedClass*>(base);
     if (derived) {
         qDebug() << "qobject_cast succeeded";
     } else {
         qDebug() << "qobject_cast failed";
     }
     delete base;
}
```

上面的代码会输出

``` bash
"qobject_cast succeeded"
```

### 总结

学了这么多，上面的大家只做概念理解即可，不需要写出完整代码，**面试时常问的两个问题**

1. 如何实现一个类，使其支持元对象系统（继承自QObject, 类的声明包含Q_OBJECT宏）
2. 元对象系统有哪些特性？（信号和槽，属性系统，对象树管理，qobject_cast类型转换）

## 信号和槽详解

信号和槽机制在元对象系统时简单介绍并使用了，这里详细介绍，包括：

1. 信号和槽的定义
2. 如何连接信号和槽
3. 信号和槽的参数匹配规则
4. 一个信号连接多个槽函数
5. 连接信号和信号
6. 信号和槽的几种连接方式
7. 发送信号

#### 信号和槽的定义

信号需要声明在signals关键字下面

``` cpp
ClassA {
  signals:
    void mySignal(int value);
    void myPropertyChanged(int value);  
}
```

信号的定义包括 信号的返回类型，一般都是void，信号的名字，以及信号携带的参数。

例如mySignal这个信号返回类型为void，参数为int类型。

**信号不需要写实现逻辑**

槽函数的声明放在slots关键字下面，但是槽函数有权限控制，有的槽函数是公有的，有的是私有的，有的是受保护的。

槽函数返回类型一般为void，也可以携带参数。

``` cpp
ClassA {
public slots:
	void publicSlot(int value);
protected slots:
	void protectedSlot(int value);
private slots:
	void privateSlot(int value);
}
```

**槽函数需要写实现逻辑**

``` cpp
void ClassA::publicSlot(int value)
{
    qDebug()<<"called public slot, value is " << value;
}

void ClassA::protectedSlot(int value)
{
    qDebug()<<"called protected slot, value is " << value;
}

void ClassA::privateSlot(int value)
{
    qDebug()<<"called private slot, value is " << value;
}
```

关于访问控制，私有的槽函数只能在其所属的类中连接，比如privateSlot只能在ClassA的函数中连接

比如我们将私有的槽函数和信号连接逻辑放在ClassA的构造函数里

``` cpp
ClassA::ClassA()
{
    //在构造函数中连接自己的信号和槽函数
    connect(this,&ClassA::mySignal,this,&ClassA::privateSlot);
}
```

#### 如何连接信号和槽

连接信号和槽的写法基本如下

``` cpp
connect(sender, &SenderType::signalName, receiver, &ReceiverType::slotName);
```

翻译过来就是

``` cpp
connect(信号发出者的指针，信号的指针，接收者的指针，槽函数的指针)
```

可以在任何函数,   连接ClassA的信号和公有槽函数

``` cpp
void con_sig_slot(){
    ClassA ca;
    //连接ca的mySignal信号和ca的publicSlot槽
    QObject::connect(&ca, &ClassA::mySignal, &ca, &ClassA::publicSlot);
}
```

**练习**

练习一下，写一下信号和槽连接的代码

**注意**

在普通函数和main函数中连接信号和槽，需要使用QObject::connect, 需显示值明使用的是QObject下的connect信号。

如果在支持了元对象系统(1 继承了QObject， 2 声明了Q_OBJECT宏 ) 的类里连接信号和槽，可以直接使用connect进行连接。

**注意**

部分公司信号和槽的连接写法采用QT4版本之前的写法,使用 `SIGNAL` 和 `SLOT` 宏：

``` cpp
connect(sender, SIGNAL(signalName()), receiver, SLOT(slotName()));
```

``` cpp
void con_sig_slot_v4(){
    ClassA ca;
    //连接ca的mySignal信号和ca的publicSlot槽
    QObject::connect(&ca, SIGNAL(mySignal()), &ca, SLOT(publicSlot()));
}
```

这种写法不推荐，编译器不做检测，很多错误在运行时才爆发，很危险。

**C++11 风格**

qt信号和槽也支持C++11风格连接

``` cpp
connect(sender, &SenderType::signalName, [=]() {
    // Lambda 表达式中的代码
});
```

例如

``` cpp
void con_sig_slot_v4(){
    ClassA ca;
    //连接ca的mySignal信号和ca的publicSlot槽
    QObject::connect(&ca, SIGNAL(mySignal()), [=](){
        //Lambda 表达式
    });
}
```



#### 信号和槽函数匹配规则

在 Qt 的信号和槽机制中，信号的参数可以比槽函数的参数多，但必须满足以下条件：

1. **参数类型和顺序匹配**：槽函数的参数类型和顺序必须与信号的前几个参数类型和顺序一致。
2. **参数数量**：槽函数的参数数量必须小于或等于信号的参数数量。

**示例**

我们能对ClassA 新增一个携带多个参数的信号paramSignal和一个处理多个参数的槽函数paramSlot

``` cpp
class ClassA:public QObject
{
    Q_OBJECT
public:
    ClassA();
signals:
    void paramSignal(int value, QString str, double dvalue);
public slots:
    void paramSlot(int value, QString str);
};
```

因为paramSlot的参数比paramSignal的参数少，但是槽函数的参数类型和信号的前几个参数类型顺序一致，所以可以连接

``` cpp
void con_param_sig_slot(){
    ClassA ca;
    //连接ca的paramSignal信号和ca的paramSlot槽
    QObject::connect(&ca, &ClassA::paramSignal, &ca, &ClassA::paramSlot);
}
```

#### 一个信号匹配多个槽函数

一个信号可以连接到多个槽函数,   比如我们的类中声明并定义了多个槽函数和信号

``` cpp
class ClassA:public QObject
{
    Q_OBJECT
public:
    ClassA();
signals:
    void mySignal(int value);
    void mySignal2(int value);
public slots:
    void publicSlot(int value);
    void publicSlot2(int value);
};
```

我们可以让信号mySignal连接到publicSlot和publicSlot2

``` cpp
void con_sig_mulslots(){
    ClassA ca;
    //一个信号连接多个槽
    QObject::connect(&ca, &ClassA::mySignal, &ca, &ClassA::publicSlot);
    QObject::connect(&ca, &ClassA::mySignal, &ca, &ClassA::publicSlot2);
}
```

#### 连接信号和信号

信号可以连接信号，将消息转发给其他信号

``` cpp
void con_sig_sig(){
    ClassA ca;
    //一个信号连接另一个信号
    QObject::connect(&ca, &ClassA::mySignal, &ca, &ClassA::mySignal2);
}
```



#### 信号和槽的几种连接方式

在 Qt 中，信号和槽的连接方式有几种不同的模式，分别是默认模式（`Qt::AutoConnection`）、直接连接（`Qt::DirectConnection`）、队列连接（`Qt::QueuedConnection`）、阻塞连接（`Qt::BlockingQueuedConnection`）以及唯一连接（`Qt::UniqueConnection`）。这些连接方式决定了槽函数在哪个线程中被调用。以下是每种连接方式的详细说明：

1. 默认模式（`Qt::AutoConnection`）

在连接信号和槽时，我们不写具体的连接方式，

说明：

- **行为**：默认模式下，Qt 会根据信号和槽所在的线程自动选择连接方式。如果信号和槽在同一个线程中，使用直接连接；如果信号和槽在不同线程中，使用队列连接。
- **槽函数线程**：如果信号和槽在同一个线程中，槽函数在发送信号的线程中调用。如果信号和槽在不同线程中，槽函数在接收信号的对象所属的线程中调用。

示例：

``` cpp
QObject::connect(sender, &Sender::signal, receiver, &Receiver::slot, Qt::AutoConnection);
```

2. 直接连接（`Qt::DirectConnection`）

说明：

- **行为**：信号发出时，槽函数立即在发出信号的线程中被调用。
- **槽函数线程**：槽函数在发送信号的线程中调用。

示例：

```cpp
QObject::connect(sender, &Sender::signal, receiver, &Receiver::slot, Qt::DirectConnection);
```

3. 队列连接（`Qt::QueuedConnection`）

说明：

- **行为**：信号发出时，槽函数调用被放入接收对象所在线程的事件队列中，槽函数将在接收对象的线程中被调用。
- **槽函数线程**：槽函数在接收信号的对象所属的线程中调用。

示例：

``` cpp
QObject::connect(sender, &Sender::signal, receiver, &Receiver::slot, Qt::QueuedConnection);
```

4. 阻塞连接（`Qt::BlockingQueuedConnection`）

说明：

- **行为**：信号发出时，槽函数调用被放入接收对象所在线程的事件队列中，且发送信号的线程会阻塞，直到槽函数执行完毕。仅在多线程环境下有效。
- **槽函数线程**：槽函数在接收信号的对象所属的线程中调用。

示例

``` cpp
QObject::connect(sender, &Sender::signal, receiver, &Receiver::slot, Qt::BlockingQueuedConnection);
```

5. 唯一连接（`Qt::UniqueConnection`）

说明：

- **行为**：确保信号和槽之间只有一个连接。如果尝试创建重复连接，连接操作会失败。可以与其他连接类型组合使用。
- **槽函数线程**：根据与其他连接类型组合使用的结果确定。

示例

``` cpp
QObject::connect(sender, &Sender::signal, receiver, &Receiver::slot, Qt::UniqueConnection | Qt::AutoConnection);
```

以上连接方式不用过多关注，实际开发采用默认连接即可，面试会问到信号和槽的连接方式。

#### 发送信号

发送信号使用emit 关键字，后面跟信号即可

``` cpp
void emit_sig(){
    ClassA ca;
    emit ca.mySignal(100);
    emit ca.paramSignal(1024,"hello hema",3.14);
}
```

#### 练习

定义一个类ClassA，ClassA包含一个信号sigNotify, 参数为(QString , int)类型。

定义一个类ClassB，ClassB包含一个公有的槽函数slotNofiy, 参数为(QString , int)， slotNotify 打印收到的信息

实现函数nofity_func,   函数内部分别定义ca对象(Class A类型)以及cb对象(Class B类型)，连接ca的sigNotify和cb的slotNotify。

并且发送ca的sigNotify,  测试cb的槽函数是否触发。

**答案**

分别定义ClassA和ClassB

``` cpp
class ClassA:public QObject
{
    Q_OBJECT
public:
    ClassA();
signals:
    void sigNotify(QString name, int year);
};
```

classB

``` cpp
class ClassB: public QObject{
    Q_OBJECT
public:
    ClassB(){}
public slots:
    void slotNotify(QString name, int year);
};

void ClassB::slotNotify(QString name, int year)
{
    qDebug() << "slotNotify called, name is " << name
             << " year is " << year;
}
```

定义函数连接并发送信号

``` cpp
void con_ca_cb(){
    ClassA ca;
    ClassB cb;
    QObject::connect(&ca, &ClassA::sigNotify, &cb, &ClassB::slotNotify);
    emit ca.sigNotify("zack",28);
}
```

main函数调用con_ca_cb会看到程序输出

``` cpp
slotNotify called, name is  "zack"  year is  28
```



# 第三章 常用界面组件类

## GUI控件类

### QWidget简介

所有界面组件类的直接或间接父类都是 QWidget。QWidget 的父类是 QObject 和 QPaintDevice，所以 QWidget 是多重继承的类。



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240611525315.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240611525315.png)



QObject 支持元对象系统，其信号与槽机制为 GUI 编程中对象间通信提供了极大的便利。

QPaintDevice 是能使 QPainter 类在绘图设备上绘图的类。

我们可以新建一个Qt Widgets Application项目， 名字叫做01-QMainWindows

创建成功后，双击mainwindow.ui文件， 进入Designer界面。



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241139784074.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241139784074.png)

1. 红框1主要是控件区，包括常用的控件都罗列在这里。
2. 绿框2主要是ui的布局区，可以拖动部件调整在布局中的位置，程序运行后会按照布局设计的样式展示。
3. 黄框3主要是ui对象层级管理区，主要展示各个对象之间的层级关系。
4. 篮筐4主要是属性编辑区，可以设计



我们在ui区可以看到MainWindow界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724062534616.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724062534616.png)







我们观察QtDesigner界面左侧控件区, 会看到QWidget在Containers里，因为QWidget属于容器类型

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240615781940.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17240615781940.png)

大家可以直接拖动designer中的widget放入MainWindow界面里

然后在右侧的对象层级管理区能看到我们新增的widget

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241147098472.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241147098472.png)

为了方便展示我们新增的widget，点击右侧对象层级管理中的widget，去右下方的属性管理器找到stylesheet样式表

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241149227829.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241149227829.png)

点击右侧的小三角弹出编辑样式表，这个样式表就是设置控件样式的，包括颜色，大小等。我们添加背景颜色为绿色

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241151441143.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241151441143.png)



点击ok保存，再次运行

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241161718716.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241161718716.png)

这是最简单的利用Designer拖动实现界面创建的方式。

### QWidget基本接口

#### 显示和隐藏



- `show()`：显示窗口。
- `hide()`：隐藏窗口。
- `close()`：关闭窗口。

#### 代码创建

我们也可通过代码创建一个widget，在main函数中将MainWindow展示逻辑去掉，替换成创建widget然后展示出来。

 **示例**

展示一个窗口， 大家可以在main函数中创建这个QWidget，并展示出来，这是通过代码创建QWidget的方式。

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    QWidget widget;
    widget.show();
    return a.exec();
}
```

#### 大小和位置

- `resize(int width, int height)`：调整窗口大小。
- `move(int x, int y)`：移动窗口到指定位置。
- `setGeometry(int x, int y, int width, int height)`：设置窗口的几何属性。
- `size()`：返回窗口的大小。
- `pos()`：返回窗口的位置。

**练习**

我们重新设置widget大小为800*600

将窗口移动到(100,100)位置

并且将窗口展示出来

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    QWidget widget;
    //重新设置大小为800*600
    widget.resize(800,600);
    //移动到(100,100)位置
    widget.move(100,100);
    widget.show();
    return a.exec();
}
```

### 添加资源文件

我们的一些界面会带有图标，为了添加图标，右键刚才创建的MainWindow项目弹出的菜单选择AddNew

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241204623591.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241204623591.png)

选择Qt Resource

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724120919541.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724120919541.png)

为资源文件命名为qrc

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241210221651.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241210221651.png)

选择添加到项目

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241211784380.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241211784380.png)



在项目目录里创建res文件夹，添加两个文件new.png和open.png

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241213111869.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241213111869.png)



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241214468439.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241214468439.png)

右键项目左侧目录数Resources下的qrc.qrc,  添加现有文件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241216932418.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241216932418.png)



在文件目录中选择我们刚才添加的图片文件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241218064145.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241218064145.png)

点击确定之后，可以看到项目结构目录下qrc文件下增加了图片资源

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241220334425.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241220334425.png)

**练习**

将图片资源添加到项目中

#### 使用资源

如果以后想要使用资源，可以右键对应的图片，在弹出的菜单选择copy path即可

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241222667525.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241222667525.png)



代码中可以直接写这个路径作为资源路径进行加载

### QMainWindow

QMainWindow是主窗口类，我们创建一个Qt Widgets Application项目，Qt Creator默认为我们生成的就是继承自QMainWindow的界面类并展示出来。

下图为QMainWindow的结构示意图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241174198414.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241174198414.png)

我们看下层级管理，

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241179388149.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241179388149.png)

能看到几个控件

1. menuBar 菜单栏
2. mainToolBar 工具栏
3. centralWidget 为中心控件
4. widget为我们刚才添加的widget控件
5. statusBar为状态栏

#### 创建菜单

创建菜单可以通过ui创建，但是不够灵活，现在企业基本采用代码创建. 

有时候MainWindow中没有菜单栏，可以通过ui添加，但不推荐，我们直接通过代码创建菜单栏，并将菜单栏设置到MainWindow中。

QMenuBar的构造函数接受一个QWidget作为其父节点

``` cpp
QMenuBar(QWidget *parent = nullptr)
```

MainWindow 设置菜单栏的接口

``` cpp
void QMainWindow::setMenuBar(QMenuBar *menuBar)
```

我们在MainWindow的构造函数中添加菜单栏

``` cpp
//设置窗口标题
this->setWindowTitle("myWindow");
//重设窗口大小
this->resize(1100,700);
//创建菜单栏
QMenuBar *menuBar = new QMenuBar(this);
//添加菜单栏到主窗口中
this->setMenuBar(menuBar);

```

QMenu构造函数有两个，可接受文本作为菜单的名字。

``` cpp
QMenu(QWidget *parent = nullptr)
QMenu(const QString &title, QWidget *parent = nullptr)
```

**练习**

接下来我们创建三个一级菜单(文件，编辑，构建)并添加到菜单栏里

``` cpp
//创建文件菜单
QMenu *menu1 = new QMenu("文件",this);
//创建编辑菜单
QMenu *menu2 = new QMenu("编辑",this);
//创建构建菜单
QMenu *menu3 = new QMenu("构建",this);
//将菜单添加到菜单栏
menuBar->addMenu(menu1);
menuBar->addMenu(menu2);
menuBar->addMenu(menu3);
```

再次运行可看到窗口里添加了菜单栏

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241187032101.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241187032101.png)

#### 添加菜单项

菜单项在Qt中叫做QAction,  QAction包含三种构造参数

``` cpp
//接受一个参数，父节点
QAction(QObject *parent = nullptr)
//接受两个参数，菜单项的名字和其父节点
QAction(const QString &text, QObject *parent = nullptr)
//接受三个参数，菜单项的图标，菜单项的名字，父节点
QAction(const QIcon &icon, const QString &text, QObject *parent = nullptr)
```

QIcon的构造传入图片路径即可构造一个图标

``` cpp
QIcon(const QString &fileName)
```

QMenu添加菜单项的接口

``` cpp
void QMenu::addAction(Action *action)
```

QMenu可以为菜单项设置分割符

``` cpp
QAction *QMenu::addSeparator()
```



**练习**

在新建菜单下添加菜单项，名字为“新建文件或项目”

在新建菜单下添加菜单项，名字为“打开文件或项目”

在新建菜单下添加分隔符，分隔符下添加菜单项，名字为退出

可以配合前面添加到资源文件为菜单项设置图标

实现如下效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724123017347.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724123017347.png)



**答案**

``` cpp
//创建菜单栏
QMenuBar *menuBar = new QMenuBar(this);
//添加菜单栏到主窗口中
this->setMenuBar(menuBar);

//创建文件菜单
QMenu *menu1 = new QMenu("文件",this);
//创建编辑菜单
QMenu *menu2 = new QMenu("编辑",this);
//创建构建菜单
QMenu *menu3 = new QMenu("构建",this);
//将菜单添加到菜单栏
menuBar->addMenu(menu1);
menuBar->addMenu(menu2);
menuBar->addMenu(menu3);
//创建新建菜单项
auto new_action = new QAction(QIcon(":/res/new.png"),"新建文件或项目",this);
//创建打开菜单项
auto open_action = new QAction(QIcon(":/res/open.png"),"打开文件或项目",this);
//创建退出菜单项
auto exit_action = new QAction("退出",this);
//添加新建菜单项
menu1->addAction(new_action);
//添加打开菜单项
menu1->addAction(open_action);
//添加分割符
menu1->addSeparator();
//添加退出菜单项
menu1->addAction(exit_action);
```

#### 菜单项添加快捷键

我们可以通过QAction的函数setShortcut为菜单项添加快捷键

``` cpp
void setShortcut(const QKeySequence &shortcut)
```

QKeySequence构造函数接受按键组成的宏，比如快捷键Ctrl+N

``` cpp
action1->setShortcut(QKeySequence(Qt::CTRL + Qt::Key_N));
```

**练习**

为新建文件菜单项添加快捷键Ctrl+N, 为打开文菜单项添加快捷键Ctrl+O

**答案**

``` cpp
//设置快捷键 ctrl + n
new_action->setShortcut(QKeySequence(Qt::CTRL+Qt::Key_N));
//设置快捷键 ctrl + o
open_action->setShortcut(QKeySequence(Qt::CTRL+Qt::Key_O));
```

#### 菜单项添加触发槽函数

当菜单项被选中或者按下快捷键触发时会执行相应的逻辑，比如新建项目被点击后，执行新建项目的操作。

点击菜单项会触发菜单项发出triggered信号

``` cpp
[signal] void QAction::triggered(bool checked = false)
```

我们可以在MainWindow写一个槽函数，接受这个信号，并简单的弹出一个提示框做提示

#### QMessageBox

Qt 提示框的类为QMessageBox，QMessageBox提供了几个不同类型的对话框

**信息消息框**

```cpp
QMessageBox::information(this, "Information", "This is an information message.");
```

**警告消息框**

```cpp
QMessageBox::warning(this, "Warning", "This is a warning message.");
```

**错误消息框**

```cpp
QMessageBox::critical(this, "Critical", "This is a critical error message.");
```

**问题消息框**

有时候提示框会提出问题，让用户选择确认还是取消，可以用问题消息框。

```cpp
QMessageBox::StandardButton reply;
reply = QMessageBox::question(this, "Question", "Do you want to continue?", QMessageBox::Yes | QMessageBox::No);
if (reply == QMessageBox::Yes) {
    // User clicked Yes
} else {
    // User clicked No
}
```

**练习**

为新建文件或项目这个菜单项添加点击后弹出信息消息框，提示“点击了创建文件或项目”

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241264721959.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241264721959.png)

**答案**

MainWindow中添加槽函数

``` cpp
void MainWindow::slotNewFile()
{
    QMessageBox::information(this,"通知","点击了新建文件或项目菜单");
}
```

在MainWindow的构造函数中连接新建菜单项和槽函数

``` cpp
//连接新建项目的菜单项的信号和mainwindow槽函数
connect(new_action, &QAction::triggered,this, &MainWindow::slotNewFile);
```



#### 工具栏

**添加工具栏**

工具栏和菜单栏类似，如果ui文件中没有工具栏，我们可以用ui文件中的工具栏添加工具项。

否则我们需要先创建工具栏

``` cpp 
//创建工具栏
auto tool_bar = new QToolBar(this);
//主窗口添加工具栏
this->addToolBar(tool_bar);
```

**添加工具项**

工具项和菜单项一样，都是QAction类型所以添加工具项很简单

添加工具项

``` cpp
//创建工具项
auto tool_new = new QAction(QIcon(":/res/new.png"),"新建",this);
auto tool_open = new QAction(QIcon(":/res/open.png"),"打开",this);
//添加工具项
tool_bar->addAction(tool_new);
tool_bar->addAction(tool_open);
//添加分割符号
tool_bar->addSeparator();
auto tool_exit = new QAction("退出",this);
//添加退出工具项
tool_bar->addAction(tool_exit);
```

#### 状态栏

如果主窗口的ui里没有状态栏，需要创建。和之前菜单栏，工具栏类似，创建好状态栏再设置到主窗口中。

``` cpp
    //创建状态栏
    QStatusBar *status = new QStatusBar(this);
    status->setObjectName("状态栏");
    //设置不显示label的边框
    status->setStyleSheet("QStatusBar::item{border: 0px}");
    //主窗口添加状态栏
    this->setStatusBar(status);
```

样式表也可以在代码中设置，我们之前是通过ui设置的。

状态栏可以设置标签，

``` cpp
//创建标签
QLabel *statusLabel = new QLabel("我是状态栏", this);

//状态栏添加信息
//显示在左侧，并且3秒后自动消失
status->showMessage("我在3秒后会消失", 3000);
//添加右侧标签(永久性)
status->addPermanentWidget(statusLabel);
```

**练习**

练习实现状态栏

### 组件划分

按照Qt Designer中提供的不同功能分区，组件大体包括

- 按钮类

  - QPushButton
  - QToolButton
  - QRadioButton
  - QCheckBox

- 输入类

  - QLineEdit
  - QTextEdit
  - QPlainTextEdit
  - QDateEdit
  - QTimeEdit
  - QSPinBox
  - QComboBox

- 显示类

  - QLabel
  - QGraphicsView
  - QProgressBar

- 容器类

  - QWidget
  - QScrollArea
  - QFrame
  - QListWidget
  - QTableWidget
  - QTreeWidget

  

大家可以在Designer中拖动上述组件感受下都是什么，因为QT组件过于庞杂，接下来按照分类挑选常用的介绍

### 按钮类

#### QPushButton 

QPushButton是Qt提供的基础按钮类，可以设置按钮的文本，图标，快捷键等。

QPUshButton的三个构造函数

``` cpp
//一个参数指定父节点
QPushButton(QWidget *parent = nullptr);
//指定显示文本和父节点
QPushButton(const QString &text, QWidget *parent = nullptr);
//指定图标，显示文本，以及父节点
QPushButton(const QIcon &icon, const QString &text, QWidget *parent = nullptr);
```

我们通过代码的方式创建QPushButton并且显示在MainWindow上, 在MainWindow的构造函数里添加

``` cpp
//创建按钮，显示文本
QPushButton *button = new QPushButton("Click Me", this);
//为按钮设置图标
button->setIcon(QIcon(":/res/open.png"));
//设置按钮的位置和大小
button->setGeometry(100, 100, 100, 40);
```

setGeometry四个参数分别为按钮所在横坐标，按钮所在纵坐标，按钮宽度，按钮的高度等。

运行后可显示按钮

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241360141836.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241360141836.png)

按钮被点击后会发出clicked信号

``` cpp
void  clicked(bool checked = false)
```

**练习**

我们可以在MainWindow写一个槽函数slotBtnClick，捕获这个信号，然后弹出消息框显示”按钮被点击“

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241366264633.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241366264633.png)

**答案**

为MainWindow类添加槽函数

``` cpp
void MainWindow::slotBtnClick()
{
    QMessageBox::information(this,"通知","点击了按钮");
}
```

在MainWindow构造函数中连接按钮点击信号和MainWindow槽函数

``` cpp
connect(button, &QPushButton::clicked,this, &MainWindow::slotBtnClick);
```

#### QToolButton

`QToolButton` 是 Qt 框架中用于创建工具按钮的类。工具按钮通常用于工具栏或其他需要紧凑按钮布局的地方。与标准的 `QPushButton` 不同，`QToolButton` 通常更小，并且可以只显示图标、只显示文本或同时显示图标和文本。 使用时需包含QToolButton头文件

QToolButton的构造函数仅有一个参数

``` cpp
QToolButton(QWidget *parent = nullptr)
```

QToolButton同样支持设置现实的图标和文本

``` cpp
//创建一个工具按钮
QToolButton *toolButton = new QToolButton(this);
//设置图标
toolButton->setIcon(QIcon(":/res/new.png"));
//设置文本
toolButton->setText("Tool");
```

工具按钮可以设置几种显示样式

``` cpp
// 仅显示图标
toolButton->setToolButtonStyle(Qt::ToolButtonIconOnly); 
 // 仅显示文本
toolButton->setToolButtonStyle(Qt::ToolButtonTextOnly);
// 图标在文本旁边
toolButton->setToolButtonStyle(Qt::ToolButtonTextBesideIcon); 
// 图标在文本上方
toolButton->setToolButtonStyle(Qt::ToolButtonTextUnderIcon);  
```

工具按钮可以放在工具栏里

``` cpp
//创建一个工具按钮
QToolButton *toolButton = new QToolButton(this);
//设置图标
toolButton->setIcon(QIcon(":/res/new.png"));
//设置文本
toolButton->setText("Tool");
 //设置按钮样式，文本在图标旁边
 toolButton->setToolButtonStyle(Qt::ToolButtonTextBesideIcon);
//工具栏添加按钮
tool_bar->addWidget(toolButton);
```

**QToolButton按钮被点击后也会发出clicked信号**。

#### 练习

创建一个QToolButton，放在工具栏里，按钮样式为Qt::ToolButtonTextBesideIcon。

点击按钮后，弹出消息框显示”ToolButton被点击了“

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241394133446.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241394133446.png)



**答案**

MainWindow构造函数里添加

``` cpp
//创建一个工具按钮
QToolButton *toolButton = new QToolButton(this);
//设置图标
toolButton->setIcon(QIcon(":/res/new.png"));
//设置文本
toolButton->setText("Tool");
//设置按钮样式，文本在图标旁边
toolButton->setToolButtonStyle(Qt::ToolButtonTextBesideIcon);
//按钮添加到工具栏上
tool_bar->addWidget(toolButton);

//连接按钮的点击信号
connect(toolButton,&QToolButton::clicked,this, &MainWindow::slotToolBtnClick);
```

MainWindow添加槽函数

``` cpp
void MainWindow::slotToolBtnClick()
{
    QMessageBox::information(this,"通知","点击了工具按钮");
}
```

#### QRadioButton

QRadioButton为单选按钮，后续我们通过例子来演示和学习。这里大家可以拖动Designer中的QRadioButton到MainWindow.ui中，看看QRadioButton的样子

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241409584314.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241409584314.png)

#### QCheckBox

QCheckBox为多选框,  大家可以添加到ui，启动程序看看样式

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724141331760.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724141331760.png)

### 输入类控件

#### QLineEdit

QLineEdit主要是用来单行输入的控件，大家可以将一个QLineEdit拖动到ui里, 运行后看看效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241417163857.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241417163857.png)

QLineEdit有几个信号介绍一下

``` cpp
//光标位置变化后发送信号
void  cursorPositionChanged(int oldPos, int newPos)
//编辑完成后发送，失去光标时发送
void  editingFinished()
//输入被拒绝时发出这个信号
void  inputRejected()
//按下回车键后
void  returnPressed()
//选择区域变化后
void  selectionChanged()
//文本变化后
void  textChanged(const QString &text)
//文本被编辑
void  textEdited(const QString &text)

```

这些信号不用死记硬背，用到的时候查下assistant手册或者AI都可以，会用就行

QLineEdit也支持设置输入的模式

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241427818662.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241427818662.png)

Normal 就是输入的内容正常显示

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436801485.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436801485.png)

NoEcho就是输入的内容完全不显示，输入什么都是一片空白

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241437541500.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241437541500.png)

Password就是以密码点的形式显示

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436491630.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436491630.png)

PasswordEchoOnEdit就是输入的时候显示字符，失去焦点后变成密码点

在输入时是这样

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436801485.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436801485.png)

失去焦点

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436491630.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241436491630.png)

通过setEchoMode可以设置输入模式

``` cpp
void setEchoMode(QLineEdit::EchoMode)

```



我们做个练习看看效果

**练习**

MainWindow上添加一个QLineEdit，设置输入模式为Password. 当输入完成后打印输入的密码

**答案**

mainwindow的构造函数里添加

``` cpp
//设置为密码输入模式
ui->lineEdit->setEchoMode(QLineEdit::Password);
//连接失去焦点信号和槽函数
connect(ui->lineEdit, &QLineEdit::editingFinished, [this](){
    qDebug() << "editing Finished slot";
});

//连接按下回车信号和槽函数
connect(ui->lineEdit, &QLineEdit::returnPressed, [this](){
    qDebug() << "returnPressed slot";
});
```

#### QTextEdit

文本编辑器，和QLineEdit一样，都是输入控件，QTextEdit支持多行输入。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241452217945.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241452217945.png)

#### QTextPlainEdit

QTextPlainEdit为纯文本编辑器，和QTextEdit功能类似，不做赘述

#### QDateEdit

QDateEdit是编辑日期的控件，拖动到ui运行可查看到

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241458969058.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17241458969058.png)

QDateEdit支持设置日期

``` cpp
QDateEdit *dateEdit = new QDateEdit(this);
dateEdit->setDate(QDate::currentDate());  // 设置为当前日期
```

获取日期

``` cpp
QDate selectedDate = dateEdit->date();
qDebug() << "Selected date:" << selectedDate.toString();
```

设置日期展示样式

``` cpp
dateEdit->setDisplayFormat("yyyy-MM-dd");
```

信号和槽

`QDateEdit` 提供了一些信号，例如 `dateChanged` 信号，当日期发生变化时会发出该信号。可以连接到槽函数来处理日期变化事件：

``` cpp
//连接日期变化信号
connect(dateEdit, &QDateEdit::dateChanged, this, &MainWindow::onDateChanged);
//日期变化的槽函数
void MainWindow::onDateChanged(const QDate &date) {
    qDebug() << "New date selected:" << date.toString();
}
```

#### QTimeEdit

QTimeEdit和QDateEdit用法类似

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724146702313.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724146702313.png)

#### QSpinBox

`QSpinBox` 是 Qt 框架中的一个控件，用于显示和编辑整数值。它提供了一个带有上下按钮的输入框，用户可以通过点击按钮或直接输入来更改数值。以下是 `QSpinBox` 的常见用法和示例。

**基本用法**

创建一个 `QSpinBox` 控件

```cpp
QSpinBox *spinBox = new QSpinBox(this);
```

**设置初始值**

可以使用 `setValue` 方法来设置 `QSpinBox` 的初始值：

```cpp
spinBox->setValue(10);
```

**获取当前值**

可以使用 `value` 方法来获取当前的数值：

```cpp
int currentValue = spinBox->value();
qDebug() << "Current value:" << currentValue;
```

**设置数值范围**

可以使用 `setMinimum` 和 `setMaximum` 方法来设置允许的数值范围：

```cpp
spinBox->setMinimum(0);  // 最小值为0
spinBox->setMaximum(100); // 最大值为100
```

或者，使用 `setRange` 方法同时设置最小值和最大值：

```cpp
spinBox->setRange(0, 100);
```

**设置步长**

可以使用 `setSingleStep` 方法来设置每次点击上下按钮时数值的变化步长：

```cpp
spinBox->setSingleStep(5);  // 每次增加或减少5
```

**设置前缀和后缀**

可以使用 `setPrefix` 和 `setSuffix` 方法来设置显示在数值前后的文本：

```cpp
spinBox->setPrefix("$");  // 在数值前显示美元符号
spinBox->setSuffix(" kg"); // 在数值后显示单位
```

**信号和槽**

`QSpinBox` 提供了一些信号，例如 `valueChanged` 信号，当数值发生变化时会发出该信号。可以连接到槽函数来处理数值变化事件：

```cpp
connect(spinBox, SIGNAL(valueChanged(int)), this, SLOT(onValueChanged(int)));

void MainWindow::onValueChanged(int value) {
    qDebug() << "New value:" << value;
}
```

**练习**

把上面的例子串起来写一写

```cpp
QSpinBox *spinBox = new QSpinBox(this);
       spinBox->setRange(0, 100);
       spinBox->setValue(10);
       spinBox->setSingleStep(5);
       spinBox->setPrefix("$");
       spinBox->setSuffix(" kg");

spinBox->setGeometry(250,300,70,30);
```

**总结**

`QSpinBox` 是一个功能强大的控件，用于显示和编辑整数值。通过设置初始值、数值范围、步长、前缀和后缀等，可以灵活地定制 `QSpinBox` 的行为。结合信号和槽机制，可以轻松处理数值变化事件。这个控件在需要数值输入的应用程序中非常有用。

#### QComboBox

`QComboBox` 是 Qt 提供的一个下拉列表控件，允许用户从一个列表中选择一个条目。它可以包含文本条目，也可以包含更复杂的自定义项。

添加条目的接口

``` cpp
void  addItem(const QString &text, const QVariant &userData = QVariant())
void  addItem(const QIcon &icon, const QString &text, const QVariant &userData = QVariant())

```

userData字段很少用到，在传递自定义数据的时候会用到。我们添加条目时默认只写一个文本参数即可。

**练习**

创建并添加条目

``` cpp
//创建下拉列表控件
QComboBox *comboBox = new QComboBox(this);
//添加条目
comboBox->addItem("Option 1");
comboBox->addItem("Option 2");
comboBox->addItem("Option 3");
//移动到250,400位置
comboBox->move(250,400);
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242036298329.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242036298329.png)

### 显示类

#### QLabel

`QLabel` 是 Qt 提供的用于显示文本或图像。它常用于展示静态内容，并且可以与其他控件组合使用来构建用户界面。

可以直接在构造函数里指定QLabel要显示的文本

``` cpp
explicit QLabel(QWidget *parent=nullptr, Qt::WindowFlags f=Qt::WindowFlags());
explicit QLabel(const QString &text, QWidget *parent=nullptr, Qt::WindowFlags f=Qt::WindowFlags());
```

例如：

``` cpp
 // 创建一个简单的文本标签
 QLabel *textLabel = new QLabel("Hello, QLabel!");
```

指定父窗口后，QLabel会自动添加到父窗口的(0,0)位置，可以通过move移动到指定的位置

``` cpp
 QLabel *textLabel = new QLabel("Hello, QLabel!",this);
```

如果未设置父窗口，可调用addWidget将label加入指定窗口. 比如在MainWindow的构造函数中调用

``` cpp
this->addWidget(textLabel);
```

也可以通过setText更新QLabel显示的文本

``` cpp
textLabel->setText("Hello, Heima");
```

**练习**

主窗口设置一个下拉列表框和QLabel，下拉列表框有三个下拉选项（option1, option2, option3），

 选择下拉条目后，label显示下拉列表框选择的内容.

提示：

QComboBox在条目有变化的时候会发出信号 currentTextChanged

**答案**

``` cpp
//创建下拉列表控件
QComboBox *comboBox = new QComboBox(this);
//添加条目
comboBox->addItem("Option 1");
comboBox->addItem("Option 2");
comboBox->addItem("Option 3");
//移动到250,400位置
comboBox->move(250,400);

//获取当前下拉框文本
auto text = comboBox->currentText();
QLabel *textLabel = new QLabel(this);
textLabel->move(250,500);
textLabel->setText(text);
//连接下拉框文本变化的信号
connect(comboBox,&QComboBox::currentTextChanged, [textLabel,comboBox](){
    textLabel->setText(comboBox->currentText());
});
```



#### QGraphicsView

`QGraphicsView` 是 Qt 框架中的一个类，用于显示和交互 `QGraphicsScene` 中的内容。它是 Qt 的图形视图框架的一部分，该框架提供了一种灵活且高效的方法来管理和显示复杂的 2D 图形.`QGraphicsView` 提供了一个视口（viewport），通过这个视口可以查看 `QGraphicsScene` 的一部分。视口可以移动和缩放，从而查看场景的不同部分。之后在绘图的时候给大家演示，这个目前仅作了解

#### QProgressBar

`QProgressBar` 是 Qt 框架中的一个小部件类，用于显示任务进度的图形化表示。它通常用于展示任务的完成百分比，给用户提供任务进度的视觉反馈。`QProgressBar` 的使用非常简单且直观，适用于各种需要显示进度的场景，例如文件下载、数据处理等

**设置范围**

可以通过 `setRange(int minimum, int maximum)` 方法设置进度条的最小值和最大值。默认情况下，最小值为 0，最大值为 100。

**设置当前值**

可以通过 `setValue(int value)` 方法设置当前的进度值。进度值在最小值和最大值之间变化。

**文本显示**

`QProgressBar` 可以在进度条上显示文本，例如完成百分比。可以通过 `setFormat(const QString &format)` 方法自定义显示的文本格式。

**练习**

主界面拖动一个按钮和进度条。进度条初始值为0，范围为0到100.

当点击按钮后，定时更新进度条，每100ms进度条的数值+1。进度条满后停止计时。

提示：QTimer为定时器类，大家锻炼下查阅assistant的能力

​			QTimer有start函数开启定时器，参数为设置的检测时间间隔，单位为ms

​			QTimer信号timout会在每次时间间隔达到时发送。

​			QTimer有stop函数停止定时器



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242928285718.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242928285718.png)

**答案**

ui中拖动按钮和进度条，按钮名称修改为timerBtn, 进度条修改为timerProgress



``` cpp
//定义定时器
auto timer = new QTimer(this);
// 绑定定时器检测间隔超时信号和回调函数
connect(timer, &QTimer::timeout, [this, timer](){
    //判断进度条是否满格
    if(ui->timerProgress->value() >= 100){
        timer->stop();
        return;
    }
    //更新进度条数值
    ui->timerProgress->setValue(ui->timerProgress->value()+1);
});

//连接点击信号
connect(ui->timerBtn,&QPushButton::clicked,[this,timer](){
    //开始定时器，每个100ms进行检测一次
    timer->start(100);
});
```



还有一些组件比如Slider，以后用到了再查文档即可，QT提供的控件库太丰富了，学习常用的先入手。

### 布局

当我们拖动一个新的控件到ui文件中，需要关注ui文件中其他控件的位置，防止两个控件重叠。

有时，随着界面调整，按照位置设置好的控件不会随着界面拉伸而改变。

比如我们拖动MainWindow界面，控件并没有随着MainWindow的拉伸做调整

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242938554425.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242938554425.png)

对于这种情况，我们可以采用Layout布局解决。

布局分为四种，有垂直布局，网格布局，水平布局，表单布局。

我们先看水平布局, 布局中的所有控件水平排列

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242946486286.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242946486286.png)

垂直布局, 布局中的所有控件垂直排列

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242949835560.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242949835560.png)



网格布局，布局中的所有控件按照网格的方式排列，有的占据多行或者多列。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242950913080.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242950913080.png)

表单布局，可以方便的完成表单样式，比如我们一些登录注册信息ui可以用这个布局。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242951754863.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17242951754863.png)



设置布局整体有三种方式：

1. 在ui中选中窗口，将窗口调整为垂直布局，网格布局，或者水平布局的一种
2. 拖动一种布局放入ui，再将其他控件放入布局中。
3. 写代码添加布局，然后再写代码将控件加入布局中。

先介绍第一种，我们双击mainwindow.ui，打开QT designer , 选中右侧对象层级表中centralWidget,



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243110214511.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243110214511.png)

再点击工具栏中网格布局图标

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243111404788.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243111404788.png)

将MainWindow的centralwidget设置为网格布局，可以在ui布局中看到控件整体布局变成了网格模式

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243113238792.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243113238792.png)

运行起来，仍有部分控件散乱排布，是因为我们没有将控件加入布局，直接添加到mainwindow导致的，接下来我们用代码的方式将这些控件加入布局.

因为我们将centralwidget修改为网格布局，所以ui->centralWidget->layout()可以直接访问这个网格布局

``` cpp
    //创建按钮，显示文本
    QPushButton *button = new QPushButton("Click Me", this);
    //为按钮设置图标
    button->setIcon(QIcon(":/res/open.png"));
    //设置按钮的位置和大小
    button->setGeometry(100, 100, 100, 40);
    connect(button, &QPushButton::clicked,
            this, &MainWindow::slotBtnClick);
    ui->centralWidget->layout()->addWidget(button);
```

依次类推，大家可以将其他的控件都加入布局，看到i的效果就是

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243122603213.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243122603213.png)

当我们缩放或者拉伸，可以看到控件会随着拉伸变化。

我们在对象管理器中选中centralWidget,观察右下方属性管理器

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243132278812.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243132278812.png)

红色框中 layoutHorizontalSpacing表示控件之间的水平间距

layoutVerticalSpacing表示控件之间的垂直间距

layoutRowStretch表示垂直拉伸比例，当布局被拉伸后，里面的控件垂直拉伸的比例如何。

layoutColumnStretch表示水平拉伸比例，当布局被拉伸后，里面的控件水平拉伸的比例如何。

如果是水平布局或i这垂直布局，间距用layoutSpacing表示，拉伸比用layoutStretch表示。

#### 代码方式创建布局

布局类型：

- 水平布局QHBoxLayout

- 垂直布局QVBoxLayout
- 网格布局QGridLayout

向布局中添加widget控件，第一个参数是要添加的控件，第二个参数是该控件的拉伸比例，不设置默认等比拉伸

``` cpp
void addWidget(QWidget *, int stretch = 0, Qt::Alignment alignment = Qt::Alignment());
```

假设水平布局中有两个控件A和B，A的拉伸比例为2，B的拉伸比例为1，那么当界面被水平拉伸时，控件A宽度的增长速度是B的2倍

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243852453919.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243852453919.png)

拉伸后

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243853493245.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243853493245.png)

可以看到拉伸后A的宽度是B的2倍

**练习**

我们创建水平布局，封装到函数SetHorizontalLayout中

``` cpp
void MainWindow::SetHorizontalLayout()
{
    //添加水平布局
    auto layout = new QHBoxLayout(this);
    //创建两个按钮
    auto btn1 = new QPushButton("btn1",this);
    auto btn2 = new QPushButton("btn2",this);
    //将按钮加入到layout中
    layout->addWidget(btn1);
    layout->addWidget(btn2);
    //将centralwidget布局设置为水平布局
    ui->centralWidget->setLayout(layout);
}
```

在MainWindow的构造函数中调用，再启动程序能看到按钮并排排列了。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243748812636.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243748812636.png)



创建垂直布局

``` cpp
void MainWindow::SetVerticalLayout()
{
    //添加垂直布局
    auto layout = new QVBoxLayout(this);
    //添加两个按钮
    auto btn1 = new QPushButton("btn1",this);
    auto btn2 = new QPushButton("btn2",this);
    //将按钮加入布局
    layout->addWidget(btn1);
    layout->addWidget(btn2);
    //将centralwidget布局设置为垂直布局
    ui->centralWidget->setLayout(layout);
}
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243756916615.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243756916615.png)



创建网格布局

``` cpp
void MainWindow::SetGridLayout()
{
    //添加网格布局
    auto layout = new QGridLayout(this);
    //创建几个按钮
    auto btn1 = new QPushButton("btn1",this);
    auto btn2 = new QPushButton("btn2", this);
    auto btn3 = new QPushButton("btn3", this);
    auto btn4 = new QPushButton("btn4", this);
    auto btn5 = new QPushButton("btn5", this);
    //btn1 放在第一行第一列，占一行一列
    layout->addWidget(btn1,0,0,1,1);
    //btn2 放在第二行第一列，占一行两列
    layout->addWidget(btn2,1,0,1,2);
    //btn3 放在第二行第三列，占一行一列
    layout->addWidget(btn3,1,2,1,1);
    //btn4 放在第三行第一列，占两行一列
    layout->addWidget(btn4,2,0,2,1);
    //btn5 放在第四行第二列，占一行一列
    layout->addWidget(btn5,3,1,1,1);
    //将centralwidget设置为网格布局
    this->centralWidget()->setLayout(layout);
}
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243779434839.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243779434839.png)

因为整个页面高度很大，所以按钮布局看起来高度不一致。可以拉伸页面，将高度缩小为最小，就能看到btn4实际是占用了两行。

#### 添加弹簧

QT提供了弹簧控件，可以通过Designer拖动到ui中，Horizontal Spacer是水平弹簧，Vertical Spacer是垂直弹簧

弹簧的作用就是压缩空间，让控件达到紧凑排布的效果。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243782456276.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243782456276.png)

也可写代码创建，写代码创建的弹簧是不分垂直还是水平的，取决于将弹簧添加到什么布局里，将弹簧加到水平布局里就是水平弹簧，将弹簧加到垂直布局里就是垂直布局

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243795114533.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243795114533.png)

QSpacerItem构造函数

``` cpp
QSpacerItem(int w, int h,QSizePolicy::Policy hData = QSizePolicy::Minimum,
                 QSizePolicy::Policy vData = QSizePolicy::Minimum)
```

第一个参数为弹簧的宽，第二个参数为弹簧的高，第三个参数为弹簧的水平策略，第四个参数为弹簧的垂直策略。

**常见的 `QSizePolicy` 策略**



1. **Fixed**:
   小部件的大小是固定的，不能扩展或收缩。
2. **Minimum**:
   小部件可以收缩到最小大小，但不能扩展。
3. **Maximum**:
   小部件可以扩展到最大大小，但不能收缩。
4. **Preferred**:
   小部件可以根据其建议的大小进行调整，但不会强制扩展或收缩。
5. **Expanding**:
   小部件可以扩展以填充可用空间。
6. **MinimumExpanding**:
   小部件可以收缩到最小大小，但也可以扩展以填充可用空间。
7. **Ignored**:
   小部件的大小策略被忽略，布局管理器将不会考虑它的大小。

不用死记硬背，最常用的就是好Expanding和Fixed，其余用到了再查文档。

将弹簧加入布局的函数为

``` cpp
void addSpacerItem(QSpacerItem *spacerItem);
```

**练习**

写代码在水平布局中插入一个弹簧，将按钮挤压到最左侧。

``` cpp
void MainWindow::SetHorizontalLayout()
{
    //添加水平布局
    auto layout = new QHBoxLayout(this);
    //创建两个按钮
    auto btn1 = new QPushButton("btn1",this);
    auto btn2 = new QPushButton("btn2",this);
    //将按钮加入到layout中
    layout->addWidget(btn1);
    layout->addWidget(btn2);
    //创建水平弹簧，水平为扩展策略，垂直为可扩充到最大20像素
    auto h_spacer = new QSpacerItem(40,20,
         QSizePolicy::Expanding,QSizePolicy::Maximum);
    //布局里添加弹簧
    layout->addSpacerItem(h_spacer);
    //将centralwidget布局设置为水平布局
    ui->centralWidget->setLayout(layout);
}
```

**效果**

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243804219663.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243804219663.png)

垂直布局也是这么设置，添加的弹簧默认为垂直弹簧。

那么网格布局添加弹簧需要指定弹簧所在的行列，添加的函数变成了addItem

``` cpp
void addItem(QLayoutItem *item, int row, int column, int rowSpan = 1, 
             int columnSpan = 1, Qt::Alignment = Qt::Alignment());
```

我们基于前面创建的网格布局代码，添加弹簧

``` cpp
//创建垂直弹簧，水平策略为Maximum,垂直方向为Expanding
auto v_spacer = new QSpacerItem(40,20,
        QSizePolicy::Maximum,QSizePolicy::Expanding);
//创建水平弹簧，水平策略为Expanding,垂直策略为Maximum
auto h_spacer = new QSpacerItem(40,20,
        QSizePolicy::Expanding, QSizePolicy::Maximum);
//加入垂直弹簧，放在第五行第1列
layout->addItem(v_spacer,4,0);
//加入水平弹簧，放在第四行第3列
layout->addItem(h_spacer,3,2);
//将centralwidget设置为网格布局
this->centralWidget()->setLayout(layout);
```

效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243818949933.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243818949933.png)

#### 布局边界

我们将一个控件或者多个控件放入布局后，它们与布局边界之间的距离叫做边界(Margin)



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724382926213.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1724382926213.png)

可通过Designer中对布局设置编剧

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243831875034.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243831875034.png)

也可以通过代码设置

``` cpp
//设置边距
void setContentsMargins(int left, int top, int right, int bottom);
```

**练习**

将之前的水平布局边距分别设置为左边距20，上边距30，右边距40，底边距50的样式

**答案**

``` cpp
layout->setContentsMargins(20,30,40,50);
```

### QListWidget

`QListWidget` 是 Qt 提供的一个方便的列表小部件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243865928078.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243865928078.png)

我们打开ui布局管理器，拖动一个QListWidget放入mainwindow.ui中

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243870486983.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243870486983.png)

右键这个QListWidget，选择编辑项目

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243871135223.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243871135223.png)

点击加号创建项目，项目名字可以修改

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243872962084.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243872962084.png)

保存ui运行一下，看看效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172438736474.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172438736474.png)



### 综合练习

实现如下界面，Profession下拉列表可以用QListWidget



![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243965443725.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243965443725.png)

## QListWidget知识



`QListWidget` 是 Qt 提供的一个便捷的列表小部件，它继承自 `QListView` 并提供了用于管理列表项的高级接口。`QListWidget` 通常用于显示和管理一组项目（`QListWidgetItem`），这些项目可以是文本、图标或两者的组合。

### 基本用法

以下是一些常见的操作，包括创建 `QListWidget`、添加项目、删除项目和响应用户交互。

#### 创建 `QListWidget`

创建一个 `QListWidget` 实例非常简单：

``` cpp
int main(int argc, char *argv[]) {
    QApplication app(argc, argv);

    QWidget window;
    //创建垂直布局
    QVBoxLayout *layout = new QVBoxLayout(&window);
    //创建ListWidget
    QListWidget *listWidget = new QListWidget(&window);
    //把listwidget加入布局中
    layout->addWidget(listWidget);
    //window设置布局
    window.setLayout(layout);
    //展示窗口
    window.show();

    return app.exec();
}
```

#### 添加项目

你可以使用 `addItem` 或 `addItems` 方法来添加项目：

``` cpp
// 添加单个项目
listWidget->addItem("Item 1");

// 添加多个项目
QStringList items = {"Item 2", "Item 3", "Item 4"};
listWidget->addItems(items);
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243980738275.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17243980738275.png)

你也可以创建 `QListWidgetItem` 对象并添加到 `QListWidget`：

``` cpp
QListWidgetItem *item = new QListWidgetItem("Item 5");
listWidget->addItem(item);
```

在指定行之前插入item

``` cpp
void insertItem(int row, QListWidgetItem *item);
```

#### 删除项目

你可以使用 `takeItem` 方法根据行号获取某个item，再调用delete方法删除这个item：

``` cpp
// 删除第一个项目, 0表示第一行
delete listWidget->takeItem(0);
```

可以利用QListWidget的row函数获取item对应的行号

``` cpp
int QListWidget::row(const QListWidgetItem *item) const
```

如果知道某个具体的item，想要从listwidget中删除, 可以用如下函数

``` cpp
inline void QListWidget::removeItemWidget(QListWidgetItem *aItem)
```

同时还需要回收aItem的内存才能彻底删除

``` cpp
listWidget->removeItemWidget(item);
delete item; // 释放内存
```

#### 获取选中的项目

你可以使用 `selectedItems` 方法来获取所有选中的项目：

``` cpp
QList<QListWidgetItem*> selectedItems = listWidget->selectedItems();
for (QListWidgetItem *item : selectedItems) {
    qDebug() << item->text();
}
```

#### 响应用户交互

你可以连接 `QListWidget` 的信号到槽函数来响应用户交互。例如，连接 `itemClicked` 信号：

``` cpp
QObject::connect(listWidget, &QListWidget::itemClicked, [](QListWidgetItem *item) {
    qDebug() << "Item clicked:" << item->text();
});
```

#### 自定义项目

你可以自定义 `QListWidgetItem` 的外观和行为。例如，设置图标、字体和背景颜色：

``` cpp
QListWidgetItem *item = new QListWidgetItem("Custom Item");
item->setIcon(QIcon(":/monkey.png"));
item->setFont(QFont("Arial", 14));
item->setBackground(Qt::yellow);
listWidget->addItem(item);
```

#### 点击信号

QListWidget中的item点击后会发出itemClicked信号

``` cpp
[signal] void QListWidget::itemClicked(QListWidgetItem *item)
```

所以可以捕获这个信号，获取item的信息。

### 练习案例

实现如下界面，点击删除选中条目按钮，则删除选中条目，未选中条目则提示未选中。

点击选中条目前插入，则在选中条目前插入文本的内容。文本为空则提示文本为空，未选中条目则提示未选中条目.

点击末尾追加，则在listwidget的末尾添加文本内容。文本为空则提示文本为空。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246369909385.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246369909385.png)

**答案**

1.  先进入ui文件拖动界面，形成如下布局

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246556608688.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246556608688.png)

界面命名和布局关系图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246558257707.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246558257707.png)

2. 添加删除选中条目被点击的逻辑,  构造函数中连接点击信号和槽

``` cpp
//连接删除按钮点击信号
connect(ui->delBtn, &QPushButton::clicked, this, &MainWindow::slotDel);
```

删除的槽函数

``` cpp
void MainWindow::slotDel()
{
    //获取当前选中的条目列表
    auto list_item = ui->listWidget->selectedItems();
    if(list_item.empty()){
        QMessageBox::information(this,"提示","未选中任何条目");
        return;
    }

    for(auto & item : list_item){
        //删除item
        ui->listWidget->removeItemWidget(item);
        delete item;
    }
}
```

3. 添加插入条目的功能，构造函数先连接点击信号和槽

``` cpp
//连接插入条目的信号
connect(ui->insertBtn, &QPushButton::clicked, this, &MainWindow::slotInsert);
```

插入槽函数

``` cpp
void MainWindow::slotInsert()
{
    //在选中的条目之前插入
    auto list_item = ui->listWidget->selectedItems();
    if(list_item.empty()){
        QMessageBox::information(this,"提示","未选中任何条目");
        return;
    }
    //获取lineEdit 的text
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"提示","未输入有效信息");
        return;
    }

    //获取第一个选中的item所在的行号
    auto item_row = ui->listWidget->row(list_item[0]);
    //在指定行号前插入item
    ui->listWidget->insertItem(item_row,text);
}
```

4. 添加追加条目的功能，构造函数先连接点击信号和槽

``` cpp
//连接追加的条目信号
connect(ui->appendBtn, &QPushButton::clicked, this, &MainWindow::slotAppend);
```

末尾追加的槽函数

``` cpp
void MainWindow::slotAppend()
{
    //获取lineEdit 的text
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"提示","未输入有效信息");
        return;
    }
    //尾部追加条目
    ui->listWidget->addItem(text);
}
```

实现追加的槽函数

``` cpp
void MainWindow::slotAppend()
{
    //获取lineEdit 的text
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"提示","未输入有效信息");
        return;
    }
    //尾部追加条目
    ui->listWidget->addItem(text);
}
```

5. 响应添加点击item的槽函数

在mainwindow的构造函数中添加连接

``` cpp
//连接item被点击信号
connect(ui->listWidget, &QListWidget::itemClicked, this,
        &MainWindow::slotItemClicked);
```

实现响应槽函数点击的逻辑

``` cpp
void MainWindow::slotItemClicked(QListWidgetItem *item)
{
    auto text = item->text();
    text = QString("当前选中条目：%1").arg(text);
    ui->label_2->setText(text);
}
```





## QTableWidget

QTableWidget是用来以表格方式展现数据的结构

QTableWidget的构造函数

``` cpp
//指定父节点构造QTableWidget
QTableWidget::QTableWidget(QWidget *parent = nullptr)
//指定行号，列号以及父节点构造QTableWidget
QTableWidget::QTableWidget(int rows, int columns, QWidget *parent = nullptr)
```

**示例**

``` cpp
//构造一个三行四列的QTableWidget
auto table_wid = new QTableWidget(3,4);
```

### 设置表头

设置行数和列数

``` cpp
//设置列数
void setColumnCount(int columns);
//获取列数
int columnCount() const;
//设置行数
void setRowCount(int rows);
//返回行数
int rowCount() const;
```

**示例**

``` cpp
auto table_wid = new QTableWidget();
//设置列数为3
table_wid->setColumnCount(3);
//设置行数为3
table_wid->setRowCount(3);
```

设置水平表头的标签

``` cpp
void QTableWidget::setHorizontalHeaderLabels(const QStringList &labels)
```

设置垂直表头的标签信息

``` cpp
void QTableWidget::setVerticalHeaderLabels(const QStringList &labels)
```

**示例**

``` cpp
auto table_wid = new QTableWidget();
//设置列数为3
table_wid->setColumnCount(3);
//设置行数为3
table_wid->setRowCount(3);
//设置水平标签
table_wid->setHorizontalHeaderLabels(
     QStringList()<<"Column 1" << "Column 2" << "Column 3");
//设置垂直标签
table_wid->setVerticalHeaderLabels(
     QStringList()<<"Row 1" << "Row 2" << "Row 3");
```

### 当前项和选中

**当前项**

QTableWidget有选中和当前项的概念，

当前项是当前选中的列表项，通过视觉效果显示出来，用户可通过键盘或者鼠标与当前项交互, 比如当前项时第一行第一列。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246671132144.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246671132144.png)



有时会没有当前项，可以通过这个函数判断

``` cpp
QTableWidgetItem *currentItem() const;
```

如果这个函数返回值为空，则说明当前QTableWidget没有焦点。

**选中**

选中和当前项不同，选中可以选择多个，但是当前项只能有一个。

当我们选中一列或一行的时候，当前项所在的单元格可能就变化了。

大家可以看到当我点击第二列的时候，在第二列第一行出现了虚线框，说明当前项变成了第1行第2列。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246595621584.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246595621584.png)

**示例**

``` cpp
//创建3行4列的表格
auto table_wid = new QTableWidget(3,4);
//获取当前item
auto * cur_item = table_wid->currentItem();
```

### 设置当前项

我们可以通过setCurrentItem或者setCurrentCell设置当前项

``` cpp
//设置当前项
void QTableWidget::setCurrentItem(QTableWidgetItem *item)
//设置当前项
void QTableWidget::setCurrentCell(int row, int column)
```

``` cpp
//将当前项设置为第1行第1列
ui->tableWidget->setCurrentCell(0,0);
```

### 获取当前的列和行

``` cpp
//返回焦点当前的行
int currentRow() const;
//返回焦点当前的列
int currentColumn() const;
```

**示例**

获取当前焦点所在的行号和列号

``` cpp
//创建3行4列的表格
auto table_wid = new QTableWidget(3,4);
//获取当前行
auto cur_row = table_wid->currentRow();
//获取当前列
auto cur_col = table_wid->currentCol();
```

### 插入列

我们可以在指定位置插入一列

``` cpp
//在第column插入一列
void QTableWidget::insertColumn(int column)
```

**示例**

``` cpp
//创建3行4列的表格
auto table_wid = new QTableWidget(3,3);
//设置水平标签
table_wid->setHorizontalHeaderLabels(
     QStringList()<<"Column 1" << "Column 2" << "Column 3");
//设置垂直标签
table_wid->setVerticalHeaderLabels(
     QStringList()<<"Row 1" << "Row 2" << "Row 3");
//在第二列处插入一列
table_wid->insertColumn(0);
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246618231612.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246618231612.png)

默认情况下，插入的列名字为其所在的列序号，如果想改为我们自定义的名字可调用

``` cpp
void setHorizontalHeaderItem(int column, QTableWidgetItem *item);
```

第一个参数为要修改的头部的哪一列，第二个参数为用item替换这个头部的列

**示例**

``` cpp
//创建3行4列的表格
auto table_wid = new QTableWidget(3,3);
//设置水平标签
table_wid->setHorizontalHeaderLabels(
     QStringList()<<"Column 1" << "Column 2" << "Column 3");
//设置垂直标签
table_wid->setVerticalHeaderLabels(
     QStringList()<<"Row 1" << "Row 2" << "Row 3");
//在第二列处插入一列
table_wid->insertColumn(0);    
 //更新列的名字
 auto * col_item = new QTableWidgetItem("Column 0");
 //更新cur_col的列表头
 table_wid->setHorizontalHeaderItem(0, col_item);
```



### 删除列

``` cpp
//删除第column列
void removeColumn(int column);
```

**示例**

``` cpp
//删除第2列
table_wid->removeColumn(1);
```

### 获取列数

``` cpp
//返回tablewidget的列数
int columnCount() const;
```

行的操作和列类似，这里我们列举下行的用法

``` cpp
//删除行
 void removeRow(int row);
//插入行
 void insertRow(int row);
//设置垂直表头
QTableWidgetItem *takeVerticalHeaderItem(int row);
```

### 更新数据

我们可以更新某一行某一列的单元格内的数据

``` cpp
//更新row行(从0开始)，column列(从0开始)的单元格数据 
void setItem(int row, int column, QTableWidgetItem *item);
```

**示例**

``` cpp
//创建一个item用来填充数据
auto new_item = new QTableWidgetItem("hello");
//将item设置到表格中,更新第2行1列数据
table_wid->setItem(1,0,new_item);
```

### 删除数据

通过takeItem根据行和列选择要删除的item

``` cpp
 QTableWidgetItem *takeItem(int row, int column);
```

调用delete删除这个item即可清空单元格数据

``` cpp
 delete item;
```

### 点击信号

QTableWidget中的某个item被点击会发出itemClicked信号

``` cpp
[signal] void QTableWidget::itemClicked(QTableWidgetItem *item)
```

可以捕获这个信号，对点击的item做一些处理和判断。

**注意**

QTableWidget中必须有item，点击这个item才会发出itemClicked信号，如果是空的表格是不会发出这个信号的。

对于空表格项或者存储item的表格项，我们可以捕获cellClicked信号

``` cpp
[signal] void QTableWidget::cellClicked(int row, int column)
```

**示例**

``` cpp
//创建3行4列的表格
auto table_wid = new QTableWidget(3,3);
//连接单元格被点击的信号
connect(table_wid, &QTableWidget::cellClicked, [](int row, int column){
    qDebug()<< "row is " << row <<" column is " << column;
})
```

### **练习案例**

实现如下界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246696506476.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17246696506476.png)

**要求**

1. 创建一个3行3列的表格，表头列信息分别为Column 1,Column 2,Column 3...

​	   行信息分别为Row1, Row2, Row3...

2. 默认为第1行第1列单元格为当前项
3. 根据输入的信息，点击增加列，将信息增加到当前列之前。支持在最后一列之后追加列，删除列等操作。
4. 根据输入的信息，点击增加行，将信息增加到当前行之前，支持在最后一行之后追加行，删除行等操作。
5. 点击选中后，打印当前条目信息。
6. 支持更新数据和删除数据操作。

**答案**

先拖动界面ui布局达到如下效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247191703736.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247191703736.png)

界面关系图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247198777955.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247198777955.png)

接下来我们在MainWindow的构造函数中初始化表格

``` cpp
//设置列
ui->tableWidget->setColumnCount(3);
//设置行
ui->tableWidget->setRowCount(3);
//设置水平头部标签
ui->tableWidget->setHorizontalHeaderLabels(
 QStringList()<<"Column 1" << "Column 2" << "Column 3");
//设置垂直头部标签
ui->tableWidget->setVerticalHeaderLabels(
 QStringList()<<"Row 1" << "Row 2" << "Row 3");
//默认设置当前项为第1行第1列
ui->tableWidget->setCurrentCell(0,0);
//初始化焦点信息
qDebug() << ui->tableWidget->currentItem();
auto cur_row = ui->tableWidget->currentRow();
auto cur_col = ui->tableWidget->currentColumn();
qDebug() << cur_row << cur_col;
if(cur_row != -1 && cur_col != -1){
    ui->label_4->setText(
    QString("当前条目: %1行%2列").arg(cur_row).arg(cur_col));
}
```

构造函数中，响应某个item被点击，只有在表格中有数据的时候点击才会触发。

``` cpp
//响应某个item被点击
connect(ui->tableWidget,&QTableWidget::itemClicked,
        [this](QTableWidgetItem *item){

    ui->label_4->setText( QString("当前条目: %1行%2列").
                          arg(item->row()).arg(item->column()));
});
```

响应某个单元格被点击

``` cpp
//响应某个单元被点击
connect(ui->tableWidget, &QTableWidget::cellClicked,
        [this](int row, int column){
    ui->label_4->setText( QString("当前条目: %1行%2列").
                          arg(row).arg(column));
       });
```

响应添加列按钮被点击

``` cpp
//添加列
connect(ui->addCol,&QPushButton::clicked, [this](){
    //判断文本是否为空
    if(ui->lineEdit->text().isEmpty()){
        QMessageBox::information(this,"通知","输入文本为空");
        return;
    }

    //获取当前单元所在的列
    auto cur_col = ui->tableWidget->currentColumn();
    if(cur_col < 0){
        QMessageBox::information(this,"通知","未选中任何列");
        return;
    }

    //在cur_col位置插入一列
    ui->tableWidget->insertColumn(cur_col);
    //要插入的文本
    auto text = ui->lineEdit->text();
    //更新列的名字
    auto * col_item = new QTableWidgetItem(text);
    //更新cur_col的列表头
    ui->tableWidget->setHorizontalHeaderItem(cur_col, col_item);

});
```

响应追加列被点击

``` cpp
//追加列
connect(ui->appendCol,&QPushButton::clicked,[this](){
    //判断文本是否为空
    if(ui->lineEdit->text().isEmpty()){
        QMessageBox::information(this,"通知","输入文本为空");
        return;
    }

    //获取列号
    auto col_count = ui->tableWidget->columnCount();
    //新增一列数据
    ui->tableWidget->insertColumn(col_count);
    //要插入的文本
    auto text = ui->lineEdit->text();
    //生成一个item用来更新表头数据
    auto col_item = new QTableWidgetItem(text);
    //更新表头对应的列数据
    ui->tableWidget->setHorizontalHeaderItem(col_count, col_item);

});
```

响应删除列按钮被点击

``` cpp
//删除列
connect(ui->delCol,&QPushButton::clicked,[this](){
    auto col = ui->tableWidget->currentColumn();
    if(col < 0){
        QMessageBox::information(this,"通知","未选中任何列");
        return;
    }

    ui->tableWidget->removeColumn(col);
});
```

响应添加行按钮被点击

``` cpp
//添加行
connect(ui->addRow,&QPushButton::clicked,[this](){
    //判断是否存在当前选中行
    auto cur_row = ui->tableWidget->currentRow();
    if(cur_row < 0){
        QMessageBox::information(this,"通知","未选中任何行");
        return;
    }

    //获取文本输入框内容
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","输入信息为空");
        return;
    }

    //在cur_row插入一行
    ui->tableWidget->insertRow(cur_row);
    //创建一个item用来更新表头的行信息
    auto row_item = new QTableWidgetItem(text);
    ui->tableWidget->setVerticalHeaderItem(cur_row, row_item);
});
```

响应删除行和追加行的按钮点击信号

``` cpp
//删除行
connect(ui->delRow,&QPushButton::clicked,[this](){
    //获取当前行
    auto cur_row = ui->tableWidget->currentRow();
    ui->tableWidget -> removeRow(cur_row);
});

//追加行
connect(ui->appendRow,&QPushButton::clicked,[this](){

    //判断文本内容
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","输入信息为空");
        return;
    }
    //获取总行数
    auto row_count = ui->tableWidget->rowCount();
    //在末尾的行后添加一行
    ui->tableWidget->insertRow(row_count);
    //创建item用来填写表头信息
    auto item = new QTableWidgetItem(text);
    //把item 放入垂直表头里
    ui->tableWidget->setVerticalHeaderItem(row_count,item);
});
```

添加数据

``` cpp
//添加数据
connect(ui->addData,&QPushButton::clicked,[this](){
    //判断文本内容
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","输入信息为空");
        return;
    }
    //获取输入的行号
    auto row_str = ui->rowLineEdit->text();
    //获取输入的列号
    auto col_str = ui->colLineEdit->text();
    if(row_str.isEmpty() || col_str.isEmpty()){
        QMessageBox::information(this,"通知","行号或列号为空");
        return;
    }

    bool b_success = false;
    auto row_int = row_str.toInt(&b_success);
    if(!b_success){
        QMessageBox::information(this,"通知","行号转换失败");
        return;
    }

    auto col_int = col_str.toInt(&b_success);
    if(!b_success){
        QMessageBox::information(this,"通知","列号转换失败");
        return;
    }

    //创建一个item用来填充数据
    auto new_item = new QTableWidgetItem(text);
    //将item设置到表格中
    ui->tableWidget->setItem(row_int-1,col_int-1,new_item);
});
```

响应删除数据的按钮点击事件

``` cpp
//删除数据
connect(ui->delData, &QPushButton::clicked, [this](){
    //判断文本内容
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","输入信息为空");
        return;
    }
    //获取输入的行号
    auto row_str = ui->rowLineEdit->text();
    //获取输入的列号
    auto col_str = ui->colLineEdit->text();
    if(row_str.isEmpty() || col_str.isEmpty()){
        QMessageBox::information(this,"通知","行号或列号为空");
        return;
    }

    bool b_success = false;
    auto row_int = row_str.toInt(&b_success);
    if(!b_success){
        QMessageBox::information(this,"通知","行号转换失败");
        return;
    }

    auto col_int = col_str.toInt(&b_success);
    if(!b_success){
        QMessageBox::information(this,"通知","列号转换失败");
        return;
    }

    //删除指定行列的数据
    auto item = ui->tableWidget->takeItem(row_int-1,col_int-1);
    delete item;
});
```

## TreeWidget

在Qt C++中，`QTreeWidget`是一个非常强大的类，用于显示和操作树形结构的数据。它继承自`QAbstractItemView`，并提供了丰富的接口来管理树中的项（`QTreeWidgetItem`）。下面我将介绍如何使用`QTreeWidget`在Qt C++应用程序中创建和操作树形结构。

### 1. 包含必要的头文件

首先，确保你的Qt项目中包含了`QTreeWidget`相关的头文件。

``` cpp
#include <QTreeWidget>
#include <QTreeWidgetItem>
```

### 2. 创建QTreeWidget

在你的窗口或对话框类中，你可以通过成员变量或局部变量来创建`QTreeWidget`。

``` cpp
// 假设this是指向当前窗口或对话框的指针
QTreeWidget *treeWidget = new QTreeWidget(this); 
```

### 3. 设置列标题

你可以通过调用`setHeaderLabels()`方法来设置树形控件的列标题。

``` cpp
QStringList headers;
headers << "Name" << "Description";
treeWidget->setHeaderLabels(headers);
```

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247232884463.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247232884463.png)

### 4. 添加项（QTreeWidgetItem）

你可以通过创建`QTreeWidgetItem`的实例并将其添加到`QTreeWidget`中来添加项。

``` cpp
QTreeWidgetItem *parentItem = new QTreeWidgetItem(treeWidget);
parentItem->setText(0, "Parent");
parentItem->setText(1, "Parent Description");

QTreeWidgetItem *childItem = new QTreeWidgetItem(parentItem);
childItem->setText(0, "Child");
childItem->setText(1, "Child Description");
```

在这个例子中，我们首先创建了一个父项`parentItem`，并将其添加到`treeWidget`中。然后，我们创建了一个子项`childItem`，并将其作为`parentItem`的子项添加。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247240308477.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247240308477.png)

### 5. 展开和折叠项

你可以通过调用`expandItem()`和`collapseItem()`方法来展开或折叠树中的项。

``` cpp
treeWidget->expandItem(parentItem); // 展开父项
treeWidget->collapseItem(parentItem); // 折叠父项
```

### 6. 响应项的选择

你可以通过连接`itemSelectionChanged()`信号来响应树中项的选择变化。

``` cpp
connect(treeWidget, &QTreeWidget::itemSelectionChanged, this, &YourClass::onItemSelectionChanged);

// 在YourClass中定义槽函数
void YourClass::onItemSelectionChanged()
{
    QList<QTreeWidgetItem*> selectedItems = treeWidget->selectedItems();
    if (!selectedItems.isEmpty()) {
        QTreeWidgetItem *item = selectedItems.first();
        // 处理选中项
    }
}
```

### 7.删除顶级项（根项）

如果你想要删除`QTreeWidget`中的一个顶级项（即直接附加在`QTreeWidget`上的项，而不是其他项的子项），你可以使用`takeTopLevelItem(int index)`方法。这个方法会移除并返回指定索引的顶级项，索引从0开始。

``` cpp
QTreeWidgetItem *itemToRemove = treeWidget->takeTopLevelItem(index);
// 如果不再需要这个项，则删除它
delete itemToRemove; 
```

**获取根节点索引**

takeTopLevelItem需要传入根节点的索引，那么我们可以通过

``` cpp
treeWidget->indexOfTopLevelItem(topLevelItem1)
```

获取topLevelItem1这个根节点的索引。

### 8.删除子项

如果你想要删除一个项的子项，你需要先获取到该父项，然后使用`takeChild(int index)`方法。但是，更常用的是遍历子项并使用`removeChild(QTreeWidgetItem *child)`方法，因为这样可以更灵活地处理子项。

``` cpp
// 假设你已经有了指向父项的指针 parentItem
int childIndex = ...; // 假设你已经知道了要删除的子项的索引
QTreeWidgetItem *childToRemove = parentItem->takeChild(childIndex);
// 如果不再需要这个子项，则删除它
delete childToRemove; 

// 或者，如果你有一个指向子项的指针
QTreeWidgetItem *childToRemoveDirectly = ...;
parentItem->removeChild(childToRemoveDirectly);
// 如果不再需要这个子项，则删除它
delete childToRemoveDirectly; 
```

**获取子节点索引**

takeChild需要传入子节点索引，我们可以通过

``` cpp
parentItem->indexOfChild(childItem1)
```

获取子节点childItem1在parentItem中的索引。

### 9.实战案例

实现如下树形列表

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247285604141.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17247285604141.png)

**要求**

1. 根据节点信息，点击添加根节点可创建根节点。如果节点信息为空则不创建并弹出提示框“节点信息为空”
2. 点击删除删除节点，可删除选中的节点。如果未选中，则提示“未选择节点”
3. 点击添加子节点，会在选择的节点下创建节点。如果未选中节点则提示“未选择节点”. 如果信息为空则提示“文本为空”
4. 当选择变化时，更新当前选中的标签。
5. 当点击变化时，更新被点击的节点标签

**答案**

构造函数中添加头部标签

``` cpp
QStringList str_list;
str_list << "Description";
ui->treeWidget->setHeaderLabels(str_list);
```

构造函数中监听选择变化

``` cpp
//获取选择变化
connect(ui->treeWidget, &QTreeWidget::itemSelectionChanged,
        [this](){
    auto select_items = ui->treeWidget->selectedItems();
    if(select_items.isEmpty()){
        //未选中直接返回
        return;
    }

    //选中则选第一个默认的
    auto select = select_items[0];
    ui->description->setText(QString("当前选中: %1")
            .arg(select->text(0)));
});
```

构造函数中监听点击变化

``` cpp
//获取点击变化
connect(ui->treeWidget, &QTreeWidget::itemClicked,
        [this](QTreeWidgetItem *item, int column){
   ui->clickdesc->setText(QString("被点击的节点: %1")
                          .arg(item->text(0)));
});
```

响应添加根节点的信号

``` cpp
void MainWindow::on_addRootBtn_clicked()
{
    //获取文本信息
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","为输入节点信息");
        return;
    }
    //添加根节点
    auto tree_item = new QTreeWidgetItem(ui->treeWidget);
    tree_item->setText(0,text);
}
```

响应添加子节点的信号

``` cpp
void MainWindow::on_addChildBtn_clicked()
{
    //获取文本信息
    auto text = ui->lineEdit->text();
    if(text.isEmpty()){
        QMessageBox::information(this,"通知","为输入节点信息");
        return;
    }

    //获取选中item列表
    auto selec_items = ui->treeWidget->selectedItems();
    if(selec_items.isEmpty()){
        QMessageBox::information(this,"通知","选择列表为空");
        return;
    }

    //默认在第一个选中的插入
    auto select = selec_items[0];
    //根据选中节点创建子节点
    auto child_item = new QTreeWidgetItem(select);
    child_item->setText(0,text);
    //展开父节点
    select->setExpanded(true);

}
```

响应删除子节点的信号

``` cpp
void MainWindow::on_rmvChildBtn_clicked()
{
    //获取选中item列表
    auto selec_items = ui->treeWidget->selectedItems();
    if(selec_items.isEmpty()){
        QMessageBox::information(this,"通知","选择列表为空");
        return;
    }

    //删除选择的item
    for(auto & select : selec_items){
        auto *parent = select->parent();
        //说明为根节点
        if(parent == nullptr){
            //获取顶级索引
            auto index_top = ui->treeWidget->indexOfTopLevelItem(select);
            //如果索引为-1说明没找到
            if(index_top == -1){
                continue;
            }
            ui->treeWidget->takeTopLevelItem(index_top);
            continue;
        }
        //如果是普通的子节点，那么直接删除就可以
        parent->removeChild(select);
        delete  select;
    }
}
```





# 第四章 Model/View模型视图

这一章概念很多，方法也很庞杂，主要是基于模型视图来讲，学习的方式是通过案例快速理解，无需纠结文字概念。

## 模型视图三要素

Qt 的 Model-View-Delegate 模式是一种设计模式，旨在分离数据（模型）、展示（视图）和用户交互（委托）。这种模式使得开发者可以灵活地处理数据的显示和编辑，同时保持代码的整洁性和可维护性。

**主要概念**

1. **Model**：负责存储和管理数据。可以是自定义模型或 Qt 提供的标准模型（如 `QStringListModel`、`QStandardItemModel` 等）。
2. **View**：负责显示数据，使用模型提供的数据来渲染用户界面。常见的视图有 `QListView`、`QTableView` 和 `QTreeView`。
3. **Delegate**：负责处理视图中每个项的显示和编辑。委托可以自定义每个项的外观和行为。

在部分企业的数据和展示管理中采用的是模型视图的方式，Model-View-Delegate这种方式可以实现一个模型对应多个展示界面的效果。

三者关系如下

![https://cdn.llfc.club/1723099309502%281%29.jpg](https://cdn.llfc.club/1723099309502%281%29.jpg)

- 模型 分为很多种，都是基于QAbstractItemModel基类派生而来。这个类定义了视图组件和代理存取数据的接口。模型只是在内存中临时存储数据，模型的数据来源可以是其他类、文件、数据库或任何数据源
    - QFileSystemModel 用于表示计算机上文件系统的模型类
    - QStringListModel 用于表示字符串列表数据的模型类
    - QStandardItemModel 标准的基于项的模型类，每个项是一个 QStandardItem 对象
    - QSqlQueryModel 用于表示数据库 SQL 查询结果的模型类
    - QSqlTableModel 用于表示数据库的一个数据表的模型类

- 视图 就是用于显示模型中的数据的界面组件
    - QListView 列表方式视图展示
    - QTreeView 树的方式视图展示
    - QTableView 表格方式视图展示

- 代理 QAbstractItemDelegate 是所有代理类的基类, 不能直接使用,可使用的是如下两个
    - QItemDelegate
    - QStyledItemDelegate
    
    
    
    模型类的继承关系

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726719189600.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726719189600.png)

### 模型结构

模型可以组织成很多种结构，如下三种最为常用

- 表格模型
- 列表模型
- 树状模型

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723100902938.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1723100902938.png)

### 项和索引
模型内部存储的是item，我们叫做项，从模型中获取项，可以采用索引的方式

要获得一个模型索引，必须提供 3 个参数：行号、列号、父项的模型索引

QAbstractItemModel提供了index方法，所以继承自它的模型都具有这个方法

``` cpp
[pure virtual] QModelIndex QAbstractItemModel::index(int row, int column, const QModelIndex &parent = QModelIndex()) const
```

row表示获取哪一行的元素，columne表示获取哪一列的元素， parant表示获取哪个节点下的子节点。

对于表格中的A,B,C三项可通过如下代码获取
``` cpp
QModelIndex indexA = model->index(0, 0, QModelIndex()); 
QModelIndex indexB = model->index(1, 1, QModelIndex()); 
QModelIndex indexC = model->index(2, 1, QModelIndex()); 
```
因为表格模型中，A,B,C的根项为最顶层节点，所以第三个参数用 QModelIndex()表示。

当模型为列表或表格结构时，使用行号、列号访问数据比较直观，所有项的父项就是顶层项，对于树状模型就比较复杂,获取B的索引为
``` cpp
QModelIndex indexA = model->index(0, 0, QModelIndex()); 
QModelIndex indexC = model->index(2, 1, QModelIndex());
QModelIndex indexB = model->index(1, 0, indexA);
```
### 设置项的数据
我们为一个项设置数据采用如下接口
``` cpp
bool QAbstractItemModel::setData(const QModelIndex &index, const QVariant &value, 
 int role = Qt::EditRole) 
```
其中，index 是项的模型索引，value 是需要设置的数据，role 是设置数据的角色

第三个参数role可以是一系列角色的并集, 角色可参考下表

![https://cdn.llfc.club/1723101654413.jpg](https://cdn.llfc.club/1723101654413.jpg)

### 获取项的数据

我们可以通过data方法获取index对应的项的数据

``` cpp
[pure virtual] QVariant QAbstractItemModel::data(const QModelIndex &index, int role = Qt::DisplayRole) const
```



## 模型基类QAbstractItemModel

QAbstractItemModel 作为模型基类，很多函数是纯虚函数，这里只做函数功能列举，大家只做眼熟即可。
- 返回行数，列数
``` cpp
int rowCount(const QModelIndex &parent = QModelIndex()) 
int columnCount(const QModelIndex &parent = QModelIndex()) 
```
- 插入和删除多行或者多列
``` cpp
bool insertRow(int row, const QModelIndex &parent = QModelIndex()) ;
bool insertRows(int row, int count, const QModelIndex &parent = QModelIndex()) ;
bool removeRow(int row, const QModelIndex &parent = QModelIndex()) ;
bool removeRows(int row, int count, const QModelIndex &parent = QModelIndex()) ;

bool insertColumn(int column, const QModelIndex &parent = QModelIndex()) ;
bool insertColumns(int column, int count, const QModelIndex &parent = QModelIndex()) ;
bool removeColumn(int column, const QModelIndex &parent = QModelIndex()) ;
bool removeColumns(int column, int count, const QModelIndex &parent = QModelIndex()) ;
```
- 移动行或者列
``` cpp
bool moveRow(const QModelIndex &sourceParent, int sourceRow, 
 const QModelIndex &destinationParent, int destinationChild) ;
bool moveColumn(const QModelIndex &sourceParent, int sourceColumn, 
 const QModelIndex &destinationParent, int destinationChild) ;
```

- 数据排序

``` cpp
//函数 sort()将数据按某一列排序，可指定排序方式，默认是升序方式。
void sort(int column, Qt::SortOrder order = Qt::AscendingOrder) ;
```
- 设置和读取项的数据
``` cpp
//函数 setData()为一个项设置数据，函数 data()返回一个项的数据，其函数原型定义如下：
bool setData(const QModelIndex &index, const QVariant &value, int role = Qt::EditRole) 
QVariant data(const QModelIndex &index, int role = Qt::DisplayRole) ;
```
- 清除一个项的数据
``` cpp
//函数 clearItemData()用于清除一个项的所有角色的数据，函数定义如下：

bool clearItemData(const QModelIndex &index)
```

## 视图基类 QAbstractItemView

视图类是控制数据显示的，同样有一个纯虚类QAbstractitemView， 它的方法大家只做理解即可，不用死记硬背，后面我们会根据具体的子类和案例带着大家学会这些操作。

- 设置和返回模型
``` cpp
void setModel(QAbstractItemModel *model) //设置数据模型
QAbstractItemModel *model() //返回关联的数据模型对象指针
```
- 获取选中的模型

``` cpp
QItemSelectionModel *selectionModel() const;
```

- 设置代理

``` cpp
// 设置代理
void  setItemDelegate(QAbstractItemDelegate *delegate);
// 为某一列设置代理
void  setItemDelegateForColumn(int column, QAbstractItemDelegate *delegate)
// 为某一行设置代理
void  setItemDelegateForRow(int row, QAbstractItemDelegate *delegate)
```

- 设置属性和获取属性

``` cpp
void setEditTriggers(QAbstractItemView::EditTriggers triggers) 
QAbstractItemView::EditTriggers editTriggers() 
```
属性值的类型为该属性值是标志类型 QAbstractItemView::EditTriggers， 它可以是几种枚举类型的并集

    - NoEditTriggers：不允许编辑。
    - CurrentChanged：当前项变化时进入编辑状态。
    - DoubleClicked：双击一个项时进入编辑状态。
    - SelectedClicked：点击一个已选择的项时进入编辑状态。
    - EditKeyPressed：当平台的编辑按键被按下时进入编辑状态

视图组件类和模型类都没有 readonly 属性，如果要设置数据是只读的，用函数 setEditTriggers()
设置视图组件为不允许编辑即可。

- 设置选择模式
``` cpp
void  setSelectionMode(QAbstractItemView::SelectionMode mode);
```
选择模式包括以下

``` cmd
SingleSelection：    单选，只能选择一个项，例如只能选择一个单元格。
ContiguousSelection：连续选择，例如按住 Shift 键选择多个连续单元格。
ExtendedSelection：  扩展选择，例如可以按住 Ctrl 键选择多个不连续的单元格。
MultiSelection：     多选，例如通过拖动鼠标选择多个单元格。
NoSelection：        不允许选择
```
- 设置选择模式

  有时我们可以设置选择整行或者多行

``` cpp
void setSelectionBehavior(QAbstractItemView::SelectionBehavior behavior)
```

选择模式包括

``` cmd
QAbstractItemView::SelectItems:  选择任意单元格
QAbstractItemView::SelectRows：   整行选择
QAbstractItemView::SelectColumns： 整列选择
```



## QStringListModel 和 QListView

QStringListModel 是处理字符串列表的模型类，其实例可以作为 QListView 组件的数据模型。 结合使用这两个类，就可以在界面上显示和编辑字符串列表, 使用需包含`<QStringListModel>`和`<QListView>`

效果如下图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267289672627.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267289672627.png)

**思路**

我们点击AddItem，会弹出提示框提示用户输入，然后将输入的内容插入到listview中。

弹出提示框可以用QInputDialog的静态函数getText

``` cpp
static QString getText(QWidget *parent, const QString &title, const QString &label,
                           QLineEdit::EchoMode echo = QLineEdit::Normal,
                           const QString &text = QString(), bool *ok = nullptr,
                           Qt::WindowFlags flags = Qt::WindowFlags(),
                           Qt::InputMethodHints inputMethodHints = Qt::ImhNone);
```

parent表示创建的提示框的父窗口

title表示提示框的标题

label表示提示框显示的内容

echo时提示框输入模式，用默认的就好

ok为true表示点击确认，否则表示取消

后面flags和inputMethodHints表示模式，用默认的就好。



点击删除Remove Item按钮，会判断当前项是否有效，有效则删除

同学们先看我完成这个案例后自己重做一遍，作为理解。

**开发讲解**

1  添加一个StringListView类，继承自QWidget

``` cpp
class StringListView : public QWidget
{
    Q_OBJECT
public:
    explicit StringListView(QWidget *parent = nullptr);

signals:

public slots:
};
```

2  StringListView类新增私有成员model和view, 并且添加增加和删减条目的槽函数

``` cpp
public slots:
    void addItem();
    void removeItem();
private:
    QStringListModel * model;
    QListView * listView;
```

3 实现StringListView的构造函数，通过布局管理列表显示和按钮，链接按钮点击信号实现增删条目的逻辑

``` cpp
StringListView::StringListView(QWidget *parent) : QWidget(parent)
{
    // 创建 QStringListModel
    model = new QStringListModel(this);
    QStringList stringList;
    stringList << "Item 1" << "Item 2" << "Item 3";
    model->setStringList(stringList);

    // 创建 QListView
    listView = new QListView(this);
    listView->setModel(model);

    // 创建添加和删除按钮
    QPushButton *addButton = new QPushButton("Add Item", this);
    QPushButton *removeButton = new QPushButton("Remove Item", this);

    // 连接信号和槽
    connect(addButton, &QPushButton::clicked, this, &StringListView::addItem);
    connect(removeButton, &QPushButton::clicked, this, &StringListView::removeItem);

    // 布局
    QVBoxLayout *layout = new QVBoxLayout(this);
    layout->addWidget(listView);
    layout->addWidget(addButton);
    layout->addWidget(removeButton);
    setLayout(layout);
}
```

4 添加条目和删除条目逻辑

``` cpp
//添加条目
void StringListView::addItem()
{
    bool ok;
    //弹出一个输入框，接受用户输入
    QString text = QInputDialog::getText(this, tr("Add Item"),
                                          tr("Item name:"), QLineEdit::Normal,
                                          "", &ok);
    //判断文本是否为空，不为空则更新列表
    if (ok && !text.isEmpty()) {
        QStringList currentList = model->stringList();
        currentList << text; // 添加新项
        model->setStringList(currentList); // 更新模型
    }
}

//删除item
void StringListView::removeItem()
{
    //根据当前索引，删除当前项
    QModelIndex index = listView->currentIndex();
    if (index.isValid()) {
        QStringList currentList = model->stringList();
             currentList.removeAt(index.row()); // 移除选中项
              model->setStringList(currentList); // 更新模型
    }
}

```

在main.cpp中添加listview的展示

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    StringListView listview;
    listview.show();

    return a.exec();
}
```



## QStandardItemModel 和 QTableView
**概念和方法**

QStandardItemModel 是以项为基本数据单元的模型类，每个项是一个 QStandardItem 对象。

使用时需包含`<QMainWindow>`和`<QStandardItem>`头文件

这部分的方法和内容比较庞杂，快速过一遍，然后零帧起手做个案例，带着大家理解一下。

- 设置行数和列数
QStandardItemModel 以二维数组的形式存储项数据，所以可以设置行数和列数。
``` cpp
void setRowCount(int rows) //设置数据模型的行数
void setColumnCount(int columns) //设置数据模型的列数
```
如果设置的列数大于 1，模型就是表格模型；如果设置的列数为 1，模型就可以看作列表模型。
- 设置项

``` cpp
void setItem(int row, int column, QStandardItem *item)
void setItem(int row, QStandardItem *item) //用于列表模型
```
- 获取项

``` cpp
QStandardItem *item(int row, int column = 0) //根据行号和列号返回项
QStandardItem *itemFromIndex(const QModelIndex &index) //根据模型索引返回项

//函数 indexFromItem()根据项返回其模型索引，其定义如下：
QModelIndex indexFromItem(const QStandardItem *item)
```
- 添加行或列
``` cpp
void appendRow(const QList<QStandardItem *> &items) //用于表格模型
void appendRow(QStandardItem *item) //用于列表模型
```
- 插入行或列

``` cpp
void insertRow(int row, const QList<QStandardItem *> &items) //用于表格模型
void insertRow(int row, QStandardItem *item) //用于列表模型
```

**案例学习**

实现表格数据展示 demo， 如下图所示

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267393278667.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267393278667.png)

**开发讲解**

**1  初步实现**

为了实现QTableview和QStandarditemModel的组合，我们在MainWindow中添加成员tableView和model

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;
    //用表格的方式展现数据
    QTableView *tableView;
    //用标准模型基类存储数据
    QStandardItemModel *model;
};
```

实现构造函数

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    // 设置窗口标题和大小
    setWindowTitle("QStandardItemModel 与 QTableView 教学案例");
    resize(600, 400);
	// 创建表格视图
    tableView = new QTableView(this);
    // 创建模型
    model = new QStandardItemModel(this);
    // 设置表格视图为中心部件
    this->setCentralWidget(tableView);
    // 初始化模型
    model->setHorizontalHeaderLabels({"姓名", "年龄", "职业"});

    // 添加数据
    QList<QStringList> data = {
        {"张三", "25", "工程师"},
        {"李四", "30", "设计师"},
        {"王五", "28", "教师"},
        {"赵六", "22", "学生"}
    };

    for (const QStringList &rowData : data) {
        QList<QStandardItem*> items;
        for (const QString &field : rowData) {
            QStandardItem *item = new QStandardItem(field);
            //设置文字居中
            item->setTextAlignment(Qt::AlignCenter);
            items.append(item);
        }
        model->appendRow(items);
    }

    // 设置模型到视图
    tableView->setModel(model);

    // 设置列宽自适应内容
    tableView->horizontalHeader()->setSectionResizeMode(QHeaderView::ResizeToContents);

    // 允许编辑
    tableView->setEditTriggers(QAbstractItemView::DoubleClicked | QAbstractItemView::SelectedClicked);

    // 启用排序功能
    tableView->setSortingEnabled(true);

}
```



运行后可以看到通过tableview和model组合，可以实现显示表格数据显示

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267334368644.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17267334368644.png)

**2  实现增删**

我们在MainWindow中增加槽函数的声明，以及新增两个按钮

``` cpp
private slots:
    //增加行
    void insertRow();
    //删除行
    void deleteRow();
private:
	QPushButton *insertButton;
    QPushButton *deleteButton;
```

完善MainWindow的构造函数列表，将model, tableview, 以及按钮的创建放在构造列表中，注意原来在构造函数中创建的要删除

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),
    tableView(new QTableView(this)),
    model(new QStandardItemModel(this)),
    insertButton(new QPushButton("插入行",this)),
    deleteButton(new QPushButton("删除行",this)){
        //...省略
    }
```

另外我们需要创建一个QWidget用来做中心部件的显示，将原来tableview设为中心部件的逻辑注释掉，

 并且基于中心部件创建一个垂直布局，

垂直布局里放入tableview和一个水平布局，水平布局里再加入两个按钮。

``` cpp
// 创建一个中心widget
QWidget *centralWidget = new QWidget(this);
// 基于中心widget创建垂直布局作为主布局
QVBoxLayout *mainLayout = new QVBoxLayout(centralWidget);
// 向布局中加入tableview
mainLayout->addWidget(tableView);
// 创建按钮布局为水平布局
QHBoxLayout *buttonLayout = new QHBoxLayout();
// 加个伸缩因子，也就是弹簧，保证按钮被挤压到右侧
buttonLayout->addStretch(); // 右对齐按钮
//添加插入按钮
buttonLayout->addWidget(insertButton);
//添加删除按钮
buttonLayout->addWidget(deleteButton);
//将按钮布局加入到主布局里
mainLayout->addLayout(buttonLayout);
//最后设置中心部件为中心widget
setCentralWidget(centralWidget);

// 连接信号与槽
connect(insertButton, &QPushButton::clicked, this, &MainWindow::insertRow);
connect(deleteButton, &QPushButton::clicked, this, &MainWindow::deleteRow);
```

实现插入行的逻辑

``` cpp
void MainWindow::insertRow()
{
    // 获取当前行数
    int row = model->rowCount();

    // 可以选择在特定位置插入，这里选择在末尾插入
    QList<QStandardItem*> items;
    // 提示用户输入新行的数据
    bool ok;
    //获取用户姓名
    QString name = QInputDialog::getText(this, "插入行", "请输入姓名:", QLineEdit::Normal, "", &ok);
    if (!ok || name.isEmpty()) return;
    //获取用户年龄
    QString age = QInputDialog::getText(this, "插入行", "请输入年龄:", QLineEdit::Normal, "", &ok);
    if (!ok || age.isEmpty()) return;
    //获取用户职业
    QString profession = QInputDialog::getText(this, "插入行", "请输入职业:", QLineEdit::Normal, "", &ok);
    if (!ok || profession.isEmpty()) return;

    auto name_item = new QStandardItem(name);
    name_item->setTextAlignment(Qt::AlignCenter);

    auto age_item = new QStandardItem(age);
    age_item->setTextAlignment(Qt::AlignCenter);

    auto profession_item = new QStandardItem(profession);
    profession_item->setTextAlignment(Qt::AlignCenter);

    items.append(name_item);
    items.append(age_item);
    items.append(profession_item);

    model->appendRow(items);

    // 可选：自动调整列宽
    tableView->resizeColumnsToContents();
}
```

实现删除逻辑

``` cpp
//删除行
void MainWindow::deleteRow()
{
    // 获取当前选中的行
     QModelIndexList selectedIndexes = tableView->selectionModel()->selectedRows();
     if (selectedIndexes.isEmpty()) {
         QMessageBox::warning(this, "删除行", "请先选择要删除的行！");
         return;
     }

     // 确认删除
     auto reply = QMessageBox::question(this, "删除行", "确定要删除选中的行吗？",
                                       QMessageBox::Yes|QMessageBox::No);
     // 取消则返回
     if (reply != QMessageBox::Yes) {
         return;
     }

     QList<int> rows;
     //selectedIndexes存储的时索引列表，可以根据索引获取行号
     for(const QModelIndex& index: selectedIndexes){
        //根据ModelIndex获取行号, 放入列表
         rows.append(index.row());
     }

     //对行号从大到小排序，因为删除要从下往上删除
     //从行号大的向上删除，保证其他待删行号不会受影响
     //greater为仿函数，接受两个参数实现从大到小排序
     std::sort(rows.begin(),rows.end(),std::greater<int>());

     // 删除选中的行，从后往前删
     for(auto row: rows){
        model->removeRow(row);
     }
}
```



## 自定义代理

同学们也注意到了，我们实现模型和视图，但是显示的内容都是文字化的，有时候我想实现特定的显示，比如在双击某个单元格后显示的是一个编辑器，有时候是一个下拉列表，那该怎么办呢？

我们可以通过自定义代理实现，前面我们提到了三要素，其中Delegate就是用来管理数据显示和编辑的。

### QStyledItemDelegate 

QAbstractItemDelegate类是所有代理类的基类，我们不用关注，我们要实现自己的代理，需要继承的是QStyledItemDelegate

QStyledItemDelegate 是视图组件使用的默认代理类，一般使用 QStyledItemDelegate 作为自定 义代理类的父类。要自定义一个代理类，必须重新实现 QStyledItemDelegate 中定义的 4 个虚函数。 这 4 个函数是由模型/视图系统自动调用的。

**1．函数 createEditor()  **

函数 createEditor()可创建用于编辑模型数据的界面组件，称为代理编辑器，例如 QSpinBox 组件，或 QComboBox 组件。其函数原型定义如下：

``` cpp
QWidget *QStyledItemDelegate::createEditor(QWidget *parent,  const QStyleOptionViewItem &option, const QModelIndex &index)  
```

 其中，parent 是要创建的组件的父组件，一般就是窗口对象；

option 是项的一些显示选项，是 QStyleOptionViewItem 类型的，包含字体、对齐方式、背景色等属性；

index 是项在数据模型中的 模型索引，通过 index->model()可以获取项所属数据模型的对象指针。

 在 QTableView 视图组件上双击一个单元格使其进入编辑状态时，系统就会自动调用 createEditor()创建代理编辑器，例如创建 QSpinBox 组件，然后将其显示在单元格里。

**2．函数 setEditorData()**  

函数 setEditorData()的功能是从数据模型获取项的某个角色（一般是 EditRole 角色）的数据， 然后将其设置为代理编辑器上显示的数据。

其函数原型定义如下：

``` cpp 
void QStyledItemDelegate::setEditorData(QWidget *editor, const QModelIndex &index)
```

 设置了自定义代理后 单元格处于编辑状态的效果 ，参数 editor 就是前面用函数 createEditor()创建的代理编辑器。

通过 index->model()可以获取项 所属数据模型的对象指针，从而获取项的数据，然后将其显示在代理编辑器上。

**3．函数 setModelData()**  

完成对当前单元格的编辑，例如输入焦点移到其他单元格时，系统会自动调用函数 setModelData()， 其功能是将代理编辑器里的输入数据保存到数据模型的项里。

其函数原型定义如下： 

``` cpp
void QStyledItemDelegate::setModelData(QWidget *editor, QAbstractItemModel *model,  const QModelIndex &index) 
```

 其中，editor 是代理编辑器，model 是数据模型，index 是所编辑的项在模型中的模型索引。

 **4．函数 updateEditorGeometry()**  

视图组件在界面上显示代理编辑器时，需要调用 updateEditorGeometry()函数为组件设置合适 的大小，例如在一个单元格里显示一个 QSpinBox 代理编辑器时，一般将其设置为单元格的大小。 

其函数原型定义如下：

``` cpp
 void QStyledItemDelegate::updateEditorGeometry(QWidget *editor,  const QStyleOptionViewItem &option, const QModelIndex &index)  
```

其中，变量 option->rect 是 QRect 类型，表示代理编辑器的建议大小。一般将代理编辑器大小设 置为建议大小即可，即用下面的一行代码：

``` cpp
 editor->setGeometry(option.rect);
```

### 定制化显示和编辑案例

**样式要求**

1  要求实现自定义的代理，完成姓名，年龄，以及职业的编辑。

2  双击姓名进行编辑，弹出编辑框

3  双击年龄进行编辑，弹出spinbox

4  双击职业进行编辑，弹出下拉框

如下图：

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726799773788.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1726799773788.png)

**开发讲解**

**1 声明自定义的代理类CustomDelegate**

``` cpp
class CustomDelegate : public QStyledItemDelegate
{
    Q_OBJECT
public:
    //构造函数
    CustomDelegate(QObject *parent = nullptr);
    //创建编辑器
    QWidget *createEditor(QWidget *parent,
                          const QStyleOptionViewItem &option,
                          const QModelIndex &index) const override;

    //设置编辑器的数据
    void setEditorData(QWidget *editor, const QModelIndex &index) const override;

    //将编辑器的数据设置到模型
    void setModelData(QWidget *editor,
                      QAbstractItemModel *model,
                      const QModelIndex &index) const override;

    //设置编辑器的尺寸匹配单元格
    void updateEditorGeometry(QWidget *editor,
                              const QStyleOptionViewItem &option,
                              const QModelIndex &index) const override;
};
```

构造函数的参数模仿基类`QStyledItemDelegate`添加了parent参数，另外声明了实现代理的必备的四个成员函数

**2 实现构造函数**

``` cpp
CustomDelegate::CustomDelegate(QObject *parent):QStyledItemDelegate (parent)
{

}
```

因为基类需要parent参数来构造，所以子类调用了基类的构造函数。

**3 创建编辑器**

实现createEditor函数，目的是为了在用户双击不同的单元格时，弹出不同的控件。

``` cpp
//实现双击的时候创建不同的控件
QWidget *CustomDelegate::createEditor(QWidget *parent, const QStyleOptionViewItem &option,
                                      const QModelIndex &index) const
{
    //姓名在第0列，年龄在第1列，职业在第2列
    //获取index对应的列数
    auto column = index.column();
    if(column == 0){
        //双击name列的时候创建一个QLineEdit
        QLineEdit * editor = new QLineEdit(parent);
        //设置最大长度
        editor->setMaxLength(50);
        return editor;
    }

    //如果年龄这一列被点击
    if(column == 1){
        //创建spinbox管理年龄
        QSpinBox* spinBox = new QSpinBox(parent);
        //设置合理的年龄范围
        spinBox->setRange(0,150);
        return spinBox;
    }

    //如果点击的是职业这一列
    if(column == 2){
        //创建下拉框comboBox
        QComboBox* comboBox = new QComboBox(parent);
        //添加职业选项
        comboBox->addItems({"工程师","设计师","教师","学生","法师"});
        return comboBox;
    }

    //条件都不满足，调用基类默认的处理方式
    return QStyledItemDelegate::createEditor(parent,option,index);
}
```

根据列号 (`index.column()`)，返回不同类型的编辑器：



- **姓名（第0列）**：`QLineEdit`，用于输入文本。可以设置最大长度以限制输入。
- **年龄（第1列）**：`QSpinBox`，用于输入数值，设置合理的范围（如0-150）。
- **职业（第2列）**：`QComboBox`，提供下拉菜单供选择预定义的职业。

**4 将模型数据设置到控件**

为了将模型数据设置到控件，我们需要使用setEditorData函数, 同样根据不同的列采用不同的设置方式

``` cpp
//将模型的数据设置到editor中
void CustomDelegate::setEditorData(QWidget *editor, const QModelIndex &index) const
{
    //根据index获取模型，再根据模型获取数据，
    //因为我们想获取可编辑类型，所以传递Qt::EditRole
    QVariant value = index.model()->data(index, Qt::EditRole);
    //获取列数
    auto column = index.column();
    //根据列数判断，如果列数为0则向编辑器中设置姓名数据
    if(column == 0){
        //需要将eitor由QWidget*转化为QLineEdit*
        auto * lineEdit = qobject_cast<QLineEdit*>(editor);
        if(lineEdit){
            //将名字设置到lineEdit里
            lineEdit->setText(value.toString());
        }
        return;
    }

    //如果是年龄列，则将数据设置到spinBox中
    if(column == 1){
        //将editor转为QSpinBox
        QSpinBox *spinBox = qobject_cast<QSpinBox*>(editor);
        if (spinBox) {
            //设置年龄
            spinBox->setValue(value.toInt());
        }
        return;
    }

    //如果是职业，则从下拉框寻找对应文本，并设置索引
    if(column == 2){
        //转化为下拉框
        QComboBox* comboBox = qobject_cast<QComboBox*>(editor);
        if(comboBox){
            int idx = comboBox->findText(value.toString());
            if(idx >= 0){
                //如果找到了就设置索引
                comboBox->setCurrentIndex(idx);
            }
        }

        return;
    }


    //都不满足，调用基类默认的函数
    QStyledItemDelegate::setEditorData(editor, index);
    return;
}
```

将模型中的数据设置到编辑器中：

- **姓名**：将文本设置到 `QLineEdit`。
- **年龄**：将数值设置到 `QSpinBox`。
- **职业**：将当前文本设置到 `QComboBox` 中的对应项。

**5 将修改写入模型中**

我们编辑完数据后，需要将修改写入模型中，此时采用setModelData即可

``` cpp
//将控件内容设置到model中
void CustomDelegate::setModelData(QWidget *editor, QAbstractItemModel *model, const QModelIndex &index) const
{
    //获取列数
    auto column = index.column();
    //设置姓名改变到model中
    if(column == 0){
        auto * lineEdit = dynamic_cast<QLineEdit*>(editor);
        if(lineEdit){
            //设置当前文本到model中
            model->setData(index,lineEdit->text(),Qt::EditRole);
        }
        return;
    }

    //设置年龄改变到model中
    if(column == 1){
        auto * spinBox = dynamic_cast<QSpinBox*>(editor);
        if(spinBox){
            //设置spinbox的值到model中
            model->setData(index,spinBox->value(),Qt::EditRole);
        }
       return;
    }

    //设置职业改变到model中
    if(column == 2){
        auto * comboBox = dynamic_cast<QComboBox*>(editor);
        if(comboBox){
            //设置下拉框文本到model中
            model->setData(index,comboBox->currentText(),Qt::EditRole);
        }
        return;
    }

    //都不满足，调用基类默认的设置
    QStyledItemDelegate::setModelData(editor,model,index);
}
```

将编辑器中的数据保存回模型：

- **姓名**：从 `QLineEdit` 获取文本并设置到模型中。
- **年龄**：从 `QSpinBox` 获取数值并设置到模型中。
- **职业**：从 `QComboBox` 获取当前选中的文本并设置到模型中。



**6 更新编辑框区域**

我们需要更新编辑区域的大小，防止区域过大或者过小，采用updateEditorGeometry函数

``` cpp
void CustomDelegate::updateEditorGeometry(QWidget *editor, const QStyleOptionViewItem &option, const QModelIndex &index) const
{
    //设置编辑器几何区域，使其不超过单元格大小
    editor->setGeometry(option.rect);
}

```

**7 将代理应用到特定的列**

在 `MainWindow` 的构造函数中，需要实例化 `CustomDelegate` 并将其应用到 `QTableView` 的特定列。可以选择应用到整个视图，也可以仅应用到特定的列。

因为我们在代理中判断了不同列的处理，所以我们将代理直接应用到整个视图即可，在mainwindow中添加

``` cpp
// 创建自定义代理
auto * custom_delegate = new CustomDelegate(this);
// 设置代理
tableView->setItemDelegate(custom_delegate);
```

## 拓展知识

### 工作中为什么使用自定义模型

使用 `QStandardItemModel` 虽然方便，但当你的数据量较大或者需要更精细控制数据行为时，性能和灵活性可能会受到限制。通过创建自定义模型，你可以：

- **优化性能**：仅实现你需要的方法，减少不必要的开销。
- **更好地控制数据**：定义专门的数据结构，更符合业务需求。
- **扩展功能**：实现特殊的数据处理或数据验证逻辑。

### 自定义模型注意事项

在 Qt 中，如果你有一个自定义的模型，并且需要手动管理数据的插入和删除，那么你确实需要在相应的方法中调用 `beginInsertRows` 和 `endInsertRows` 以插入新行，调用 `beginRemoveRows` 和 `endRemoveRows` 以删除行。这些函数的作用是通知视图（如 `QTableView` 或 `QListView`）即将发生的数据变化，确保视图能够正确更新。

**为什么系统模型不需要手动调用这些方法？**

当使用 Qt 提供的系统模型（如 `QStringListModel`、`QStandardItemModel` 等）时，这些模型已经实现了内部的管理机制。它们在添加、删除或更新数据时会自动调用 `beginInsertRows`、`endInsertRows`、`beginRemoveRows` 和 `endRemoveRows`。因此，用户不需要手动干预，只需调用相应的方法（如 `insertRow()`、`removeRow()` 等），系统模型会自动处理这些通知。

在 Qt 中，自定义模型类时，通常需要继承 `QAbstractItemModel` 类，并实现一些纯虚函数，以定义数据模型的行为。根据 Qt 的文档，子类化模型需要实现的函数可以分为以下几类：

### **自定义模型需要实现的核心函数**

当你创建一个自定义模型，通常会继承自 `QAbstractTableModel` 或 `QAbstractListModel`。对于表格数据（如姓名、年龄、职业），`QAbstractTableModel` 是更合适的选择。以下是创建自定义模型时通常需要实现的核心函数：

**1 必须实现的纯虚函数**

这些函数是 `QAbstractTableModel` 的纯虚函数，必须在自定义模型中实现：

- **`rowCount`**: 返回模型中的行数。
- **`columnCount`**: 返回模型中的列数。
- **`data`**: 根据给定的 `QModelIndex` 和角色（例如显示、编辑）返回对应的数据。



**2 推荐实现的函数**

为了使模型支持编辑、插入、删除等功能，还应实现以下函数：

- **`setData`**: 允许模型的数据被修改。
- **`flags`**: 设置每个单元格的属性（如是否可编辑）。
- **`headerData`**: 设置行/列的头部标签。
- **`insertRows`**: 实现插入新行的逻辑。
- **`removeRows`**: 实现删除行的逻辑。



**3 可选实现的函数**

根据需要，特别是当数据结构发生大规模变化时，可以实现：

- **`resetModel`**（使用 `beginResetModel` 和 `endResetModel`）: 当模型的数据发生重大变化时使用，如整体更换数据源。



### 自定义模型实现案例

我们可以通过自定义模型，将之前的信息表重新实现

**1 创建Person.h用来存储用户信息**

``` cpp
class Person
{
public:
    Person();
    QString _name;
    int _age;
    QString _profession;
};
```

Person.cpp中实现构造函数

``` cpp
Person::Person():_name(""),_age(0),_profession("")
{

}

Person::Person(QString name, int age, QString profession)
    :_name(name),_age(age),_profession(profession)
{

}
```

**2 创建自定义模型类**

因为我们是用QTableView展示数据，那配套的数据是QAbstractTableModel(表格数据)最为合适，所以我们定义的模型类要继承这个模型类

我们右键QT项目选择新建模型类PeopleModel,  先定义PeopleModel类并声明成员函数

``` cpp
class PeopleModel : public QAbstractTableModel
{
    Q_OBJECT
public:
    explicit PeopleModel(QObject* parent = nullptr);
    //必须实现的纯虚函数
    //返回行数
   int rowCount(const QModelIndex &parent = QModelIndex()) const override;
   //返回列数
   int columnCount(const QModelIndex &parent = QModelIndex()) const override;
   // 获取数据
   QVariant data(const QModelIndex &index, int role = Qt::DisplayRole) const override;
   // 设置数据
   bool setData(const QModelIndex &index, const QVariant &value, int role = Qt::EditRole) override;
   // 返回索引项对应的标记
   Qt::ItemFlags flags(const QModelIndex &index) const override;
   // 返回头部各列数据
   QVariant headerData(int section, Qt::Orientation orientation,
                         int role = Qt::DisplayRole) const override;
   //插入和删除行会调用如下函数
   bool insertRows(int row, int count, const QModelIndex &parent = QModelIndex()) override;
   bool removeRows(int row, int count, const QModelIndex &parent = QModelIndex()) override;
   //重置整个模型数据
   void resetData(const QList<Person> &newPeople);
private:
    QList<Person> _people;
};
```

**3 实现PeopleModel构造函数**

``` cpp
PeopleModel::PeopleModel(QObject *parent)
    :QAbstractTableModel(parent)
{
    // 初始化一些示例数据
    _people.append(Person{"张三", 25, "工程师"});
    _people.append(Person{"李四", 30, "设计师"});
    _people.append(Person{"王五", 28, "教师"});
    _people.append(Person{"赵六", 22, "学生"});
}
```

**4 返回行数和列数**

``` cpp
int PeopleModel::rowCount(const QModelIndex &parent) const
{
    Q_UNUSED(parent)
    //返回QList中元素的个数
    return _people.count();
}

int PeopleModel::columnCount(const QModelIndex &parent) const
{
    Q_UNUSED(parent)
    //返回列数
    return 3;
}

```

**5 返回index对应的表格模型数据**

``` cpp
//返回index对应的数据
QVariant PeopleModel::data(const QModelIndex &index, int role) const
{
    //先判断索引是否有效
    if(!index.isValid()){
        return QVariant();
    }

    //判断行号是不是超过最大行,因为index的row是从0开始的
    if(index.row() >= _people.count() || index.row() < 0){
        return QVariant();
    }

    //获取索引对应的行号，再根据行号获取对应人物数据
    auto & person = _people[index.row()];

    // 如果role不是表现角色并且不是可编辑的，就直接返回无效数据
    if(role != Qt::DisplayRole && role != Qt::EditRole){
        return QVariant();
    }

    //判断列数
    auto const & column = index.column();
    //第0列则返回用户名字
    if(column == 0){
        return person._name;
    }

    //第1列则返回用户年龄
    if(column == 1){
        return person._age;
    }

    //第2列则返回用户专业
    if(column == 2){
        return person._profession;
    }

    //都不满足则返回空
    return QVariant();
}
```

**6 设置用户数据**

``` cpp
//设置用户数据
bool PeopleModel::setData(const QModelIndex &index, const QVariant &value, int role)
{
    //如果索引无效，或者角色不可编辑则直接返回false，表示无需设置
    if(!index.isValid() || role != Qt::EditRole){
        return false;
    }

    //进一步判断index.row是否越界
    if(index.row() >= _people.count() || index.row() < 0){
        return false;
    }

    auto & person = _people[index.row()];

    //最后判断列数设置对应字段
    const auto & column = index.column();
    //列数索引大于等于3则直接返回
    if(column >= 3){
        return false;
    }

    //设置名字
    if(column == 0){
        person._name = value.toString();
        //通知tableview视图刷新
        //三个参数分别表示和要刷新区域的左上角的索引，右下角的索引，以及刷新的角色列表
        emit dataChanged(index,index,{role});
        return true;
    }


    //设置年龄
    if(column == 1){
        person._age = value.toInt();
        //通知tableview视图刷新
        //三个参数分别表示和要刷新区域的左上角的索引，右下角的索引，以及刷新的角色列表
        emit dataChanged(index,index,{role});
        return true;
    }


    //设置专业
    if(column == 2){
        person._profession = value.toString();
        //通知tableview视图刷新
        //三个参数分别表示和要刷新区域的左上角的索引，右下角的索引，以及刷新的角色列表
        emit dataChanged(index,index,{role});
        return true;
    }

    return false;

}
```

**7 返回项的角色**

``` cpp
//返回项的标记
Qt::ItemFlags PeopleModel::flags(const QModelIndex &index) const
{
    if (!index.isValid())
          return Qt::NoItemFlags;

      return Qt::ItemIsSelectable | Qt::ItemIsEnabled | Qt::ItemIsEditable;
}
```

如果索引无效，则返回NoItemFlags表示无效的项，否则返回可编辑，可被选择以及有效标记。

**8 返回表头数据**

根据表头返回某个列的名字

``` cpp
QVariant PeopleModel::headerData(int section, Qt::Orientation orientation,
                                 int role) const
{
    if (role != Qt::DisplayRole)
        return QVariant();

    if (orientation == Qt::Horizontal) {
        switch (section) {
        case 0:
            return tr("姓名");
        case 1:
            return tr("年龄");
        case 2:
            return tr("职业");
        default:
            return QVariant();
        }
    }else if (orientation == Qt::Vertical){

        return QString("Row %1").arg(section + 1);
    }
    return QVariant();
}
```

**9 实现插入接口**

insertRows会在model调用insertRow的时候触发，所以更新模型数据的时候要实现

``` cpp
bool PeopleModel::insertRows(int row, int count, const QModelIndex &parent)
{
    Q_UNUSED(parent);
    if (row < 0 || row > _people.size())
        return false;

    beginInsertRows(QModelIndex(), row, row + count - 1);
    for (int i = 0; i < count; ++i) {
        _people.insert(row, Person{"", 0, ""});
    }
    endInsertRows();
    return true;
}
```

**10 实现删除接口**

removeRows会在model调用removeRow的时候触发，所以更新模型的时候要实现

``` cpp
bool PeopleModel::removeRows(int row, int count, const QModelIndex &parent)
{
    Q_UNUSED(parent);
    if (row < 0 || (row + count) > _people.size())
        return false;

    beginRemoveRows(QModelIndex(), row, row + count - 1);
    for (int i = 0; i < count; ++i) {
        _people.removeAt(row);
    }
    endRemoveRows();
    return true;
}
```

**11 重置数据**

更新模型数据的时候会调用此函数

``` cpp
void PeopleModel::resetData(const QList<Person> &newPeople)
{
    beginResetModel();
    _people = newPeople;
    endResetModel();
}
```

到此模型更新完毕，为了方便演示，我们将原来的模型改为我们自定义的模型

**12 更改模型为自定义模型**

在MainWindow的声明中将model改为PeopleModel*类型

``` cpp
PeopleModel* model;
```

然后将MainWindow的构造函数中构造这个自定义模型 ， 并将之前对模型数据的初始化删除

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),
    tableView(new QTableView(this)),
    model(new PeopleModel(this)),
    insertButton(new QPushButton("插入行",this)),
    deleteButton(new QPushButton("删除行",this)){
        
    }
```

**13  新增重置按钮**

MainWindow声明处增加重置按钮，添加新的槽函数

``` cpp
//重置数据按钮
QPushButton *resetButton;
private slots:
    //重置数据
    void resetModelData();
```

MainWindow的构造函数中添加重置按钮

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),
    tableView(new QTableView(this)),
    model(new PeopleModel(this)),
    insertButton(new QPushButton("插入行",this)),
    deleteButton(new QPushButton("删除行",this)),
    resetButton(new QPushButton("重置数据", this)){
        //...
    }
```

并且MainWindow构造函数中将重置按钮放入布局，且链接信号和槽

``` cpp
//添加重置按钮
buttonLayout->addWidget(resetButton);
connect(resetButton, &QPushButton::clicked, this, &MainWindow::resetModelData);
```

**14 重新实现槽函数**

我们希望在insertRow()调用后让新插入的行的第一个单元格处于编辑状态

删除和之前没区别，获取选中的行然后删除，从后往前删

最后是重置数据直接调用模型的resetData就可以了。

``` cpp
void MainWindow::insertRow()
{
    // 在末尾插入一行
    int row = model->rowCount();
    if (model->insertRow(row)) {
        // 自动选择新插入的行并开始编辑第一个单元格（姓名）
        QModelIndex index = model->index(row, 0);
        tableView->setCurrentIndex(index);
        tableView->edit(index);
    } else {
        QMessageBox::warning(this, "插入失败", "无法插入新行！");
    }
}

//删除行
void MainWindow::deleteRow()
{
    // 获取选中的行
    QModelIndexList selected = tableView->selectionModel()->selectedRows();
    if (selected.isEmpty()) {
        QMessageBox::information(this, "提示", "请先选择要删除的行！");
        return;
    }

    // 删除从后往前
    for (int i = selected.size() - 1; i >= 0; --i) {
        if (!model->removeRow(selected.at(i).row())) {
            QMessageBox::warning(this, "删除失败", "无法删除所选择的行！");
        }
    }

}

void MainWindow::resetModelData()
{
    // 示例：重置模型数据为一个新的列表
    QList<Person> newPeople = {
        {"孙七", 35, "产品经理"},
        {"周八", 27, "测试工程师"},
        {"吴九", 29, "销售经理"}
    };
    model->resetData(newPeople);
}

```



# 第五章 事件系统

Qt 的事件系统是 Qt 应用程序与用户交互、响应系统事件以及在不同组件之间传递信息的核心机制。理解和掌握 Qt 的事件系统对于开发复杂且响应迅速的应用程序至关重要。本文将全面介绍 Qt 事件系统的各个方面，包括事件的种类、事件的分发与捕获机制、事件过滤器、事件优先级等，并通过示例代码帮助你深入理解这些概念。

## Qt 事件系统概述

Qt 的事件系统基于事件驱动编程模型。在这种模型中，应用程序的执行流程主要由事件（如用户输入、定时器触发、网络数据到达等）驱动。Qt 通过事件循环（Event Loop）不断监听并分发事件，使得应用程序能够对各种异步事件做出及时响应。

**事件循环（Event Loop）** 是 Qt 应用程序的核心组成部分。它负责检索和分发事件给相应的对象。通常情况下，`QApplication` 或 `QGuiApplication` 类的实例会启动事件循环，当调用 `exec()` 函数时，事件循环开始运行，直到程序退出。

``` cpp
#include <QApplication>
#include <QPushButton>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    QPushButton button("Hello Qt");
    button.show();

    return app.exec(); // 启动事件循环
}
```

在上述示例中，`app.exec()` 启动了事件循环，应用程序进入等待和处理事件的状态，直到用户关闭窗口或程序调用 `quit()` 退出。

## 事件的类型

Qt 定义了多种事件类型，每种事件类型对应不同的用户交互或系统行为。下面是一些常见的事件类型：



- **用户输入事件**：
  - `QEvent::MouseButtonPress`：鼠标按钮按下事件。
  - `QEvent::MouseButtonRelease`：鼠标按钮释放事件。
  - `QEvent::MouseMove`：鼠标移动事件。
  - `QEvent::KeyPress`：键盘按下事件。
  - `QEvent::KeyRelease`：键盘释放事件。
- **窗口事件**：
  - `QEvent::Show`：窗口显示事件。
  - `QEvent::Hide`：窗口隐藏事件。
  - `QEvent::Resize`：窗口大小调整事件。
  - `QEvent::Move`：窗口移动事件。
- **系统事件**：
  - `QEvent::Timer`：定时器事件。
  - `QEvent::Close`：窗口关闭事件。
- **绘图事件**：
  - `QEvent::Paint`：绘图事件。
- **自定义事件**：
  - 用户可以根据需要定义自己的事件类型，通常从 `QEvent::User` 开始编号。



**事件类型常量的定义**：



Qt 的所有事件类型都在 `QEvent::Type` 枚举中定义，如下所示：

``` cpp
enum Type {
    None = 0,
    WindowTitleChange = 0x01,
    WindowIconChange = 0x02,
    // ...
    MouseButtonPress = 0x20,
    MouseButtonRelease = 0x21,
    // ...
    KeyPress = 0x40,
    KeyRelease = 0x41,
    // ...
    User = 1000 // 自定义事件类型起始值
};
```

开发者可以通过检查事件对象的类型来确定如何处理特定事件。

## 事件的分发机制

Qt 的事件分发机制主要依赖于对象的继承关系和事件传递路径。Qt 提供了一套基于 `QObject` 的事件分发系统，使得事件能够在对象层次结构中传递。

### 1 事件分发的基本流程

1. **事件接收**：当事件发生时，事件循环会创建一个 `QEvent` 对象，表示这个事件。
2. **事件队列**：事件被放入目标对象的事件队列。
3. **事件处理**：目标对象接收事件，并决定如何处理它（重绘、响应用户输入等）。
4. **事件传递**：如果事件未被目标对象完全处理，事件可以传递到更高层的对象（如父对象）。



### 2  事件处理函数

每个 `QObject` 派生的类都可以通过重写特定的事件处理函数来响应事件。常见的事件处理函数包括：



- `bool QWidget::event(QEvent *event)`：通用事件处理函数，处理所有类型的事件。可以根据事件类型进一步分发。
- `void QWidget::mousePressEvent(QMouseEvent *event)`：处理鼠标按下事件。
- `void QWidget::keyPressEvent(QKeyEvent *event)`：处理键盘按下事件。
- `void QWidget::paintEvent(QPaintEvent *event)`：处理绘图事件。



这些事件处理函数可以被重写，以便在事件发生时执行特定的操作。

### **3 示例：重写事件处理函数**

``` cpp
#include <QApplication>
#include <QWidget>
#include <QMouseEvent>
#include <QMessageBox>

class MyWidget : public QWidget
{
protected:
    void mousePressEvent(QMouseEvent *event) override
    {
        QMessageBox::information(this, "Mouse Event",
                                 QString("Mouse pressed at (%1, %2)")
                                 .arg(event->x()).arg(event->y()));
    }

    void paintEvent(QPaintEvent *event) override
    {
        // 自定义绘图逻辑
        QPainter painter(this);
        painter.drawText(event->rect(), Qt::AlignCenter, "Hello, Qt!");
    }
};

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    MyWidget widget;
    widget.resize(300, 200);
    widget.show();

    return app.exec();
}
```

### 重写event函数

我们不仅仅可以重写指定的事件，还可以重写event函数(通用事件处理函数)，在event里根据事件类型做出判断，并且进行事件处理。

我们制作一个子部件`ChildWidget`，重新实现它的`PaintEvent`,绘制一个红色边框更显眼 

然后重写event函数，判断鼠标点击事件弹出消息框

``` cpp

class ChildWidget : public QLabel
{
public:
    ChildWidget(const QString &text, QWidget *parent = nullptr) : QLabel(text, parent)
    {
        setAlignment(Qt::AlignCenter);
    }

protected:

    void paintEvent(QPaintEvent * event) override{
        // 自定义绘图逻辑
        QPainter painter(this);
        // 设置背景颜色

        //设置画笔
        painter.setPen(QPen(Qt::red,2));

        // 绘制与控件相同大小的矩形
        painter.drawRect(rect());

        // 调用基类的 paintEvent
        QLabel::paintEvent(event);
    }

    bool event(QEvent *event) override
    {
        //如果是鼠标点击事件
        if (event->type() == QEvent::MouseButtonPress) {
            QMessageBox::information(this, "Child Event", "Child received mouse press event.");
            // 返回 false 以允许事件继续传递到父对象
            return false;
        }
        return QLabel::event(event);
    }
};
```

在main.cpp中创建这个`ChildWidget`，其父窗口为`MainWindow`,我们试试

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    w.resize(800,600);
    //创建子部件，父窗口为MainWindow
    auto * child_wid = new ChildWidget("click me",&w);
    child_wid->setGeometry(100,100,100,50);
    //注意show为阻塞函数，所以创建工作要放在show上
    w.show();
    return a.exec();
}
```

运行后点击子部件，会看到弹出消息框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172706717268.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_172706717268.png)



## 事件传递模式

Qt 的事件传递遵循一定的模式，特别是在使用继承和父子对象体系时。主要有两种事件传递方式：

1. **直接事件传递**：事件直接发送到目标对象。
2. **事件链传递（Event Chain）**：事件从目标对象传递到其父对象，直到被处理或达到顶层对象。

### 1 直接事件传递

直接事件传递是指事件被发送到指定的目标对象，并由该对象直接处理。例如，点击按钮时，事件直接发送到按钮对象。

**发送事件的方式**：

- **同步发送**：使用 `QCoreApplication::sendEvent(QObject *receiver, QEvent *event)`。事件被立即发送并处理，调用方等待处理完成。
- **异步发送**：使用 `QCoreApplication::postEvent(QObject *receiver, QEvent *event)`。事件被放入接收者的事件队列，等待事件循环处理。

这个稍后我们自定义事件的时候可以用一下，目前做个了解。

### 2 事件链传递

事件链传递是指事件在目标对象、其父对象及进一步的父对象中逐级传递，直到被处理或到达事件链的顶端。

事件链的传递顺序如下：

1. **事件过滤器**：在事件传递到目标对象之前，事件可以被安装在目标对象或其父对象上的事件过滤器拦截和处理，事件过滤器之后讲解
2. **目标对象**：首先尝试由目标对象处理事件。
3. **父对象**：如果目标对象未处理事件，事件将被传递到其父对象，依此类推，直到顶层对象（通常是 `QApplication`）。
4. **默认处理**：如果事件链上的所有对象都未处理事件，则事件最终会被系统的默认事件处理程序处理。

**注意**

要想让事件传递链生效，需要在目标对象的event处理函数里返回false，表示未处理完全，这样其父节点依次处理。

### 3 示例：事件链传递

我们定义一个ChildWidget继承自QLabel，重写paintEvent绘制区域，和event事件处理点击事件。

再定义一个ParentWiget，继承自QWidget，重写event事件处理点击事件

然后让ChildWidget成为ParentWidget的子部件

``` cpp
class ParentWidget : public QWidget
{
    Q_OBJECT
public:
    explicit ParentWidget(QWidget *parent = nullptr);
    bool event(QEvent *event) override
    {
        if (event->type() == QEvent::MouseButtonPress) {
            QMessageBox::information(this, "Parent Event", "Parent received mouse press event.");
            //返回true不向上传递
            return true;
        }
        //其他事件类型调用基类默认处理
        return QWidget::event(event);
    }
signals:

public slots:
};


class ChildWidget : public QLabel
{
public:
    ChildWidget(const QString &text, QWidget *parent = nullptr) : QLabel(text, parent)
    {
        setAlignment(Qt::AlignCenter);
    }

protected:

    void paintEvent(QPaintEvent * event) override{
        // 自定义绘图逻辑
        QPainter painter(this);
        // 设置背景颜色

        //设置画笔
        painter.setPen(QPen(Qt::red,2));

        // 绘制与控件相同大小的矩形
        painter.drawRect(rect());

        // 调用基类的 paintEvent
        QLabel::paintEvent(event);
    }

    bool event(QEvent *event) override
    {
        if (event->type() == QEvent::MouseButtonPress) {
            QMessageBox::information(this, "Child Event", "Child received mouse press event.");
            // 返回 false 以允许事件继续传递到父对象
            return false;
        }
        return QLabel::event(event);
    }
};

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    ParentWidget parent;
    parent.resize(300, 200);

    ChildWidget *child = new ChildWidget("Click Me", &parent);
    child->setGeometry(50, 50, 200, 100);

    parent.show();
    return a.exec();
}
```

在这个示例中，当用户点击标签（`ChildWidget`）时：



1. 事件首先被发送到 `ChildWidget`。
2. `ChildWidget` 的 `event` 方法处理事件，并弹出一个消息框。
3. 返回 `false`，表示事件未被完全处理，事件继续传递到其父对象 `ParentWidget`。
4. `ParentWidget` 的 `event` 方法接收同一个事件，并弹出另一个消息框。



如果将 `ChildWidget::event` 返回 `true`，事件将不会传递到 `ParentWidget`。

``` cpp
bool event(QEvent *event) override
{
    if (event->type() == QEvent::MouseButtonPress) {
        QMessageBox::information(this, "Child Event", "Child received mouse press event.");
        // 返回 true 不允许事件继续传递到父对象
        return true;
    }
    return QLabel::event(event);
}
```

## 事件过滤器

事件过滤器允许对象拦截并处理事件，而无需直接修改事件发送者的代码。通过事件过滤器，可以在更高层次上控制和监视事件。

### 1 安装事件过滤器

要使用事件过滤器，需要以下步骤：

1. **创建一个继承自 `QObject` 的过滤器类**，并重写 `eventFilter` 方法。
2. **将过滤器对象安装到目标对象上**，使用 `QObject::installEventFilter(QObject *filterObj)`。

### 2 事件过滤器的工作原理

当目标对象接收到事件时，Qt 首先调用安装在该对象上的事件过滤器的 `eventFilter` 方法。

如果事件过滤器返回 `true`，则事件被认为已经处理，目标对象不会再处理该事件。

如果返回 `false`，表示事件过滤器未完全处理这个事件，事件将继续传递到目标对象。

### 3 示例：使用事件过滤器

下面的示例展示了如何使用事件过滤器拦截按钮的鼠标点击事件，并在不影响按钮正常行为的情况下记录点击次数。

我们重写了鼠标按键事件，以及事件过滤器，分别弹出不同的消息框。

``` cpp
class MyButton : public QPushButton {
    Q_OBJECT
public:
    MyButton(QWidget *parent = nullptr):
        QPushButton(parent),clickCount(0){}

    MyButton(const QString &text, QWidget *parent = nullptr):
        QPushButton (text,parent),clickCount(0){
        this->installEventFilter(this);
    }

    //事件过滤器
    bool eventFilter(QObject *obj, QEvent *event) override
    {
        if (event->type() == QEvent::MouseButtonPress) {
            clickCount++;
            QMessageBox::information(nullptr, "Click Filter",
                                     QString("Button clicked %1 times.").arg(clickCount));
            // 返回 false 以允许事件继续传递
            return false;
        }
        // 其他事件处理
        return QPushButton::eventFilter(obj, event);
    }

    void mousePressEvent(QMouseEvent *e) override{
        QMessageBox::information(nullptr,"MousePressEvent","MousePressEvent");
        QPushButton::mousePressEvent(e);
    }

private:
    int clickCount;
};


int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;

    MyButton button("Click Me",&w);
    button.setGeometry(50,50,200,50);
    w.show();
    return a.exec();
}
```

点击按钮后会触发事件过滤器进而根据鼠标点击事件统计点击次数，并且弹窗。

有的同学可能会问，如果事件过滤器返回false和true的区别是什么？我们可以将MyButton的eventFilter改为

``` cpp
//事件过滤器
bool eventFilter(QObject *obj, QEvent *event) override
{
    if (event->type() == QEvent::MouseButtonPress) {
        clickCount++;
        QMessageBox::information(nullptr, "Click Filter",
                                 QString("Button clicked %1 times.").arg(clickCount));
        // 返回 false 以允许事件继续传递
        return false;
    }
    // 其他事件处理
    return QPushButton::eventFilter(obj, event);
}
```

再次运行程序，点击按钮，发现只会弹出事件过滤器的消息框。

## 三种事件处理方式优先级

我们学习了三种是事件处理方式

1. 重写event函数
2. 重写具体的事件函数
3. 重写事件过滤器并安装

那么这三种方式，调用的顺序会怎么样呢？

我们还是在MainWindow中创建一个按钮，然后用三种方式捕获这个按钮的点击事件，并弹出对应的信息。看看触发顺序

``` cpp
class MyButton: public QPushButton
{
    Q_OBJECT

public:
    //构造函数
    explicit MyButton(const QString &text, QWidget *parent = nullptr):
        QPushButton(text,parent){
        //装载事件过滤器
        this->installEventFilter(this);
    }

    //重写鼠标点击事件
    void mousePressEvent(QMouseEvent *e) override {
        QMessageBox::information(nullptr, "mousePressEvent",
                                 "mousePressEvent triggered!");
        return QPushButton::mousePressEvent(e);
    }
    //重写event事件
    bool event(QEvent *e) override {
        //判断是鼠标按下事件
        if(e->type() == QEvent::MouseButtonPress){
            QMessageBox::information(nullptr,"event triggered",
                                     "event MouseButtonPress triggered");
            //返回false，表示未处理完全，可以继续交给父节点处理鼠标按下事件
            return false;
        }

        //不是鼠标按下事件可以调用基类处理方式
        return QPushButton::event(e);
    }
    //重写事件过滤器
    virtual bool eventFilter(QObject *watched, QEvent *event){
        //判断是不是鼠标按下事件
        if(event->type() == QEvent::MouseButtonPress){
            //弹出消息框表示事件过滤器捕获
            QMessageBox::information(nullptr,"eventFilter triggered",
                                     "eventFilter MouseButtonPress triggered");
            //返回false，表示未处理完全，交给按钮的其他处理机制捕获
            return false;
        }

        return QPushButton::eventFilter(watched, event);
    }

};
```

可以看到event中捕获了鼠标按下事件，为了让事件继续抛给按钮的父节点处理，我们选择了返回false。

我们在main函数中调用

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    //创建按钮
    auto button = new MyButton("Click Me", &w);
    button->setGeometry(100,100,100,50);
    w.show();

    return a.exec();
}
```

运行后点击按钮，发现依次弹出两个信息框，没有触发mousePressEvent函数

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270745501737.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270745501737.png)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270746008065.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270746008065.png)

可以看出触发的顺序是eventFilter, 然后才是event.

那同学们思考下，为什么没有触发mousePressEvent吗？

因为mousePressEvent是一个虚函数，虚函数是通过基类指针调用，进而调用子类实现的，这是多态，基类调用mousePressEvent也是通过基类的event进行派发的，而我们看到在event处理函数中我们判断是鼠标点击事件后返回的是false，也就不交给基类处理了，导致无法通过基类调用派发子类功能。

所以我们将event捕获到鼠标点击事件后不再直接返回，而是继续调用基类`QPushButton`的event函数，进而调用基类的mousePressEvent,最后通过多态效果触发我们自己实现的mousePressEvent

``` cpp
//重写event事件
bool event(QEvent *e) override {
    //判断是鼠标按下事件
    if(e->type() == QEvent::MouseButtonPress){
        QMessageBox::information(nullptr,"event triggered",
                                 "event MouseButtonPress triggered");
        //不返回继续调用基类的事件派发机制
    }

    //不是鼠标按下事件可以调用基类处理方式
    return QPushButton::event(e);
}
```

这样再次调用就能看到依次弹出三个消息框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270745501737.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270745501737.png)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270746008065.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270746008065.png)

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727075117679.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727075117679.png)



## 自定义事件

我们期望实现一个窗口，里面有一个按钮，点击按钮后弹出信息，显示收到了自定义的事件

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270762478400.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270762478400.png)

**开发思路**

我们可以自定义一个事件类型，在Qt里允许我们自定义事件，在QEvent::User就是QT留给用户自定义的事件类型id，我们可以基于这个id加1自定义自己的

事件

``` cpp
// 定义自定义事件类型
const QEvent::Type MyCustomEventType = static_cast<QEvent::Type>(QEvent::User + 1);
```

自定义事件类

``` cpp
// 自定义事件类
class MyCustomEvent : public QEvent
{
public:
    // QEvent构造函数需要一个事件类型，我们自定义了一个类型
    // message为我们要记录的事件信息
    MyCustomEvent(const QString &message)
        : QEvent(MyCustomEventType), message(message) {
    }

    //添加方法获取事件信息
    QString getMessage() const { return message; }

private:
    QString message;
};
```

再自定义一个接受事件的窗口

``` cpp
// 接收自定义事件的窗口
class EventReceiver : public QWidget
{
public:
    EventReceiver(QWidget *parent = nullptr) : QWidget(parent)
    {
        resize(600,400);
        QPushButton *button = new QPushButton("Send Custom Event", this);
        QVBoxLayout *layout = new QVBoxLayout(this);
        layout->addWidget(button);
        setLayout(layout);
        //链接按钮点击事件，按钮按下后触发发送自定义事件的槽函数
        connect(button, &QPushButton::clicked, this, &EventReceiver::sendCustomEvent);
    }

protected:
    // 重写事件处理函数
    bool event(QEvent *event) override
    {
        //如果是我们自定义的事件则弹出信息并且直接返回
        if (event->type() == MyCustomEventType) {
            MyCustomEvent *customEvent = static_cast<MyCustomEvent*>(event);
            QMessageBox::information(this, "Custom Event Received", customEvent->getMessage());
            return true; // 事件已被处理
        }
        return QWidget::event(event); // 交给基类处理其他类型的事件
    }

private slots:
    void sendCustomEvent()
    {
        // 创建并发送自定义事件
        MyCustomEvent *event = new MyCustomEvent("This is a custom event!");
        // 将事件投递到对象的待处理事件队列里
        QCoreApplication::postEvent(this, event);
    }
};

```

主函数中调用自定义的窗口

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    EventReceiver receiver;
    receiver.show();

    return a.exec();
}
```

运行后，点击按钮，会在槽函数`sendCustomEvent`内派发自定义的`MyCustomEvent`事件，投递给自己

QT事件循环会从`EventReceiver`的事件队列里依次取出事件处理，每次都会触发`event`函数，当取到`MyCustomEventType`类型时，就弹出我们自定义的消息框了。

## 拓展知识

**1 多层级事件过滤**

事件过滤器不仅可以安装在目标对象上，也可以安装在父对象或更高层级的对象上。这样可以实现全局或局部的事件监控和处理。

为了方便，我们在MainWindow.h中定义一个`ClickEventFilter`类，实现`eventFilter`捕获`KeyPress`按键事件

``` cpp
class ClickEventFilter : public QObject
{
    Q_OBJECT
public:
    explicit ClickEventFilter(QObject *parent = nullptr) : QObject(parent) {}

protected:
    bool eventFilter(QObject *obj, QEvent *event) override {
        //如果是按键事件
        if (event->type() == QEvent::KeyPress) {
            //转化为按键事件
            QKeyEvent * key_event= static_cast<QKeyEvent*>(event);
            //获取对象名称
            QString objectName = obj->objectName();

            if (objectName.isEmpty()) {
                objectName = obj->metaObject()->className();
            }

            QMessageBox::information(nullptr, "Global Click Filter",
                                     QString("Pressed object: %1\n Key Text is %2\n")
                                     .arg(objectName)
                                     .arg(key_event->text()));
            // 返回 false 以允许事件继续传递
            return false;
        }
        return QObject::eventFilter(obj, event);
    }
};
```

我们在mainwindow中创建一个按钮

``` cpp
auto *pushBtn = new QPushButton("click me", this);
pushBtn->setGeometry(100,100,100,50);
```

接下来我们在main.cpp中为Application安装这个事件过滤器, 因为Application位于最顶层，所以事件过滤器安装在了最顶层，那么可以监控所有对象的事件

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    w.show();
    ClickEventFilter *filter = new ClickEventFilter(&a);
    a.installEventFilter(filter);

    return a.exec();
}
```

我们运行程序后，点击按键d，会发现依次弹出三个对话框，表明我们为最顶层app安装了过滤器达到了监听所有对象的效果。

先弹出最顶层窗口MainWindowWindow的按键消息

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727055830169.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727055830169.png)

再弹出按钮的按键消息

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270560631023.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270560631023.png)

最后弹出MainWindow的按键消息

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270562811656.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270562811656.png)



**2 多事件过滤器优先级**

一个对象可以安装不同的事件过滤器，假设我们为按钮安装了两个事件过滤器，一个高优先级的事件过滤器内部返回true，就会阻止低优先级的事件过滤器处理。

我们先实现两个等级的事件过滤器

``` cpp
//高优先级过滤器
class HighPriorityFilter : public QObject
{
    Q_OBJECT
public:
 explicit HighPriorityFilter(QObject *parent = nullptr) : QObject(parent) {}
protected:
    bool eventFilter(QObject *obj, QEvent *event) override
    {
        //判断鼠标事件
        if (event->type() == QEvent::MouseButtonPress) {
            QMessageBox::information(nullptr, "High Priority Filter",
                                     "High priority filter intercepted the click!");
            // 阻止事件继续传递
            return true;
        }
        return QObject::eventFilter(obj, event);
    }
};

//低优先级事件过滤器
class LowPriorityFilter : public QObject
{
    Q_OBJECT
public:
 explicit LowPriorityFilter(QObject *parent = nullptr) : QObject(parent) {}
protected:
    bool eventFilter(QObject *obj, QEvent *event) override
    {
        //鼠标按下事件
        if (event->type() == QEvent::MouseButtonPress) {
            QMessageBox::information(nullptr, "Low Priority Filter",
                                     "Low priority filter intercepted the click!");
            // 允许事件继续传递
        }
        return QObject::eventFilter(obj, event);
    }
};

```

接下来我们在MainWindow的构造函数里创建按钮，并为它安装这两个过滤器，最后安装的最先触发

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    auto *pushBtn = new QPushButton("click me", this);
    pushBtn->setGeometry(100,100,100,50);
    //注意安装顺序，最后安装的被认为是最先触发的
    auto * low_filter = new LowPriorityFilter(pushBtn);
    pushBtn->installEventFilter(low_filter);
    //最后安装的最先触发，被认为是高级事件过滤器
    auto * high_filter = new HighPriorityFilter(pushBtn);
    pushBtn->installEventFilter(high_filter);
}
```

运行程序，点击按钮，会发现只弹出高级事件过滤器的消息框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270586098269.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270586098269.png)

如果我们将`HighPriorityFilter`的`eventFilter`内部的逻辑改为返回false，就表示这个事件过滤器未完全处理好这个事件，可以继续交给其他事件过滤器处理

我们点击按钮后，会先弹出High priority filter，再弹出下面的消息框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270597742675.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270597742675.png)







# 第六章 对话框

## 1. 对话框简介



**对话框（Dialog）** 是一种弹出式窗口，用于与用户进行交互，传递信息或获取用户输入。在 Qt 中，对话框广泛用于提示信息、获取输入、设置选项等。

- **模态对话框（Modal Dialog）**：在显示期间，禁止用户与其他窗口进行交互，用户必须先关闭对话框才能操作主窗口。
- **非模态对话框（Non-Modal Dialog）**：允许用户在对话框显示的同时，与其他窗口进行交互。



## 2. 对话框类型

### 模态对话框

- **QMessageBox**：用于显示信息、警告、错误或提问等消息。
- **QInputDialog**：用于获取用户输入，如文本、数字等。
- **QFileDialog:** 用于打开文件
- **QProgressDialog:** 进度对话框，用来显示进度
- **QDialog**：用于创建自定义的对话框。



### 非模态对话框

可以使用 `show()` 方法显示非模态对话框，与主窗口同时存在且可交互。

## 3. 常用对话框类

### 1 QMessageBox

`QMessageBox` 提供了标准的对话框用于显示信息、警告、错误和提问。

**常用方法：**

- `information(QWidget *parent, const QString &title, const QString &text, ...)`
- `warning(QWidget *parent, const QString &title, const QString &text, ...)`
- `critical(QWidget *parent, const QString &title, const QString &text, ...)`
- `question(QWidget *parent, const QString &title, const QString &text, ...)`

**案例**

创建一个MainWindow，在MainWindow里添加几个按钮，每个按钮点击后显示不同的QMessageBox，比如按下了警告按钮，就弹出警告信息。如下图

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270796898695.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270796898695.png)

**开发思路**

在MainWindow构造函数里调整大小，并且增加垂直布局，将四个按钮加入布局中，并且链接点击信号和槽函数，在槽函数里弹出不同的消息框

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    //重置大小
    this->resize(600,400);
    //设置中心部件
    QWidget *centralWidget = new QWidget(this);
    QVBoxLayout *layout = new QVBoxLayout(centralWidget);

    //创建按钮点击后响应基本信息
    QPushButton * infoBtn = new QPushButton("显示信息对话框", this);
    layout->addWidget(infoBtn);

    //创建警告信息
    QPushButton * warnBtn = new QPushButton("显示警告对话框", this);
    layout->addWidget(warnBtn);

    //创建危机信息
    QPushButton * criticalBtn = new QPushButton("显示危机对话框", this);
    layout->addWidget(criticalBtn);

    //创建提问信息
    QPushButton * questionBtn = new QPushButton("显示提问对话框", this);
    layout->addWidget(questionBtn);

    setCentralWidget(centralWidget);
    // 响应信息按钮
    connect(infoBtn, &QPushButton::clicked, this, [=]() {
           //弹出信息对话框
           QMessageBox::information(this, "信息", "这是一个信息对话框");
       });

    //响应警告按钮被点击
    connect(warnBtn, &QPushButton::clicked, this, [=]() {
            //弹出警告对话框
           QMessageBox::warning(this, "警告", "这是一个警告对话框");
       });

    //响应危机按钮被点击
    connect(criticalBtn, &QPushButton::clicked, this, [=]() {
            //弹出警告对话框
           QMessageBox::critical(this, "危机", "这是一个危机对话框");
       });

    //响应提问按钮被点击
    connect(questionBtn, &QPushButton::clicked, this, [=]() {
            //弹出警告对话框
           QMessageBox::question(this, "提问", "元神启动了吗?");
       });
}
```

运行程序后，发现这些消息框如果不点击确定，会阻塞MainWindow。

### 2 QInputDialog



`QInputDialog` 用于获取用户输入，可以是文本、整数或浮点数。



**常用方法：**



- `getText(QWidget *parent, const QString &title, const QString &label, ...)`
- `getInt(QWidget *parent, const QString &title, const QString &label, ...)`
- `getDouble(QWidget *parent, const QString &title, const QString &label, ...)`



**案例练习：**

我们需实现如下界面，点击输入姓名按钮后弹出输入对话框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270808907309.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270808907309.png)

我们在MainWindow里继续添加一个按钮，提示输入姓名

``` cpp
//创建一个输入对话框按钮
QPushButton *inputButton = new QPushButton("输入姓名", this);
layout->addWidget(inputButton);
```

然后编写槽函数，在槽函数中弹出一个输入对话框

``` cpp
//响应输入框按钮被点击
connect(inputButton, &QPushButton::clicked, this, [=]() {
    bool ok;
    //弹出输入对话框
    QString name = QInputDialog::getText(this,
                                         "输入", "请输入你的姓名：",
                                         QLineEdit::Normal, "", &ok);
    //返回ok为true表示创建成功，name不为空则弹出信息框
    if (ok && !name.isEmpty()) {
        QMessageBox::information(this, "姓名", QString("你好，%1！").arg(name));
    }
});
```



### 3 QDialog（自定义对话框）



`QDialog` 是一个基类，用于创建自定义的对话框，可以通过 Qt Designer 设计界面，并添加自定义功能。

界面如下

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270834254938.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270834254938.png)

点击ok后弹出提示框

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270837996809.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270837996809.png)

**创建自定义对话框的步骤：**

1. **设计界面**：
   - 使用 Qt Designer 创建一个新的对话框（.ui 文件）。
   - 添加需要的控件（如标签、输入框、按钮等）。
2. **创建对话框类**：
   - 使用 `QDialog` 作为基类。
   - 在类中包含生成的 UI 类。
   - 实现对话框的功能，如接受用户输入、验证输入、信号与槽等。





**开发思路：**



我们创建一个简单的设置对话框，用户可以输入用户名和密码。右键项目选择新建设计师界面类

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270812661959.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270812661959.png)

选择界面模板，创建一个Dialog带按钮组，按钮组在下方的界面

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270814811195.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270814811195.png)

点击下一步，创建的Dialog名字为SetDialog

拖动两个水平布局放入SetDialog中，再将SetDialog设置为垂直布局

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270819267965.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270819267965.png)

右侧布局管理器修改属性名

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270820882906.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270820882906.png)

我们在SetDialog的构造函数中设置密码输入框的模式为不可见

``` cpp
SetDialog::SetDialog(QWidget *parent) :
    QDialog(parent),
    ui(new Ui::SetDialog)
{
    ui->setupUi(this);
    //设置密码输入框模式
    ui->passwdEdit->setEchoMode(QLineEdit::Password);
}

```

我们为SetDialog增加两个方法，获取输入框里填写的名字和密码信息

``` cpp
QString SetDialog::getUserName() const
{
    return ui->nameEdit->text();
}

QString SetDialog::getPassword() const
{
    return ui->passwdEdit->text();
}
```

接下来我们在MainWindow中添加一个按钮，提示用户点击，进而显示这个设置对话框

``` cpp
QPushButton *openDialogButton = new QPushButton("打开设置对话框", this);
layout->addWidget(openDialogButton);
```

然后链接按钮点击信号，当按钮被点击后，显示对话框，对话框展示可以使用exec()方法，展示后对话框会阻塞用户其他操作，只能点击确定或者取消，

点击确定或者取消后，exec()会返回`QDialog::Accept`或者`QDialog::Rejected`. 

如果点击的是确定，则弹出用户输入的信息

``` cpp
//链接点击信号
connect(openDialogButton, &QPushButton::clicked, this, [=]() {
        //创建设置对话框
       SetDialog dialog(this);
       //exec表示模态方式启动
       if (dialog.exec() == QDialog::Accepted) {
           QString userName = dialog.getUserName();
           QString password = dialog.getPassword();
           QMessageBox::information(this, "设置",
                                    QString("用户名：%1\n密码：%2").arg(userName, password));
       }
   });
```

运行程序，点击打开设置对话框按钮，会触发槽函数，显示对话框，只有点击ok或者cancel之后，对话框才会退出，否则一直阻塞。



## 4. 对话框的实现与使用



### 1 创建和显示对话框



- **模态对话框**：使用 `exec()` 方法显示，调用该方法后，程序会等待对话框关闭后继续执行。

  ```cpp
  QDialog dialog;
  dialog.exec(); // 模态
  ```

- **非模态对话框**：使用 `show()` 方法显示，对话框显示后，程序继续执行，不会等待对话框关闭。

  ```cpp
  QDialog *dialog = new QDialog(this);
  dialog->show(); // 非模态
  ```

### 2  模态与非模态对话框的区别



- **模态对话框**：
  - 阻塞主窗口，用户必须先关闭对话框才能返回主窗口。
  - 常用于需要强制用户响应的情况，如确认操作、输入关键信息等。
- **非模态对话框**：
  - 不阻塞主窗口，用户可以在对话框和主窗口之间自由切换。
  - 常用于辅助信息显示、工具窗口等。

## 扩展

### 1 对话框事件过滤

在我们使用其他厂商的应用的时候，经常遇到这样一个场景

点击关闭窗口后会弹出提示框，提示是否确认关闭，如果点击取消，则不关闭对话框。

点击确认才关闭对话框。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270851264651.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270851264651.png)

怎么实现上述功能呢？

**开发思路**

1 先重写对话框的关闭事件处理函数`closeEvent`, 这个函数有个参数QCloseEvent，表示关闭事件

``` cpp
void closeEvent(QCloseEvent *) override;
```

对于关闭事件继承自QEvent，QEvent提供了两个方法

``` cpp
//表示接受
inline void accept() { m_accept = true; }
//表示忽略
inline void ignore() { m_accept = false; }
```

如果我们把这个事件忽略，他就不会被事件轮询处理。如果我们接受这个事件，那么他就会被事件轮询处理，所以给出关闭处理的完美答案

``` cpp
void closeEvent(QCloseEvent *event)  {
    QMessageBox::StandardButton resBtn = QMessageBox::question(this, "关闭确认",
        tr("你确定要关闭对话框吗？\n"),
        QMessageBox::No | QMessageBox::Yes,
        QMessageBox::Yes);
    if (resBtn != QMessageBox::Yes) {
        event->ignore();
    } else {
        event->accept();
    }
}
```

### 2 QFileDialog

QT为了方便我们操作，提供了很多快速创建不同类型对话框的类，以及静态方法，比如文件对话框

**常见用途：**



- 打开文件（如文本文件、图片等）
- 保存文件
- 选择目录

#### 常用方法



**静态函数：**



- `static QString getOpenFileName(QWidget *parent = nullptr, const QString &caption = QString(), const QString &dir = QString(), const QString &filter = QString(), QString *selectedFilter = nullptr, Options options = Options())`

  > 打开一个“打开文件”对话框，允许用户选择单个文件。

- `static QStringList getOpenFileNames(QWidget *parent = nullptr, const QString &caption = QString(), const QString &dir = QString(), const QString &filter = QString(), QString *selectedFilter = nullptr, Options options = Options())`

  > 打开一个“打开文件”对话框，允许用户选择多个文件。

- `static QString getSaveFileName(QWidget *parent = nullptr, const QString &caption = QString(), const QString &dir = QString(), const QString &filter = QString(), QString *selectedFilter = nullptr, Options options = Options())`

  > 打开一个“保存文件”对话框，允许用户选择或输入要保存的文件名。

- `static QString getExistingDirectory(QWidget *parent = nullptr, const QString &caption = QString(), const QString &dir = QString(), Options options = Options())`

  > 打开一个“选择目录”对话框，允许用户选择一个现有的目录。

#### 示例代码



**示例 1：打开单个文件**

``` cpp
#include <QApplication>
#include <QPushButton>
#include <QFileDialog>
#include <QMessageBox>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QPushButton button("打开文件");
    button.resize(200, 50);
    button.show();

    QObject::connect(&button, &QPushButton::clicked, [&]() {
        QString fileName = QFileDialog::getOpenFileName(
            &button,
            "选择一个文件",
            "/home",
            "所有文件 (*.*);;文本文件 (*.txt);;图片文件 (*.png *.jpg *.bmp)");

        if (!fileName.isEmpty()) {
            QMessageBox::information(&button, "文件选择", QString("你选择了：\n%1").arg(fileName));
        }
    });

    return a.exec();
}
```

**示例 2：保存文件**

``` cpp
#include <QApplication>
#include <QPushButton>
#include <QFileDialog>
#include <QMessageBox>
#include <QFile>
#include <QTextStream>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QPushButton button("保存文件");
    button.resize(200, 50);
    button.show();

    QObject::connect(&button, &QPushButton::clicked, [&]() {
        QString fileName = QFileDialog::getSaveFileName(
            &button,
            "保存文件",
            "/home/untitled.txt",
            "文本文件 (*.txt);;所有文件 (*.*)");

        if (!fileName.isEmpty()) {
            QFile file(fileName);
            if (file.open(QIODevice::WriteOnly | QIODevice::Text)) {
                QTextStream out(&file);
                out << "这是测试保存的文件内容。\n";
                file.close();
                QMessageBox::information(&button, "保存文件", "文件已成功保存。");
            } else {
                QMessageBox::warning(&button, "保存文件", "无法打开文件进行写入。");
            }
        }
    });

    return a.exec();
}
```

**示例 3：选择多个文件**

``` cpp
#include <QApplication>
#include <QPushButton>
#include <QFileDialog>
#include <QMessageBox>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QPushButton button("选择多个文件");
    button.resize(200, 50);
    button.show();

    QObject::connect(&button, &QPushButton::clicked, [&]() {
        QStringList fileNames = QFileDialog::getOpenFileNames(
            &button,
            "选择多个文件",
            "/home",
            "所有文件 (*.*);;图片文件 (*.png *.jpg *.bmp);;文本文件 (*.txt)");

        if (!fileNames.isEmpty()) {
            QString files = fileNames.join("\n");
            QMessageBox::information(&button, "文件选择", QString("你选择了：\n%1").arg(files));
        }
    });

    return a.exec();
}
```

**示例 4：选择目录**

``` cpp
#include <QApplication>
#include <QPushButton>
#include <QFileDialog>
#include <QMessageBox>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QPushButton button("选择目录");
    button.resize(200, 50);
    button.show();

    QObject::connect(&button, &QPushButton::clicked, [&]() {
        QString dir = QFileDialog::getExistingDirectory(
            &button,
            "选择一个目录",
            "/home",
            QFileDialog::ShowDirsOnly | QFileDialog::DontResolveSymlinks);

        if (!dir.isEmpty()) {
            QMessageBox::information(&button, "目录选择", QString("你选择了目录：\n%1").arg(dir));
        }
    });

    return a.exec();
}
```

####  实际案例



**案例：图像浏览器**



创建一个简单的图像浏览器，允许用户选择一个目录，显示该目录中的所有图片文件。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270901253913.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270901253913.png)

选择文件夹后，会将选择文件夹内的所有图片展开，点击左侧列表内容，会在右侧显示图片

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270902654105.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17270902654105.png)

**步骤概述：**



1. **创建主窗口**，包含：
   - 一个按钮“选择目录”
   - 一个 `QListWidget` 显示图片列表
   - 一个 `QLabel` 显示选中的图片
2. **实现功能**：
   - 点击按钮时，弹出 `QFileDialog` 选择目录
   - 扫描目录中的图片文件，并在 `QListWidget` 中显示
   - 选择列表中的图片时，显示在 `QLabel` 中

**示例代码：**

``` cpp
#include <QPushButton>
#include <QFileDialog>
#include <QListWidget>
#include <QLabel>
#include <QVBoxLayout>
#include <QHBoxLayout>
#include <QPixmap>
#include <QMessageBox>
#include <QDebug>

class ImageBrowser : public QDialog
{
    Q_OBJECT

public:
    ImageBrowser(QWidget *parent = nullptr) : QDialog(parent)
    {
        QPushButton *button = new QPushButton("选择目录", this);
        listWidget = new QListWidget(this);
        auto *right_wid = new QWidget(this);

        auto *right_layout = new QVBoxLayout(right_wid);

        imageLabel = new QLabel(this);
        imageLabel->setFixedSize(400,400);

        right_layout->addWidget(imageLabel);

        QHBoxLayout *mainLayout = new QHBoxLayout(this);
        QVBoxLayout *leftLayout = new QVBoxLayout();
        leftLayout->addWidget(button);
        leftLayout->addWidget(listWidget);
        mainLayout->addLayout(leftLayout);
        mainLayout->addWidget(right_wid);

        connect(button, &QPushButton::clicked, this, &ImageBrowser::selectDirectory);
        connect(listWidget, &QListWidget::itemClicked, this, &ImageBrowser::displayImage);
    }

    ~ImageBrowser(){
       // QMessageBox::information(nullptr,"提示信息","图片浏览器析构");
    }

private slots:
    void selectDirectory()
    {
        _dir = QFileDialog::getExistingDirectory(
            this,
            "选择图片目录",
            "/home",
            QFileDialog::ShowDirsOnly | QFileDialog::DontResolveSymlinks);

        if (!_dir.isEmpty()) {
            listWidget->clear();
            QStringList filters;
            filters << "*.png" << "*.jpg" << "*.jpeg" << "*.bmp" << "*.gif";
            QDir directory(_dir);
            QStringList images = directory.entryList(filters, QDir::Files);
            for (const QString &image : images) {
                listWidget->addItem(image);
            }
        }
    }

    void displayImage(QListWidgetItem *item)
    {
        QString imagePath = _dir + QDir::separator() + item->text();
        QPixmap pixmap(imagePath);

        if (!pixmap.isNull()) {
            //保持横纵比，且平滑缩放,返回一个新的缩放后的图片
            pixmap = pixmap.scaled(imageLabel->width(),imageLabel->height(),Qt::KeepAspectRatio,
                          Qt::SmoothTransformation);
            imageLabel->setPixmap(pixmap);
        }
    }

private:
    QListWidget *listWidget;
    QLabel *imageLabel;
    QString _dir;
};

```

mainwindow中添加按钮，并响应点击信号

``` cpp
    //图像浏览器
    //创建按钮提示用户打开对话框
    QPushButton *openPicBtn = new QPushButton("打开图片浏览器", this);
    layout->addWidget(openPicBtn);

    //链接点击信号
    connect(openPicBtn, &QPushButton::clicked, this, [=]() {
        //创建浏览器
        _browser = new ImageBrowser();
        _browser->setWindowTitle("简单图像浏览器");
        _browser->resize(600, 450);
        _browser->exec();
        _browser->deleteLater();

    });
```

运行程序，点击按钮后可实现上述效果。

### QProgressDialog 



**`QProgressDialog`** 是 Qt 提供的一个对话框类，用于显示长时间运行任务的进度。它可以显示任务的进度条、标签信息，以及一个“取消”按钮，允许用户中断任务。



**常见用途：**



- 下载或上传文件
- 数据处理或转换
- 文件复制或移动

#### 常用方法

- **构造函数：**

  ```cpp
  QProgressDialog(QWidget *parent = nullptr, Qt::WindowFlags flags = Qt::WindowFlags())
  ```

  或者指定详细信息：

  ```cpp
  QProgressDialog(const QString &labelText, const QString &cancelButtonText, int minimum, int maximum, QWidget *parent = nullptr, Qt::WindowFlags flags = Qt::WindowFlags())
  ```

- **设置文本：**

  ```cpp
  void setLabelText(const QString &label);
  void setCancelButtonText(const QString &text);
  ```

- **范围和值：**

  ```cpp
  void setRange(int minimum, int maximum);
  void setValue(int value);
  ```

  或者使用单一参数设置进度范围：

  ```cpp
  void setMaximum(int maximum);
  void setMinimum(int minimum);
  ```

- **其他设置：**

  ```cpp
  void setWindowModality(Qt::WindowModality modality);
  void setAutoClose(bool autoClose);
  void setAutoReset(bool autoReset);
  ```

- **信号：**

  - `void canceled()`: 当用户点击“取消”按钮时发出。

#### 示例代码



**示例 1：模拟一个耗时任务**

实现如下图效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727091758859.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1727091758859.png)

我们可以在main函数中新增按钮和点击的响应逻辑

``` cpp
//创建一个按钮演示进度框
//创建按钮提示用户打开对话框
QPushButton *progressBtn = new QPushButton("演示进度框", this);
layout->addWidget(progressBtn);

//链接点击信号
connect(progressBtn, &QPushButton::clicked, this, [=]() {
    //演示进度框
    QProgressDialog progress("正在执行任务...", "取消", 0, 100,this);
         progress.setWindowModality(Qt::WindowModal);
         progress.setMinimumDuration(0);
         progress.setValue(0);

         for (int i = 0; i <= 100; ++i) {
             // 模拟耗时任务
              // 暂停1秒
             QEventLoop loop;//定义一个新的事件循环
             QTimer::singleShot(1000, &loop, SLOT(quit()));//创建单次定时器，槽函数为事件循环的退出函数
             loop.exec();//事件循环开始执行，程序会卡在这里，直到定时时间到，本循环被退出


             progress.setValue(i);

             if (progress.wasCanceled()) {
                 QMessageBox::information(this, "取消", "任务已被取消。");
                 break;
             }
         }

         if (progress.value() == progress.maximum()) {
             QMessageBox::information(this, "完成", "任务已完成。");
         }

});
```



# 第七章 数据库

## 数据库**SQLite**  

**SQLite** 是一种轻量级的关系数据库管理系统，不需要单独的服务器进程，适合嵌入式应用。**Qt** 提供了丰富的 SQL 模块，使得在应用程序中集成数据库操作变得简单。本文将通过示例介绍如何使用 Qt 的 SQL 类与 SQLite 数据库进行交互，特别是如何使用 `QSqlTableModel`、`QSqlQueryModel` 以及 `QSqlQuery` 来实现数据的增删改查（CRUD）操作。

我们可以提前用navicat建立一个sqlite的数据库

![https://cdn.llfc.club/1727143284818.jpg](https://cdn.llfc.club/1727143284818.jpg)

创建sqlite3数据库，链接名字随便写，数据库名字我命名为example_sqlite

<img src="https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271434864463.png" alt="https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271434864463.png" style="zoom:50%;" />

记得点一下数据库文件右边的三个小点的按钮，将数据库另存一下

<img src="https://cdn.llfc.club/1727144188118.jpg" alt="https://cdn.llfc.club/1727144188118.jpg" style="zoom:50%;" />

点击确定后，会创建好sqlite数据库, 可以看到数据库下面有个main的库，库下面有表之类的结构。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271437093373.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271437093373.png)

建立好数据库后我们可以通过右键表，创建新的表结构

![https://cdn.llfc.club/1727144330278.jpg](https://cdn.llfc.club/1727144330278.jpg)

但是我们这里讲述的是如何通过QT代码创建表，所以不在navicat中手动创建表。

我们需要通过代码在数据库中创建一张employees表，并且插入数据

![https://cdn.llfc.club/1727152581392.jpg](https://cdn.llfc.club/1727152581392.jpg)

## 配置 Qt 项目



创建一个新的 Qt Widgets 应用程序项目，假设项目名称为 `QtSQLiteExample`。



**项目文件（.pro）配置：**



要使用 Qt 的 SQL 模块，需要在项目文件中添加相关模块：sql



```pro
QT += core gui sql

greaterThan(QT_MAJOR_VERSION, 4): QT += widgets

TARGET = QtSQLiteExample
TEMPLATE = app

SOURCES += main.cpp \
           mainwindow.cpp

HEADERS += mainwindow.h

FORMS += mainwindow.ui
```

## 建立与 SQLite 的连接



在使用任何 SQL 模型或查询之前，需要先建立与 SQLite 数据库的连接。



### 1. 包含必要的头文件



在需要使用 SQL 功能的文件中，包含 Qt SQL 模块的头文件：



```cpp
#include <QSqlDatabase>
#include <QSqlError>
#include <QSqlQuery>
#include <QDebug>
```



### 2. 初始化数据库连接



通常，可以在 `main.cpp` 或应用程序的初始化部分进行数据库连接设置。创建连接的接口如下

``` cpp

static QSqlDatabase addDatabase(const QString& type,
                             const QString& connectionName = QLatin1String(defaultConnection));
```

第一个参数type表示数据库的类型，第二个参数connectionName表示连接的名字，我们可以为连接指定名字，如果不设置就用默认连接。

以下示例在 `main.cpp` 中建立连接

``` cpp
// 添加 SQLite 数据库驱动
QSqlDatabase db = QSqlDatabase::addDatabase("QSQLITE");
// 设置数据库文件路径（相对路径或绝对路径）
db.setDatabaseName("example.db");
```

如果程序的执行路径下没有example.db，上述代码会在程序的运行路径创建一个"example.db"文件。

如果我们希望用户选择db文件可以用文件对话框，QFileDialog有一个static函数用来打开文件

``` cpp
   static QString getOpenFileName(QWidget *parent = nullptr,
                                   const QString &caption = QString(),
                                   const QString &dir = QString(),
                                   const QString &filter = QString(),
                                   QString *selectedFilter = nullptr,
                                   Options options = Options());
```

第一个参数是父窗口，第二个参数是标题，第三个参数是默认打开哪个文件夹，第四个参数是过滤器，用来指定显示哪些文件。

函数会返回所选择的文件的路径。

我们将建立连接代码稍作修改

``` cpp
// 利用文件对话框打开选择db文件
auto file_path = QFileDialog::getOpenFileName(nullptr,"选择sqlitedb文件","","*.db");
if(file_path.isEmpty()){
    QMessageBox::critical(nullptr,"文件错误信息","未选择文件!");
    return false;
}
```

我们设置默认选择db文件，如果不选择返回的就是空字符串，空字符串直接判断无效就返回。

接下来我们再调用之前写好的逻辑创建驱动并且设置数据库文件路径

``` cpp
// 添加 SQLite 数据库驱动
QSqlDatabase db = QSqlDatabase::addDatabase("QSQLITE");

// 设置数据库文件路径（相对路径或绝对路径）
db.setDatabaseName(file_path);
```

创建好db后我们打开数据库

``` cpp
// 打开数据库
if (!db.open()) {
    qDebug() << "无法打开数据库:" << db.lastError().text();
    return false;
}
```

接下来创建数据表，创建数据表的语句有多行，所以采用QT提供`R”()“`方式，表示原样字符串，我们可以把多行的字符串写到括号里

``` cpp
// 创建一个示例表，如果不存在的话
QSqlQuery query;
QString createTable = R"(
    CREATE TABLE IF NOT EXISTS employees (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        name TEXT NOT NULL,
        position TEXT NOT NULL,
        salary REAL
    )
)";
```

我们写了创建数据表的语句，接下来可以通过query去执行， query是QSqlQuery类型，包含exec方法传入要执行的sql语句，返回执行结果。

``` cpp
if (!query.exec(createTable)) {
    qDebug() << "创建表失败:" << query.lastError().text();
    return false;
}
```

同样的道理，我们可以基于employees表进行增删改查了, 我们可以查询一下employees表中的记录数，如果记录数为0，则向表中插入数据。我们能可以在navicat中新建一个查询，看看查到的结果

![https://cdn.llfc.club/1727149386800.jpg](https://cdn.llfc.club/1727149386800.jpg)

一般来说查询语句会返回多行，每一行有多列，因为count比较特殊，只返回1行1列表示员工数量。

所以我们可以取查询结果的第一列，下标为0获取记录数。

``` cpp
// 插入示例数据（如果表为空）
query.exec("SELECT COUNT(*) FROM employees");
if (query.next()) {
    //查询结果的第0列表示数量
    int count = query.value(0).toInt();
    if (count == 0) {
        QString insertData = "INSERT INTO employees (name, position, salary) VALUES "
                             "('Alice', 'Developer', 60000),"
                             "('Bob', 'Designer', 55000),"
                             "('Charlie', 'Manager', 75000)";
        if (!query.exec(insertData)) {
            qDebug() << "插入数据失败:" << query.lastError().text();
            return false;
        }
    }
}

```

所以我们给出完整代码

``` cpp
bool initializeDatabase()
{
    // 利用文件对话框打开选择db文件
    auto file_path = QFileDialog::getOpenFileName(nullptr,"选择sqlitedb文件","","*.db");
    if(file_path.isEmpty()){
        QMessageBox::critical(nullptr,"文件错误信息","未选择文件!");
        return false;
    }

    // 添加 SQLite 数据库驱动,使用默认连接
    QSqlDatabase db = QSqlDatabase::addDatabase("QSQLITE");

    // 设置数据库文件路径（相对路径或绝对路径）
    db.setDatabaseName(file_path);

    // 打开数据库
    if (!db.open()) {
        qDebug() << "无法打开数据库:" << db.lastError().text();
        return false;
    }

    // 创建一个示例表，如果不存在的话
    QSqlQuery query;
    QString createTable = R"(
        CREATE TABLE IF NOT EXISTS employees (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            name TEXT NOT NULL,
            position TEXT NOT NULL,
            salary REAL
        )
    )";

    if (!query.exec(createTable)) {
        qDebug() << "创建表失败:" << query.lastError().text();
        return false;
    }

    // 插入示例数据（如果表为空）
    query.exec("SELECT COUNT(*) FROM employees");
    if (query.next()) {
        //查询结果的第0列表示数量
        int count = query.value(0).toInt();
        if (count == 0) {
            QString insertData = "INSERT INTO employees (name, position, salary) VALUES "
                                 "('Alice', 'Developer', 60000),"
                                 "('Bob', 'Designer', 55000),"
                                 "('Charlie', 'Manager', 75000)";
            if (!query.exec(insertData)) {
                qDebug() << "插入数据失败:" << query.lastError().text();
                return false;
            }
        }
    }

    return true;
}

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    if(!initializeDatabase()){
        QMessageBox::information(nullptr,"数据库错误","创建数据库失败");
        return -1;
    }
    MainWindow w;
    w.show();

    return a.exec();
}

```

启动程序选择我们之前创建好的数据库，程序会在数据库中创建employees表，并且插入数据

![https://cdn.llfc.club/1727152581392.jpg](https://cdn.llfc.club/1727152581392.jpg)



## QSqlTableModel 



`QSqlTableModel` 是 Qt 提供的一个模型类，专门用于操作数据库中的单一表。它基于 SQL 数据库驱动，支持常见的数据库如 SQLite、MySQL、PostgreSQL 等。主要特点包括：



- **直接操作单一表**：能够方便地对单个数据库表进行增删改查操作。
- **与视图的无缝集成**：可以轻松地与 `QTableView`、`QListView` 等视图组件配合使用，实现数据的可视化展示和编辑。
- **支持多种编辑策略**：提供灵活的方式来管理数据的提交和取消。
- **自动同步数据**：在数据库和模型之间保持数据的一致性。

使用时要用`#include <QSqlTableModel>`

### 基本使用流程



使用 `QSqlTableModel` 的基本步骤如下：



1. **建立数据库连接**：确保与数据库的连接已建立，并且目标表存在。
2. **创建模型实例**：实例化 `QSqlTableModel` 对象。
3. **设置目标表**：指定要操作的数据库表。
4. **选择数据**：从数据库中检索数据以填充模型。
5. **与视图集成**：将模型与视图组件（如 `QTableView`）绑定，以显示和编辑数据。
6. **操作数据**：通过模型的接口插入、删除或修改数据。
7. **提交或还原更改**：根据编辑策略提交更改到数据库或撤销更改。



### 关键函数与属性



**1 构造函数**



```cpp
QSqlTableModel(QObject *parent = nullptr, QSqlDatabase db = QSqlDatabase())
```



- **parent**：父对象，通常设为 `nullptr`。
- **db**：使用的数据库连接，如果不传递参数，默认使用默认连接。



**2 主要函数**



- **setTable(const QString &tableName)**：设置模型所操作的数据库表。
- **select()**：从数据库中检索数据并填充模型。
- **setEditStrategy(QSqlTableModel::EditStrategy strategy)**：设置编辑策略。
- **insertRow(int row, const QModelIndex &parent = QModelIndex())**：在指定行插入新行。
- **removeRow(int row, const QModelIndex &parent = QModelIndex())**：删除指定行。
- **submitAll()**：提交所有更改到数据库（适用于手动提交策略）。
- **revertAll()**：撤销所有未提交的更改。
- **setFilter(const QString &filter)**：设置数据过滤条件。
- **setSort(int column, Qt::SortOrder order)**：设置排序条件。



**3 主要属性**



- **QSqlTableModel::editStrategy**：编辑策略，决定更改如何提交到数据库。



**4. 编辑策略**



`QSqlTableModel` 提供了三种编辑策略，用于控制对数据库的更改是如何提交的：



1. **QSqlTableModel::OnManualSubmit**（手动提交）：
   - 默认策略。
   - 所有更改（插入、删除、修改）都存储在模型中，直到调用 `submitAll()` 才提交到数据库。
   - 可以通过 `revertAll()` 撤销所有未提交的更改。
   - 适用于需要在一次性提交所有更改的场景，例如用户完成一系列编辑后再决定提交。
2. **QSqlTableModel::OnRowChange**（行更改时提交）：
   - 当用户完成对一行的编辑并移动到另一行时，自动提交该行的更改。
   - 更改直接提交到数据库。
   - 适用于希望实时保存每行更改的场景。
3. **QSqlTableModel::OnFieldChange**（字段更改时提交）：
   - 当用户更改任何字段的值时，立即提交该更改到数据库。
   - 适用于需要每次字段编辑后立即保存更改的场景。



**设置编辑策略示例：**

```cpp
model->setEditStrategy(QSqlTableModel::OnManualSubmit);
```

### 演示案例

我们通过QSqlTableModel和QTableView展示数据库的内容，并且支持在表格中修改提交保存到数据库

界面效果如下

![https://cdn.llfc.club/1727160032365.jpg](https://cdn.llfc.club/1727160032365.jpg)



我们在mainwindow中添加变量和函数声明

``` cpp
//数据模型
QSqlTableModel *model;
//设置模型
void setupModel();
//设置视图
void setupView();
```

实现setupModel

``` cpp
void MainWindow::setupModel()
{
    //创建模型
    model = new QSqlTableModel(this);
    //使用默认连接，对表employees操作
    model->setTable("employees");
    //设置提交策略为手动提交
    model->setEditStrategy(QSqlTableModel::OnManualSubmit);

    // 设置表头标签
    model->setHeaderData(0, Qt::Horizontal, "ID");
    model->setHeaderData(1, Qt::Horizontal, "姓名");
    model->setHeaderData(2, Qt::Horizontal, "职位");
    model->setHeaderData(3, Qt::Horizontal, "薪水");

    //将sql中的数据写入model中
    if (!model->select()) {
        QMessageBox::critical(this, "错误", "无法检索数据: " + model->lastError().text());
    }
}
```

在mainwindow构造函数中调用setupModel将数据加载到模型中

``` cpp
MainWindow::MainWindow(QWidget *parent)
    : QMainWindow(parent)
    , ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    setupModel();
}
```

我们回到mainwindow.ui中添加tableview和几个按钮，下面是整体布局

![https://cdn.llfc.club/1727158940741.jpg](https://cdn.llfc.club/1727158940741.jpg)

下面是布局属性图

![https://cdn.llfc.club/1727159174781.jpg](https://cdn.llfc.club/1727159174781.jpg)

模型加载成功后，将模型加载到tableview中。

``` cpp
void MainWindow::setupView()
{
    //设置模型
    ui->tableView->setModel(model);
    //设置选中模式为单个选中
    ui->tableView->setSelectionMode(QAbstractItemView::SingleSelection);
    //设置整行选中
    ui->tableView->setSelectionBehavior(QAbstractItemView::SelectRows);
    //设置编辑触发模式为双击或者选中时点击
    ui->tableView->setEditTriggers(QAbstractItemView::DoubleClicked
                                   | QAbstractItemView::SelectedClicked);
    //重置列宽自适应内容
    ui->tableView->resizeColumnsToContents();
}
```

在构造函数中加载视图

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    //加载模型
    setupModel();
    //加载视图
    setupView();
}
```

运行程序，选择db后弹出界面如下

![https://cdn.llfc.club/1727160032365.jpg](https://cdn.llfc.club/1727160032365.jpg)

接下来我们实现增加功能, 点击添加后默认添加一行数据

![https://cdn.llfc.club/1727160662669.jpg](https://cdn.llfc.club/1727160662669.jpg)

ui中右键添加按钮，选择槽函数跳转到实现，然后写具体添加逻辑

``` cpp
//添加按钮
void MainWindow::on_addBtn_clicked()
{
    //获取模型行数
    int row = model->rowCount();
    //在最后一行插入
    if (!model->insertRow(row)) {
        QMessageBox::warning(this, "错误", "无法插入行: "
                             + model->lastError().text());
        return;
    }

    // 自动设置默认值（可选）
    model->setData(model->index(row, 1), "新员工");
    model->setData(model->index(row, 2), "职位");
    model->setData(model->index(row, 3), 50000.0);

    //提交新插入的数据
    if (!model->submitAll()) {
        QMessageBox::warning(this, "错误", "无法提交新行: "
                             + model->lastError().text());
    }
}
```

查看数据库可以看到数据是写入成功了

接下来我们实现删除逻辑

``` cpp
void MainWindow::on_delBtn_clicked()
{
    //获取选中的行
    QModelIndexList selection = ui->tableView->selectionModel()->selectedRows();
    if (selection.isEmpty()) {
        QMessageBox::information(this, "提示", "请选择要删除的行。");
        return;
    }

    //行号列表
    QList<int> row_list;
    //遍历选中，将行号存起来
    foreach (QModelIndex index, selection) {
        row_list.append(index.row());
    }

    //排序从大到小
    std::sort(row_list.begin(),row_list.end(),std::greater<int>());

    //从行号大的删除
    for(auto & row : row_list){
        model->removeRow(row);
    }

    //提交修改
    if (!model->submitAll()) {
        QMessageBox::warning(this, "错误", "无法删除行: " + model->lastError().text());
    }
}
```

实现提交逻辑， 当我们修改表格数据后可以将修改提交到数据库

``` cpp
void MainWindow::on_subBtn_clicked()
{
    //提交模型修改到数据库
    if (!model->submitAll()) {
        QMessageBox::warning(this, "错误", "无法提交更改: " + model->lastError().text());
    } else {
        QMessageBox::information(this, "成功", "更改已提交。");
    }
}
```

我们新建一条数据，在数据库后台看到的还是默认值，修改后不提交，发现数据库也没变，点击提交后，再查看数据库就发现记录写入数据库了。

接下来实现撤销逻辑，当我们修改后点击还原，会将model还原为和数据库一致的状态

``` cpp
void MainWindow::on_revertBtn_clicked()
{
    //还原数据模型
    model->revertAll();
    QMessageBox::information(this, "已还原", "所有未提交的更改已还原。");
}
```

### 拓展

**控制列宽**

之前的表格列的宽度太小了，而且我们希望每一列文字居中对齐，并且我们希望薪水可以限制，

![https://cdn.llfc.club/1727167599718.jpg](https://cdn.llfc.club/1727167599718.jpg)

那么重新实现代理

``` cpp
#ifndef MYDELEGATE_H
#define MYDELEGATE_H
#include <QStyledItemDelegate>
#include <QPainter>
#include <QSpinBox>

class Mydelegate : public QStyledItemDelegate
{
public:
    Mydelegate(QObject *parent = nullptr):QStyledItemDelegate(parent){}
    void paint(QPainter *painter,
               const QStyleOptionViewItem &option, const QModelIndex &index)
    const override{
        //拷贝一份样式的副本，防止对引用做出污染
        QStyleOptionViewItem opt = option;
        //绑定opt和index
        initStyleOption(&opt, index);

        // 根据列设置不同的对齐方式
        opt.displayAlignment = Qt::AlignCenter;

        // 调用基类绘制（确保选中状态等被正确处理）
        QStyledItemDelegate::paint(painter, opt, index);
    }

    //创建编辑器
    QWidget *createEditor(QWidget *parent,
                          const QStyleOptionViewItem &option,
                          const QModelIndex &index) const override{
        //判断如果是第三列，则创建spinbox
        if(index.column() == 3){
            //创建spinbox
            QSpinBox *editor = new QSpinBox(parent);
            //设置最低薪水
            editor->setMinimum(3000);
            //设置最高薪水
            editor->setMaximum(2000000);
            //设置spinbox步长
            editor->setSingleStep(1000);
            return editor;
        }
        //其他列调用基类默认函数创建
        return QStyledItemDelegate::createEditor(parent,option,index);
    }

    //将模型的数据放入编辑器中
    void setEditorData(QWidget *editor, const QModelIndex &index) const override{
        //如果是第三列
        if(index.column() == 3){
            //获取数据
            int value = index.model()->data(index, Qt::EditRole).toInt();
            QSpinBox *spinBox = static_cast<QSpinBox*>(editor);
            //将数据设置到编辑器中
            spinBox->setValue(value);
            return;
        }
        //其他列调用基类设置数据
        return QStyledItemDelegate::setEditorData(editor,index);
    }
    //将编辑其中的数据放入模型中
    void setModelData(QWidget *editor,
                      QAbstractItemModel *model,
                      const QModelIndex &index) const override{
        if(index.column() == 3){
            //editor强制转换为QSpinBox
            QSpinBox *spinBox = static_cast<QSpinBox*>(editor);
            //检测输入是否合法，做数值限制
            spinBox->interpretText();
            //获取spinBox的值
            int value = spinBox->value();
            //将这个值写入模型
            model->setData(index, value, Qt::EditRole);
            return;
        }

        //其他类型调用默认的设置函数
        QStyledItemDelegate::setModelData(editor,model,index);
    }
    //更新编辑区域
    void updateEditorGeometry(QWidget *editor,
                              const QStyleOptionViewItem &option,
                              const QModelIndex &index) const override{
        //设置编辑区域
        editor->setGeometry(option.rect);
    }
};

#endif // MYDELEGATE_H

```

修改tableview表头的显示方式为拉伸，并且创建代理

``` cpp
void MainWindow::setupView()
{
    //设置模型
    ui->tableView->setModel(model);
    //设置选中模式为单个选中
    ui->tableView->setSelectionMode(QAbstractItemView::SingleSelection);
    //设置整行选中
    ui->tableView->setSelectionBehavior(QAbstractItemView::SelectRows);
    //设置编辑触发模式为双击或者选中时点击
    ui->tableView->setEditTriggers(QAbstractItemView::DoubleClicked
                                   | QAbstractItemView::SelectedClicked);
    //设置表头宽度拉伸
    ui->tableView->horizontalHeader()->setSectionResizeMode(QHeaderView::Stretch);
    //创建代理
    auto * delegate = new Mydelegate(this);
    //设置代理
    ui->tableView->setItemDelegate(delegate);
    //重置列宽自适应内容
    ui->tableView->resizeColumnsToContents();
}
```

再次运行能看到效果要求的效果

![https://cdn.llfc.club/1727167599718.jpg](https://cdn.llfc.club/1727167599718.jpg)

## QSqlQueryModel

`QSqlQueryModel` 是只读模型，适用于执行自定义查询并将结果显示在视图中。它不支持对数据进行直接编辑。

### 1. 包含头文件



```cpp
#include <QSqlQueryModel>
```



### 2. 基本用法

QSqlQueryModel有两个方法，都是用来执行sql语句的，只是参数不同。

``` cpp
//执行查询，传入QSqlQuery做的查询
void setQuery(const QSqlQuery &query);
//执行查询，可指定查询语句和数据库
void setQuery(const QString &query, const QSqlDatabase &db = QSqlDatabase());
```

### 3. 实现案例

以下示例展示如何使用 `QSqlQueryModel` 来执行自定义查询并显示结果。

我们需要显示如下的视图界面，右侧的为按薪水排序的只读视图。我们可以利用 `QSqlQueryModel`按照薪水排序存储，并且放入tableview中展示。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271739811261.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17271739811261.png)

我们在之前的案例ui中再增加一个视图，用来显示最高薪水，并且增加按钮，用来刷新最高薪水

![https://cdn.llfc.club/1727170154904.jpg](https://cdn.llfc.club/1727170154904.jpg)



属性结构图

![https://cdn.llfc.club/1727170319884.jpg](https://cdn.llfc.club/1727170319884.jpg)

在mainwindow的类中添加QSqueryModel*类型的成员变量,  以及响应刷新的槽函数

``` cpp
private slots:
    void on_refreshBtn_clicked();
private:
    //查询模型，用来做显示工资排序
    QSqlQueryModel* query_model;
```

然后在setupModel中添加query_model的初始化，并且编写sql语句将薪水按从大到小排序列出来

``` cpp
void MainWindow::setupModel()
{
    //创建模型
    model = new QSqlTableModel(this);
    //使用默认连接，对表employees操作
    model->setTable("employees");
    //设置提交策略为手动提交
    model->setEditStrategy(QSqlTableModel::OnManualSubmit);

    // 设置表头标签
    model->setHeaderData(0, Qt::Horizontal, "ID");
    model->setHeaderData(1, Qt::Horizontal, "姓名");
    model->setHeaderData(2, Qt::Horizontal, "职位");
    model->setHeaderData(3, Qt::Horizontal, "薪水");

    //将sql中的数据写入model中
    if (!model->select()) {
        QMessageBox::critical(this, "错误", "无法检索数据: " + model->lastError().text());
    }

    //创建查询模型
    query_model = new QSqlQueryModel(this);

    //编写查询语句
    QString query_str = "SELECT * FROM employees ORDER BY salary DESC";
    //创建查询
    query_model->setQuery(query_str);

    //判断查询是否出错
    if (query_model->lastError().isValid()) {
        QMessageBox::critical(this, "错误", "无法检索数据: " +
                              query_model->lastError().text());
    }

    //设置表头标签
    query_model->setHeaderData(0, Qt::Horizontal, "ID");
    query_model->setHeaderData(1, Qt::Horizontal, "姓名");
    query_model->setHeaderData(2, Qt::Horizontal, "职位");
    query_model->setHeaderData(3, Qt::Horizontal, "薪水");

}
```

设置视图的逻辑把QSqlQueryModel和视图绑定, 为了美观，我们将表头模式设置为拉伸

``` cpp
void MainWindow::setupView()
{
    //设置模型
    ui->tableView->setModel(model);
    //设置选中模式为单个选中
    ui->tableView->setSelectionMode(QAbstractItemView::SingleSelection);
    //设置整行选中
    ui->tableView->setSelectionBehavior(QAbstractItemView::SelectRows);
    //设置编辑触发模式为双击或者选中时点击
    ui->tableView->setEditTriggers(QAbstractItemView::DoubleClicked
                                   | QAbstractItemView::SelectedClicked);
    //设置表头宽度拉伸
    ui->tableView->horizontalHeader()->setSectionResizeMode(QHeaderView::Stretch);

    // 设置model
    ui->highView->setModel(query_model);
    // 设置单选模式
    ui->highView->setSelectionMode(QAbstractItemView::SingleSelection);
    // 设置一次选择一行
    ui->highView->setSelectionBehavior(QAbstractItemView::SelectRows);
    // 设置不触发编辑
    ui->highView->setEditTriggers(QAbstractItemView::NoEditTriggers);
    // 设置表头自动拉伸
    ui->highView->horizontalHeader()->setSectionResizeMode(QHeaderView::Stretch);

}
```

实现刷新按钮的槽函数逻辑，其实就是再次查询一下数据库，将结果写入query_model，因为query_model已经和视图绑定了，就会导致视图自动刷新

``` cpp
void MainWindow::on_refreshBtn_clicked()
{
    //编写查询语句
    QString query_str = "SELECT * FROM employees ORDER BY salary DESC";
    //创建查询
    query_model->setQuery(query_str);

    //判断查询是否出错
    if (query_model->lastError().isValid()) {
        QMessageBox::critical(this, "错误", "无法检索数据: " +
                              query_model->lastError().text());
    }
}
```

再次运行，就会弹出案例界面，并且我们在左侧编辑数据后提交，点击刷新，右侧视图就会出现按照薪水排序的效果

### 4.实现代理(拓展内容)

同学们看到表格内容不是按照居中对齐的，对于这种情况我们可以重新实现代理

``` cpp
#ifndef MYDELEGATE_H
#define MYDELEGATE_H
#include <QStyledItemDelegate>
#include <QPainter>
#include <QSpinBox>

class Mydelegate : public QStyledItemDelegate
{
public:
    Mydelegate(QObject *parent = nullptr):QStyledItemDelegate(parent){}
    void paint(QPainter *painter,
               const QStyleOptionViewItem &option, const QModelIndex &index)
    const override{
        //拷贝一份样式的副本，防止对引用做出污染
        QStyleOptionViewItem opt = option;
        //绑定opt和index
        initStyleOption(&opt, index);

        // 根据列设置不同的对齐方式
        opt.displayAlignment = Qt::AlignCenter;

        // 调用基类绘制（确保选中状态等被正确处理）
        QStyledItemDelegate::paint(painter, opt, index);
    }

    //创建编辑器
    QWidget *createEditor(QWidget *parent,
                          const QStyleOptionViewItem &option,
                          const QModelIndex &index) const override{
        //判断如果是第三列，则创建spinbox
        if(index.column() == 3){
            //创建spinbox
            QSpinBox *editor = new QSpinBox(parent);
            //设置最低薪水
            editor->setMinimum(3000);
            //设置最高薪水
            editor->setMaximum(2000000);
            //设置spinbox步长
            editor->setSingleStep(1000);
            return editor;
        }
        //其他列调用基类默认函数创建
        return QStyledItemDelegate::createEditor(parent,option,index);
    }

    //将模型的数据放入编辑器中
    void setEditorData(QWidget *editor, const QModelIndex &index) const override{
        //如果是第三列
        if(index.column() == 3){
            //获取数据
            int value = index.model()->data(index, Qt::EditRole).toInt();
            QSpinBox *spinBox = static_cast<QSpinBox*>(editor);
            //将数据设置到编辑器中
            spinBox->setValue(value);
            return;
        }
        //其他列调用基类设置数据
        return QStyledItemDelegate::setEditorData(editor,index);
    }
    //将编辑其中的数据放入模型中
    void setModelData(QWidget *editor,
                      QAbstractItemModel *model,
                      const QModelIndex &index) const override{
        if(index.column() == 3){
            //editor强制转换为QSpinBox
            QSpinBox *spinBox = static_cast<QSpinBox*>(editor);
            //检测输入是否合法，做数值限制
            spinBox->interpretText();
            //获取spinBox的值
            int value = spinBox->value();
            //将这个值写入模型
            model->setData(index, value, Qt::EditRole);
            return;
        }

        //其他类型调用默认的设置函数
        QStyledItemDelegate::setModelData(editor,model,index);
    }
    //更新编辑区域
    void updateEditorGeometry(QWidget *editor,
                              const QStyleOptionViewItem &option,
                              const QModelIndex &index) const override{
        //设置编辑区域
        editor->setGeometry(option.rect);
    }
};

#endif // MYDELEGATE_H

```

新增setupDelegate方法，然后在setupDelegate中设置代理，我们为两个视图设置代理

``` cpp
//设置代理
void MainWindow::setupDelegate()
{
    //创建模型代理
   auto* model_delegate =  new Mydelegate(this);
   //设置代理
   ui->tableView->setItemDelegate(model_delegate);

   //创建查询模型代理
   auto* query_model_delegate = new Mydelegate(this);
   //设置代理
   ui->highView->setItemDelegate(query_model_delegate);
}
```

在mainwindow的构造函数添加调用

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    //加载模型
    setupModel();
    //加载视图
    setupView();
    //设置代理
    setupDelegate();
}
```

## QSqlQuery

`QSqlQuery` 提供了更底层的 SQL 操作能力，适用于执行自定义的 SQL 语句，如复杂的查询、事务处理以及动态参数绑定。

### 1. 基本用法



以下示例展示如何使用 `QSqlQuery` 来执行查询和插入操作。

在执行sql语句前，我们还是要创建数据库类型，并且设置要操作的数据库

``` cpp
bool executeQueries()
{
    // 利用文件对话框打开选择db文件
    auto file_path = QFileDialog::getOpenFileName(nullptr,"选择sqlitedb文件","","*.db");
    if(file_path.isEmpty()){
        QMessageBox::critical(nullptr,"文件错误信息","未选择文件!");
        return false;
    }

    // 添加 SQLite 数据库驱动,使用默认连接
    QSqlDatabase db = QSqlDatabase::addDatabase("QSQLITE");

    // 设置数据库文件路径（相对路径或绝对路径）
    db.setDatabaseName(file_path);

    // 打开数据库
    if (!db.open()) {
        qDebug() << "无法打开数据库:" << db.lastError().text();
        return false;
    }
    //...todo 查询逻辑
}
```



如果执行的sql语句不带参数，我们可以直接执行sql语句

``` cpp
bool executeQueries(){
    //...省略数据库连接
        QSqlQuery query;

    // 执行查询
    QString selectQuery = "SELECT id, name, position, salary FROM employees";
    if (!query.exec(selectQuery)) {
        qDebug() << "查询失败:" << query.lastError().text();
        return false;
    }

    //如果有多条数据，通过循环依次打印
    while (query.next()) {
        //获取每条查询结果的第一个字段，从0开始
        int id = query.value(0).toInt();
        //获取每条查询结果的第二个字段，从1开始
        QString name = query.value(1).toString();
        //获取每条查询结果的第三个字段，从2开始
        QString position = query.value(2).toString();
        //获取每条查询结果的第四个字段，从3开始
        double salary = query.value(3).toDouble();
        //输出查询结果
        qDebug() << id << name << position << salary;
    }

}
```

###  2. 参数绑定



使用参数绑定可以防止 SQL 注入，并使代码更清晰。

如果执行的sql语句需要携带参数，我们可以通过`:占位名`的方式填入查询语句，并且在查询前将实际参数绑定给这个占位符即可

``` cpp
bool executeQueries(){
    //...省略数据库连接和打开
    // 插入数据，通过:name, :position, :salary占位
    QString insertQuery = "INSERT INTO employees (name, position, salary) VALUES (:name, :position, :salary)";
    if (!query.prepare(insertQuery)) {
        qDebug() << "准备插入语句失败:" << query.lastError().text();
        return false;
    }
    //绑定参数，通过绑定:name,:position,:salary为具体参数
    query.bindValue(":name", "David");
    query.bindValue(":position", "Tester");
    query.bindValue(":salary", 48000.0);

    //执行sql语句
    if (!query.exec()) {
        qDebug() << "插入失败:" << query.lastError().text();
        return false;
    } else {
        qDebug() << "成功插入一条记录。";
    }

    return true;
}
```

如果写着麻烦，可以用`?`占位

``` cpp
bool executeQueries(){
    //...省略数据库连接和打开
    // 插入数据，通过?占位
    QString insertQuery = "INSERT INTO employees (name, position, salary) VALUES (?,?,?)";
    if (!query.prepare(insertQuery)) {
        qDebug() << "准备插入语句失败:" << query.lastError().text();
        return false;
    }
    //绑定参数，将具体参数name1,position1,salary1按顺序填入？位置
    query.addBindValue("name1");
    query.addBindValue("position1");
    query.addBindValue("salary1");

    //执行sql语句
    if (!query.exec()) {
        qDebug() << "插入失败:" << query.lastError().text();
        return false;
    } else {
        qDebug() << "成功插入一条记录。";
    }

    return true;
}
```



### 3. 事务处理(拓展内容)



在执行多个相关的 SQL 语句时，可以使用事务确保操作的原子性。

开启事物需要提前设置数据库，我们将数据库的打开操作提出到一个函数里，将数据库设置为全局变量

``` cpp
QSqlDatabase db;
bool openDB(){
    // 利用文件对话框打开选择db文件
    auto file_path = QFileDialog::getOpenFileName(nullptr,"选择sqlitedb文件","","*.db");
    if(file_path.isEmpty()){
        QMessageBox::critical(nullptr,"文件错误信息","未选择文件!");
        return false;
    }

    // 添加 SQLite 数据库驱动,使用默认连接
     db = QSqlDatabase::addDatabase("QSQLITE");

    // 设置数据库文件路径（相对路径或绝对路径）
    db.setDatabaseName(file_path);

    // 打开数据库
    if (!db.open()) {
        qDebug() << "无法打开数据库:" << db.lastError().text();
        return false;
    }
    return true;
}
```

创建事务，事务中有多条操作，最后一起提交，如果某一条失败了则回滚

``` cpp
//执行事物
bool performTransaction()
{
	//创建事务
    if (!db.transaction()) {
        qDebug() << "事务开始失败:" << db.lastError().text();
        return false;
    }

    QSqlQuery query;
    //注意sqlite查询语句中有字符串的用单引号包裹
    if (!query.exec("UPDATE employees SET salary = salary + 5000 WHERE position = 'Developer'")) {
        qDebug() << "更新失败:" << query.lastError().text();
        //如果失败则回滚
        db.rollback();
        return false;
    }

    //如果不会拼接可以采用之前替换的方式
    auto query_str = "UPDATE employees SET salary = salary + 3000 WHERE position = ?";
    //准备执行
    if(!query.prepare(query_str)){
        qDebug() << "准备更新失败:" << query.lastError().text();
        //回滚
        db.rollback();
        return false;
    }

    //绑定数值
    query.addBindValue("Designer");

    //执行语句

    if (!query.exec()) {
        qDebug() << "更新失败:" << query.lastError().text();
        db.rollback();
        return false;
    }

    //执行完成后要提交结果，将多次执行的结果一次提交
    if (!db.commit()) {
        qDebug() << "事务提交失败:" << db.lastError().text();
        db.rollback();
        return false;
    }

    qDebug() << "事务成功提交。";
    return true;
}
```

### 4 获取自动生成的键（扩展内容）

通过`query.lastInsertId().toInt()`,我们可以获得插入返回的id

``` cpp
//获取插入后返回的id
bool insertAndRetrieveId(const QString &name, const QString &position, double salary, int &id)
{
    QSqlQuery query;
    query.prepare("INSERT INTO employees (name, position, salary) VALUES (:name, :position, :salary)");
    query.bindValue(":name", name);
    query.bindValue(":position", position);
    query.bindValue(":salary", salary);

    if (!query.exec()) {
        qDebug() << "插入失败:" << query.lastError().text();
        return false;
    }

    // 获取最后插入的 ID
    id = query.lastInsertId().toInt();
    return true;
}
```



# 第八章 绘图
## Qt 绘图系统概述



Qt 的绘图系统基于设备无关性（Device-Independent），允许开发者在不同的平台上创建一致的图形界面。主要组件包括：



- **QPainter**：用于在各种绘图设备（如窗口、图像、打印机等）上进行绘制操作。
- **绘图设备（QPaintDevice）**：如 `QWidget`、`QImage`、`QPixmap`、`QPrinter` 等，提供绘图的目标。
- **坐标系统**：Qt 使用二维坐标系，支持坐标变换（缩放、旋转、平移等）以简化复杂的绘图任务。
- **QGraphicsScene/QGraphicsView**：高级图形框架，用于管理和显示大量的二维图形项，并支持复杂的用户交互。



接下来，我们将深入探讨这些组件及其应用。

## QPainter 基础



`QPainter` 是 Qt 中进行绘图的核心类。它提供了一组丰富的方法来绘制各种形状、文本、图像等。



### 绘图设备



`QPainter` 可以在多种绘图设备上绘制，包括：



- **QWidget**：在窗口或自定义控件上绘制。
- **QImage**：在图像上绘制，适用于图像处理。
- **QPixmap**：在位图上绘制，常用于图形显示。
- **QPrinter**：用于打印任务。



在大多数情况下，开发者会在自定义 `QWidget` 的 `paintEvent` 中使用 `QPainter`。

### 基本用法



1. **创建和初始化 `QPainter`**:

   - 通常在 `QWidget` 的 `paintEvent` 方法中使用 `QPainter`。您需要创建一个 `QPainter` 对象，并将其与一个 `QPaintDevice`（如 `QWidget`、`QPixmap` 或 `QImage`）关联。

   ```cpp
   void MyWidget::paintEvent(QPaintEvent *event) {
       QPainter painter(this); // 'this' 是 QWidget 的指针
       // 进行绘制操作
   }
   ```

2. **绘制基本形状**:

   - `QPainter` 提供了多种方法来绘制基本形状，如直线、矩形、圆形等。

   ```cpp
   // 绘制直线
   painter.drawLine(10, 10, 100, 100);
   
   // 绘制矩形
   painter.drawRect(20, 20, 80, 60);
   
   // 绘制圆形
   painter.drawEllipse(50, 50, 80, 80);
   ```

3. **绘制文本**:

   - 使用 `drawText` 方法绘制文本，可以指定字体、颜色等。

   ```cpp
   painter.setFont(QFont("Arial", 16));
   painter.drawText(30, 30, "Hello, Qt!");
   ```

4. **设置颜色和画笔**:

   - 使用 `QPen` 设置线条的颜色和样式，使用 `QBrush` 设置填充颜色。

   ```cpp
   QPen pen(Qt::blue); // 创建蓝色画笔
   painter.setPen(pen);
   
   QBrush brush(Qt::green); // 创建绿色填充
   painter.setBrush(brush);
   ```

5. **绘制图像**:

   - 使用 `drawImage` 或 `drawPixmap` 方法绘制图像。

   ```cpp
   QImage image("path/to/image.png");
   painter.drawImage(10, 10, image);
   ```

6. **变换和旋转**:

   - 可以通过 `translate`、`rotate` 和 `scale` 方法进行坐标变换。

   ```cpp
   painter.translate(50, 50); // 移动原点
   painter.rotate(45); // 旋转
   painter.drawRect(0, 0, 100, 100); // 绘制相对于新原点的矩形
   ```

7. **保存和恢复状态**:

   - 可以使用 `save` 和 `restore` 方法保存和恢复 `QPainter` 的状态，以便在绘制时进行临时更改。

   ```cpp
   painter.save(); // 保存当前状态
   painter.setPen(Qt::red);
   painter.drawLine(0, 0, 100, 100);
   painter.restore(); // 恢复到保存的状态
   ```

8. **绘制路径**:

   - 使用 `QPainterPath` 创建复杂的形状。

   ```cpp
   QPainterPath path;
   path.moveTo(20, 20);
   path.lineTo(80, 20);
   path.lineTo(80, 80);
   path.closeSubpath();
   painter.drawPath(path);
   ```

### 基本绘图操作

例如我们想要在QWidget中绘制图形，需要自己定义一个Widget继承QWidget，然后重写paintEvent事件，在paintEvent中绘制图形.



以下是一个基本的例子，展示如何在自定义控件上绘制简单的图形和文本。



#### 示例：自定义 QWidget 绘制基本图形

创建项目的时候我们不选择创建主窗口，而是选择基于QWidget创建自定义的PainterWidget，我们自定义PainterWidget继承自QWidget，然后重写的paintEvent事件

``` cpp
class PainterWidget : public QWidget
{
    Q_OBJECT

public:
    explicit PainterWidget(QWidget *parent = nullptr);
    ~PainterWidget();
protected:
    //重写paintEvent事件
    void paintEvent(QPaintEvent* event) override;
private:
    Ui::PainterWidget *ui;
};
```

实现重回逻辑

``` cpp
//重写绘制事件
void PainterWidget::paintEvent(QPaintEvent *event)
{
    Q_UNUSED(event);

    QPainter painter(this);

    // 设置抗锯齿
    painter.setRenderHint(QPainter::Antialiasing, true);

    // 设置画笔和颜色
    QPen pen(Qt::black);
    pen.setWidth(2);
    painter.setPen(pen);

    // 绘制矩形
    painter.drawRect(50, 50, 100, 100);

    // 绘制椭圆
    painter.setBrush(QBrush(Qt::green));
    painter.drawEllipse(200, 50, 100, 100);

    // 绘制线条
    painter.setPen(QPen(Qt::red, 3));
    painter.drawLine(50, 200, 350, 200);

    // 绘制文本
    painter.setPen(QPen(Qt::blue));
    painter.setFont(QFont("Arial", 16));
    painter.drawText(150, 250, "Hello, Qt!");
}
```

**效果说明**：



- 矩形（黑色边框）
- 椭圆（绿色填充）
- 红色线条
- 蓝色文字



#### 运行效果



运行上述代码，将显示一个包含矩形、椭圆、线条和文本的窗口。



![https://cdn.llfc.club/1727233903334.jpg](https://cdn.llfc.club/1727233903334.jpg)

## 坐标系统与坐标变换



Qt 使用一个二维坐标系统来进行绘图，默认情况下，坐标的原点位于绘图设备的左上角，x 轴向右，y 轴向下。理解坐标变换对于创建复杂的图形和动画至关重要。

![https://cdn.llfc.club/1727236217869.jpg](https://cdn.llfc.club/1727236217869.jpg)

### 坐标系统概念



- **设备坐标系**：绘图设备的实际像素坐标。
- **逻辑坐标系**：开发者定义的坐标系统，便于绘图和布局。
- **变换**：通过缩放、旋转、平移等操作，将逻辑坐标映射到设备坐标。



### 坐标变换方法



`QPainter` 提供了一套变换方法，使得开发者可以轻松地进行坐标变换：



- **平移**：`translate(dx, dy)`，将绘图原点移动到 `(dx, dy)`。
- **旋转**：`rotate(angle)`，按顺时针方向旋转指定角度。
- **缩放**：`scale(sx, sy)`，沿 x 轴和 y 轴分别缩放。
- **倾斜**：`shear(sx, sy)`，沿 x 轴和 y 轴倾斜。



#### 示例：坐标变换

在widget中绘制图形

![https://cdn.llfc.club/1727248849258.jpg](https://cdn.llfc.club/1727248849258.jpg)



下面的例子展示了如何在绘图中应用平移、旋转和缩放变换。

``` cpp
//重新绘制widget显示的内容
void TransformWidget::paintEvent(QPaintEvent *event)
{
    Q_UNUSED(event);

    QPainter painter(this);
    //设置抗锯齿
    painter.setRenderHint(QPainter::Antialiasing, true);

    // 绘制原始矩形
    painter.setPen(QPen(Qt::black, 2));
    //画矩形
    painter.drawRect(50, 50, 100, 100);

    // 保存画笔状态，包括颜色，宽度等。
    painter.save();
    // 向右平移 200
    painter.translate(200, 0);
    painter.setPen(QPen(Qt::red, 2));
    painter.drawRect(50, 50, 100, 100);
    // 还原画笔状态
    painter.restore();

    // 保存画笔状态
    painter.save();
    // 移动原点到 (100, 200)
    painter.translate(100, 200);
    // 旋转 45 度
    painter.rotate(45);
    painter.setPen(QPen(Qt::green, 2));
    // 绘制中心在原点的矩形
    painter.drawRect(-50, -50, 100, 100);
    painter.restore();

    // 保存画笔状态
    painter.save();
    // 移动原点
    painter.translate(300, 200);
    // x 缩放 1.5，y 缩放 0.5
    painter.scale(1.5, 0.5);
    painter.setPen(QPen(Qt::blue, 2));
    painter.drawRect(-50, -50, 100, 100);
    painter.restore();
}

```

运行结果显示

![https://cdn.llfc.club/1727248849258.jpg](https://cdn.llfc.club/1727248849258.jpg)

## QImage 使用详解



`QImage` 是 Qt 框架中的一个类，用于处理和操作图像数据。它提供了多种功能，包括加载、保存、转换和绘制图像。以下是 `QImage` 的详细知识点和功能：



### 1. 基本概念



- **定义**: `QImage` 是一个用于处理图像的类，支持多种格式（如 BMP、PNG、JPEG 等），并提供了对图像数据的低级访问。
- **用途**: 常用于图形应用程序中，能够加载和保存图像文件，进行图像处理和绘制。



### 2. 创建 QImage



- **默认构造函数**: 创建一个空的 `QImage` 对象。

  ```cpp
  QImage image;
  ```

- **指定大小和格式**: 创建一个指定大小和格式的 `QImage`。

  ```cpp
  QImage image(width, height, QImage::Format_RGB32);
  ```

- **从文件加载**: 从文件加载图像。

  ```cpp
  QImage image("path/to/image.png");
  ```

- **从其他 QImage 复制**: 通过复制构造函数创建一个新的 QImage。

  ```cpp
  QImage copyImage(originalImage);
  ```



### 3. 图像格式



- 格式类型

  

  - `QImage::Format_RGB32`：每个像素占用 32 位（RGBA），适用于高质量图像。
  - `QImage::Format_ARGB32`：包含 Alpha 通道（透明度）。
  - `QImage::Format_Grayscale8`：灰度图像。
  - `QImage::Format_Mono`：单色图像。



### 4. 图像操作



- **图像大小**:

  - 获取图像的宽度和高度：

    ```cpp
    int width = image.width();
    int height = image.height();
    ```

- **缩放和裁剪**:

  - 缩放图像：

    ```cpp
    QImage scaledImage = image.scaled(newWidth, newHeight);
    ```

  - 裁剪图像：

    ```cpp
    QImage croppedImage = image.copy(x, y, width, height);
    ```

- **旋转和翻转**:

  - 旋转图像：

    ```cpp
    QImage rotatedImage = image.transformed(QMatrix().rotate(90));
    ```

  - 水平翻转：

    ```cpp
    image = image.mirrored(true, false);
    ```



### 5. 图像保存



- 保存到文件

  : 将图像保存到文件中，支持多种格式。

  ```cpp
  image.save("path/to/save/image.png", "PNG");
  ```



### 6. 图像转换



- 转换格式

  : 可以将图像转换为不同的格式。

  ```cpp
  QImage convertedImage = image.convertToFormat(QImage::Format_Grayscale8);
  ```



### 7. 绘制 QImage



- 在 QWidget 上绘制

  :

  - 使用 `QPainter` 在 `QWidget` 上绘制 `QImage`。

  ```cpp
  void MyWidget::paintEvent(QPaintEvent *event) {
      QPainter painter(this);
      painter.drawImage(0, 0, image);
  }
  ```



### 8. 示例: 加载修改保存图像

我们希望创建一个ImageWidget，加载原有的图片资源，并在原有的图片资源基础上绘制一个圆形的红色圈圈，并且通过widget显示出来

![https://cdn.llfc.club/1727253218458.jpg](https://cdn.llfc.club/1727253218458.jpg)

**实现过程**

我们创建一个QT项目，名称为ImageWidget，窗口名称为ImageWidget继承自QWidget.

项目建立好后，右键项目添加新建文件，选择Qt resource file，名称叫做res即可

无需创建前缀，前缀为/即可，添加文件选择文件夹中的th.jpg



在ImageWidget中添加QImage成员和声明paintEvent函数

``` cpp
protected:
    void paintEvent(QPaintEvent* event) override;
private:
    QImage image;
```

接下来在ImageWidget构造函数中加载图片资源

``` cpp
ImageWidget::ImageWidget(QWidget *parent) :
    QWidget(parent),
    ui(new Ui::ImageWidget)
{
    ui->setupUi(this);
    //加载图像
    if(!image.load(":/th.jpg")){
        // 确保资源路径正确，如果加载失败则创建一个像素32位的图像
        image = QImage(200,200,QImage::Format_ARGB32);
        //填充颜色
        image.fill(Qt::white);
    }

    //对图像处理...
}
```

我们可以使用QPainter在图片中心上绘制一个红色的圆圈

``` cpp
ImageWidget::ImageWidget(QWidget *parent) :
    QWidget(parent),
    ui(new Ui::ImageWidget)
{
    ui->setupUi(this);
    //加载图像
    if(!image.load(":/th.jpg")){
        // 确保资源路径正确，如果加载失败则创建一个像素32位的图像
        image = QImage(200,200,QImage::Format_ARGB32);
        //填充颜色
        image.fill(Qt::white);
    }

    // 对图像进行简单处理：在图像中心绘制一个红色圆圈
    QPainter painter(&image);
    //设置抗锯齿
    painter.setRenderHint(QPainter::Antialiasing, true);
    //设置画刷
    painter.setBrush(Qt::red);
    //画圆形，在图片中心且半径为50
    painter.drawEllipse(image.rect().center(), 50, 50);

    // 保存修改后的图像（可选）
    image.save("modified_image.png");
    // 设置固定的大小
    setFixedSize(image.size());
}
```

此时运行程序后，去运行的目录里会看到有一个新的图片modified_image.png，打开看图片上有一个红色的圆圈

![https://cdn.llfc.club/modified_image.png](https://cdn.llfc.club/modified_image.png)

我们接下来在ImageWidget上绘制这个图片，可以重写paintEvent函数，采用QPainter绘制

``` cpp
void ImageWidget::paintEvent(QPaintEvent *event)
{
    Q_UNUSED(event);

    QPainter painter(this);
    //绘制图像函数
    painter.drawImage(0, 0, image);
}
```

程序启动后，可以看到widget中绘制了我们添加的图片

![https://cdn.llfc.club/1727253218458.jpg](https://cdn.llfc.club/1727253218458.jpg)

### 9. 示例:  图像转灰度图像

我们实现在一个widget中展示一个图片的不同效果，一个原图，一个灰度图，如下图所示

![https://cdn.llfc.club/1727255340782.jpg](https://cdn.llfc.club/1727255340782.jpg)

**实现过程**

我们新建项目，主窗口创建GrayscaleWidget继承自QWidget

接下来我们在类的声明中声明两个QImage类型的变量, 并且重写paintEvent函数

``` cpp
class GrayscaleWidget : public QWidget
{
    Q_OBJECT

public:
    explicit GrayscaleWidget(QWidget *parent = nullptr);
    ~GrayscaleWidget();
protected:
    //重写绘制逻辑
    virtual void paintEvent(QPaintEvent *event) override;
private:
    Ui::GrayscaleWidget *ui;
    //存储彩色图像
    QImage colorImage;
    //存储灰度图
    QImage grayImage;

};
```

接下来我们在构造函数中加载我们的彩色图片资源，加载图片资源前也是需要将图片资源添加到项目里，通过创建qt 资源再添加

``` cpp
GrayscaleWidget::GrayscaleWidget(QWidget *parent) :
    QWidget(parent),
    ui(new Ui::GrayscaleWidget)
{
    ui->setupUi(this);
    // 加载彩色图像
    if (!colorImage.load(":/th.jpg")) {
        // 确保资源路径正确
        colorImage = QImage(200, 200, QImage::Format_ARGB32);
        colorImage.fill(Qt::white);
    }

    // 转换为灰度图像
    grayImage = colorImage.convertToFormat(QImage::Format_Grayscale8);
    //设置窗口大小
    setFixedSize(colorImage.width() * 2 + 10, colorImage.height());
}
```

重写绘制事件

``` cpp
void GrayscaleWidget::paintEvent(QPaintEvent *event)
{
    Q_UNUSED(event);
	//创建painter
    QPainter painter(this);

    // 绘制彩色图像
    painter.drawImage(0, 0, colorImage);

    // 在彩色图像右侧绘制灰度图像
    painter.drawImage(colorImage.width() + 10, 0, grayImage);
}
```

## QGraphicsScene 与 QGraphicsView 框架



`QGraphicsScene` 和 `QGraphicsView` 提供了一个高级的二维图形框架，适用于创建复杂的图形界面、动画以及交互式应用。它基于场景-视图模式，允许在场景中添加和管理大量的图形项，然后通过视图进行显示和交互。



### 基础概念



- **QGraphicsScene**：管理和组织所有的图形项（`QGraphicsItem`）。
- **QGraphicsView**：显示 `QGraphicsScene`，并提供视图变换（缩放、旋转等）和用户交互功能。
- **QGraphicsItem**：场景中的基本图形单元，可以是预定义的形状或自定义的图形。

打个比方

**QGraphicsItem**    相当于是舞台上的人

**QGraphicsScene**  相当于是舞台

 **QGraphicsView**   相当于我们看待舞台的视角

### QGraphicsScene



`QGraphicsScene` 是一个用于管理和存储图形项（`QGraphicsItem`）的场景。它负责处理图形项的添加、删除、更新和渲染。



#### 主要功能



- **管理图形项**: 可以添加、删除和管理多个图形项。
- **事件处理**: 处理与图形项相关的事件，如鼠标点击、键盘输入等。
- **坐标系统**: 提供一个坐标系统，可以在其中定位和操作图形项。



#### 常用方法



- `addItem(QGraphicsItem *item)`: 向场景中添加图形项。
- `removeItem(QGraphicsItem *item)`: 从场景中移除图形项。
- `clear()`: 清空场景中的所有图形项。
- `items()`: 返回场景中的所有图形项。



### QGraphicsView



`QGraphicsView` 是一个用于显示 `QGraphicsScene` 的窗口部件。它负责将场景的内容渲染到屏幕上，并提供用户交互。



#### 主要功能



- **可视化图形场景**: 显示 `QGraphicsScene` 中的内容。
- **视图变换**: 支持缩放、平移等视图变换操作。
- **事件转发**: 将用户输入事件（如鼠标和键盘事件）转发给场景中的图形项。



#### 常用方法



- `setScene(QGraphicsScene *scene)`: 设置要显示的场景。
- `fitInView()`: 调整视图以适应场景的内容。
- `scale()`: 缩放视图。
- `setRenderHint()`: 设置渲染提示，以提高绘制质量。

### 添加与管理图形项



`QGraphicsScene` 提供了多种添加图形项的方法，如 `addRect`、`addEllipse`、`addText` 等，也支持自定义图形项。



### **示例1：创建简单的图形场景**

实现下图所示，我们在场景中添加几个item，然后实现拖动和选中它们的效果。

![https://cdn.llfc.club/1727260777312.jpg](https://cdn.llfc.club/1727260777312.jpg)



我们声明一个类GraphicsSceneWidget，使其继承自QGraphicsView

``` cpp
#include <QGraphicsView>
#include <QWidget>

class GraphicsSceneWidget: public QGraphicsView
{
    Q_OBJECT
public:
    GraphicsSceneWidget(QWidget* parent = nullptr);
    ~GraphicsSceneWidget();
};
```

我们可以在GraphicsSceneWidget构造函数内部创建QGraphicsScene，向QGraphicsScene添加一些图形，最后将QGraphicsScene设置到视图里

``` cpp
GraphicsSceneWidget::GraphicsSceneWidget(QWidget *parent)
{
    //创建场景
    QGraphicsScene *scene = new QGraphicsScene(this);
    //设置场景区域
    //scene->setSceneRect(0,0,600,600);
    scene->setSceneRect(-1000, -1000, 2000, 2000);
    // 添加矩形
    QGraphicsRectItem *rect = scene->addRect(50, 50, 100, 100, QPen(Qt::black), QBrush(Qt::yellow));

    //设置可移动，可选中
    rect->setFlag(QGraphicsItem::ItemIsMovable ,true);
    rect->setFlag(QGraphicsItem::ItemIsSelectable ,true);
    // 添加椭圆
    QGraphicsEllipseItem *ellipse = scene->addEllipse(200, 50, 100, 100, QPen(Qt::blue), QBrush(Qt::green));

    //设置可移动，可选中
    ellipse->setFlag(QGraphicsItem::ItemIsMovable ,true);
    ellipse->setFlag(QGraphicsItem::ItemIsSelectable ,true);

    // 添加文本
    QGraphicsTextItem *text = scene->addText("Hello, QGraphicsScene!");
    text->setFont(QFont("Arial", 16));
    text->setDefaultTextColor(Qt::red);
    text->setPos(350, 50);

    //设置可移动，可选中
    text->setFlag(QGraphicsItem::ItemIsMovable ,true);
    text->setFlag(QGraphicsItem::ItemIsSelectable ,true);

    // 设置场景
    setScene(scene);

    // 设置视图属性
    setRenderHint(QPainter::Antialiasing);
    // 设置拖拽模式
    setDragMode(QGraphicsView::ScrollHandDrag);

}
```

关于拖拽模式

- **`NoDrag`**: 无拖动操作，适用于默认或无交互状态。
- **`ScrollHandDrag`**: 用于滚动视图，允许用户通过拖动来平移内容。
- **`RubberBandDrag`**: 用于选择多个对象或区域，用户通过拖动来绘制选择框。

接下来我们在主函数创建视图，并且展示

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建视图
    GraphicsSceneWidget w;
    //展示视图
    w.show();

    return a.exec();
}
```

### 示例2：调整视图

我们可以通过调整视图，实现不同方式查看场景，包括旋转，缩放，平移等

如下图所示

![https://cdn.llfc.club/1727311577543.jpg](https://cdn.llfc.club/1727311577543.jpg)]

我们在MainWindow.ui中为CentralWidget添加一个水平布局，然后将CentralWidget调整为垂直布局，那么水平布局就会填满整个CentralWidget。

左边放入QGraphicsView，右边放入一个widget，widget宽度限制120。

接下来在右侧widget中加入几个按钮并将右侧widget设置为垂直布局。

ui布局如下

![https://cdn.llfc.club/1727260600057.jpg](https://cdn.llfc.club/1727260600057.jpg)

属性结构如下：

![https://cdn.llfc.club/1727261929286.jpg](https://cdn.llfc.club/1727261929286.jpg)



我们之前自定义了一个视图是GraphicsSceneWidget，GraphicsSceneWidget继承自QGraphicsView.

那么我们可以将QGraphicsView提升为我们自定义的GraphicsSceneWidget类型

右键属性图中的graphicsView点击提升为

![https://cdn.llfc.club/1727262111408.jpg](https://cdn.llfc.club/1727262111408.jpg)

弹出窗口后，添加提升类的名称为GraphicsSceneWidget，勾选全局包含。

![https://cdn.llfc.club/1727262248003.jpg](https://cdn.llfc.club/1727262248003.jpg)

然后点击添加，再点击提升。可以看到属性图中graphicsView提升为GraphicsSceneWidget类型了。

![https://cdn.llfc.club/1727262450195.jpg](https://cdn.llfc.club/1727262450195.jpg)

接下来分别实现几个槽函数

``` cpp
//实现放大
void MainWindow::on_zoomIn_clicked()
{
    //视图放大1.5被
    ui->graphicsView->scale(1.5,1.5);
}

//实现缩小
void MainWindow::on_zoomOut_clicked()
{
    //视图缩小0.5
    ui->graphicsView->scale(0.5,0.5);
}

//顺时针旋转
void MainWindow::on_clockwise_clicked()
{
    //顺时针旋转15度
    ui->graphicsView->rotate(15);
}

//逆时针旋转
void MainWindow::on_counterClockwise_clicked()
{
    //逆时针旋转15度
    ui->graphicsView->rotate(-15);
}

//左平移
void MainWindow::on_moveleft_clicked()
{
    // 将可视区域的矩形范围的中心点的坐标转换到场景中，得出在场景中的坐标
    QPointF currentCenter = ui->graphicsView->mapToScene(
                ui->graphicsView->viewport()->rect().center());
    // 视口左移
    ui->graphicsView->centerOn(currentCenter.x() - 100, currentCenter.y());
}

//右平移
void MainWindow::on_moveRight_clicked()
{
    // 将可视区域的矩形范围的中心点的坐标转换到场景中，得出在场景中的坐标
    QPointF currentCenter = ui->graphicsView->mapToScene(
                ui->graphicsView->viewport()->rect().center());
    // 视口右移
    ui->graphicsView->centerOn(currentCenter.x() + 100, currentCenter.y());

}

```

这样我们点击对应的按钮，就可以实现视图的缩放，旋转，平移了。

### 示例3：自定义图形(拓展内容)

我们可以自定义图形，比如实现如下图的五角星的绘制

![https://cdn.llfc.club/1727317699888.jpg](https://cdn.llfc.club/1727317699888.jpg)

创建好项目CustomItem之后，我们添加一个类StarItem，继承自QGraphicsItem

``` cpp
class StarItem : public QGraphicsItem
{
public:
    StarItem(QGraphicsItem *parent = nullptr);

    // 重写边界函数
    QRectF boundingRect() const override;

    // 重写绘制函数
    void paint(QPainter *painter, const QStyleOptionGraphicsItem *option, QWidget *widget) override;

protected:
    // 重写鼠标事件处理
    void mousePressEvent(QGraphicsSceneMouseEvent *event) override;
    void mouseReleaseEvent(QGraphicsSceneMouseEvent *event) override;

private:
    QPainterPath starPath;
};
```

我们编程中采用的cos和sin等正余弦函数的参数和数学中不同，编程中正余弦参数为弧度，比如180°角度的弧度就是M_PI，就是我们常说的3.1415926.

使用M_PI要包含头文件`#include <qmath.h>`

那么360°对应的弧度就是M_PI * 360/180 = 2 *M_PI

30°的余弦函数计算公式为`cos(M_PI*30/180)`

 一个五角星有五个角，所以角与角之间应该是360/5=72°

72°对应的弧度就是M_PI*72/180,我们用deg存储

假设我们将五角星的原点设置为(0,0)，那么它上面的点，我们定义为第一个点也就是(0,-R)



![https://cdn.llfc.club/1727319511086.jpg](https://cdn.llfc.club/1727319511086.jpg)

接下来求顺时针的第二个点

![https://cdn.llfc.club/1727322331753.jpg](https://cdn.llfc.club/1727322331753.jpg)

已知第一个点和第二个点之间的角度为72°(两条红线夹角)，我们通过计算72°对应的弧度应为`deg = M_PI*72/180`

我们还知道第二个点到圆心的长度为R，那么可以计算出绿色线的长度为R*sin(deg)

黑色的线的长度为R*cos(deg)

所以第二个点的坐标为`(R*sin(deg), -R*cos(deg))`,因为坐标原点在五角星中心，所以第二个点的纵坐标为`-R*cos(deg)`

依次类推，可以推出第三个点的坐标为`(R*sin(2*deg),-R*cose(2*deg))`, 我们推出五个点的坐标

然后将要绘制的路线提前存起来，路线就是先将画笔移动到第一个点的位置

接下来从第一个点向第三个点连线，红色的线表示绘制的路径

![https://cdn.llfc.club/1727322777379.jpg](https://cdn.llfc.club/1727322777379.jpg)

从第三个点向第五个点连线

![https://cdn.llfc.club/1727322830878.jpg](https://cdn.llfc.club/1727322830878.jpg)

从第五个点向第二个点连线

![https://cdn.llfc.club/1727322905766.jpg](https://cdn.llfc.club/1727322905766.jpg)

从第二个点向第四个点连线

![https://cdn.llfc.club/1727322975552.jpg](https://cdn.llfc.club/1727322975552.jpg)

从第四个点回到原点

![https://cdn.llfc.club/1727323031187.jpg](https://cdn.llfc.club/1727323031187.jpg)

``` cpp
StarItem::StarItem(QGraphicsItem *parent)
    : QGraphicsItem(parent)
{

    double R = 100;
    double deg = M_PI*72/180;
    QList<QPoint> points = {
                           QPoint(0,-R),
                           QPoint(R*sin(deg),-R*cos(deg)),
                           QPoint(R*sin(2*deg),-R*cos(2*deg)),
                           QPoint(R*sin(3*deg),-R*cos(3*deg)),
                           QPoint(R*sin(4*deg),-R*cos(4*deg)),
                           };

    //移动到第一个点
    starPath.moveTo(points[0]);
    //从第一个点向第三个点连线
    starPath.lineTo(points[2]);
    //从第三个点向第五个点连线
    starPath.lineTo(points[4]);
    //从第五个点向第二个点连线
    starPath.lineTo(points[1]);
    //从第二个点向第四个点连线
    starPath.lineTo(points[3]);
    //从第四个点回到原点
    starPath.closeSubpath();


    // 设置图形项在场景的位置
    setPos(300, 200);

    // 启用图形项的选中状态
    setFlag(QGraphicsItem::ItemIsSelectable, true);
    setFlag(QGraphicsItem::ItemIsMovable, true);
}
```

接下来实现item所在的碰撞区域，每一个item都有一个矩形区域表示它的边界，我们重写这个函数

``` cpp
QRectF StarItem::boundingRect() const
{

    // 增加边界以避免裁剪
    return starPath.boundingRect().adjusted(-5, -5, 5, 5);
}
```

1. **starPath.boundingRect()**
   starPath 是一个 QPainterPath 对象，它表示一个绘图路径，可能包含多个形状、线条和曲线。

   boundingRect() 是 QPainterPath 的一个成员函数，它返回一个 QRectF 对象，表示该路径的边界矩形。这个矩形是一个最小的矩形，完全包围了路径中的所有形状。

2. **adjusted(left, top, right, bottom)**

   adjusted() 是 QRectF 的一个成员函数，用于调整矩形的边界。它接受四个参数，分别表示：
   left: 向左调整的距离
   top: 向上调整的距离
   right: 向右调整的距离
   bottom: 向下调整的距离

我们可以重写item的paintEvent函数，达到自定义绘制item的效果

``` cpp
//重回item样式
void StarItem::paint(QPainter *painter, const QStyleOptionGraphicsItem *option, QWidget *widget)
{
    Q_UNUSED(option);
    Q_UNUSED(widget);

    // 设置画笔和刷子
    //选中状态更改画笔颜色
    if (isSelected()) {
        painter->setPen(QPen(Qt::red, 2));
    } else {
        painter->setPen(QPen(Qt::cyan, 2));
    }
    painter->setBrush(QBrush(Qt::yellow));

    // 绘制星形路径
    painter->drawPath(starPath);
}
```

我们同样可以重写鼠标点击和释放的功能，这里没有做特殊处理，只是调用了基类的处理

``` cpp
void StarItem::mousePressEvent(QGraphicsSceneMouseEvent *event)
{
    // 点击时改变颜色
    Q_UNUSED(event);
    // 可以在这里添加更多自定义的交互逻辑
    QGraphicsItem::mousePressEvent(event);
}

void StarItem::mouseReleaseEvent(QGraphicsSceneMouseEvent *event)
{
    Q_UNUSED(event);
    QGraphicsItem::mouseReleaseEvent(event);
}
```

接下来在main函数中加载这个item

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建场景
    QGraphicsScene *scene = new QGraphicsScene();
    //设置场景大小
    scene->setSceneRect(0, 0, 600, 400);

    // 添加自定义星形图形项
    StarItem *star = new StarItem();
    scene->addItem(star);

    // 创建视图
    QGraphicsView *view = new QGraphicsView(scene);
    view->setRenderHint(QPainter::Antialiasing);
    view->setWindowTitle("自定义图形项示例");
    view->resize(800, 600);
    view->show();

    return a.exec();
}
```




# 第九章 QChart

### 简介



**QChart** 是 Qt 提供的一个用于创建各种类型图表（如折线图、柱状图、饼图等）的模块。它基于 Qt Charts 模块，旨在简化图表的创建和管理，使开发者能够快速构建出美观、功能丰富的图表界面。



###  QChart 组件概述



QChart 主要由以下几个核心组件组成：



- **QChart**: 图表的核心对象，管理所有的系列（Series）、轴（Axes）、图例（Legend）等。
- **QChartView**: 用于在界面上显示 QChart 的视图组件，继承自 QGraphicsView。
- **Series（系列）**: 数据的集合，不同类型的图表有不同的系列，如 QLineSeries（折线系列）、QBarSeries（柱状系列）、QPieSeries（饼图系列）等。
- **Axes（坐标轴）**: 图表的坐标轴，负责显示数据的范围和刻度，常用的有 QValueAxis（数值轴）、QCategoryAxis（类别轴）等。
- **Legend（图例）**: 显示系列的名称和对应颜色，帮助用户理解图表内容。





###  环境配置



在使用 QChart 之前，需要确保开发环境已经配置好 Qt Charts 模块。以下是配置步骤：



1. **安装 Qt Charts 模块**

   如果使用 Qt 5.7 及以上版本，Qt Charts 模块已包含在 Qt 框架中。否则需要单独安装。

2. **在项目文件中添加 Qt Charts**

   编辑项目的 `.pro` 文件，添加以下内容以启用 Qt Charts 模块：

   ```pro
   QT += charts
   ```

3. **包含 Qt Charts 头文件**

   在源码中包含 Qt Charts 的头文件：

   ```cpp
   #include <QtCharts/QChartView>
   #include <QtCharts/QLineSeries>
   #include <QtCharts/QBarSeries>
   #include <QtCharts/QPieSeries>
   ```

   或者使用模块方式：

   ```cpp
   #include <QtCharts>
   ```

4. **命名空间**

   Qt Charts 的所有类都位于 `QtCharts` 命名空间中，因此在使用时需要指定命名空间，或者使用 `QT_CHARTS_USE_NAMESPACE` 宏：

   ```cpp
   QT_CHARTS_USE_NAMESPACE
   ```

### 折线图

在 Qt Charts 中，绘制折线图主要涉及以下核心组件：



- **QLineSeries**：用于存储折线图的数据点。
- **QChart**：图表的核心对象，管理所有的系列、坐标轴和图例。
- **QChartView**：用于在界面上显示 `QChart` 的视图组件，类似于 `QGraphicsView`。
- **QValueAxis**：数值坐标轴，用于在图表中显示数值范围。

Qt Charts的方法不复杂，我们通过案例快速学习

####  示例场景

实现这样一个折线图

![https://cdn.llfc.club/1727332061313.jpg](https://cdn.llfc.club/1727332061313.jpg)



我们将创建一个显示某个产品销量随时间变化的折线图

创建一个项目LineSeries

在pro中添加charts

``` cpp
QT       += core gui charts
```

完成mainwindow的声明

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;
    // 用于在界面上显示 `QChart` 的视图组件，类似于 `QGraphicsView`
    QChartView *chartView;
    // 图表的核心对象，管理所有的系列、坐标轴和图例。
    QChart *chart;
    // 用于存储折线图的数据点
    QLineSeries *series;
    // 数值坐标轴，用于在图表中显示数值范围
    QValueAxis *axisX;
    // y轴坐标
    QValueAxis *axisY;

};
```

在构造函数中我们创建折线图，并且添加数据点，分别设置横纵坐标范围

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);

    // 创建折线系列
      series = new QLineSeries();
      //设置系列名字
      series->setName("产品销量");

      // 添加数据点 (X: 时间, Y: 销量)
      series->append(0, 1);
      series->append(1, 3);
      series->append(2, 2);
      series->append(3, 5);
      series->append(4, 4);

      // 创建图表
      chart = new QChart();
      //将数据添加到图表中
      chart->addSeries(series);
      //设置图表名字
      chart->setTitle("产品销量折线图示例");
      //设置图例可见
      chart->legend()->setVisible(true);
      //设置图例在底部
      chart->legend()->setAlignment(Qt::AlignBottom);

      // 创建坐标轴
      axisX = new QValueAxis();
      //设置x轴坐标标题
      axisX->setTitleText("时间");
      //设置x轴刻度文本显示的格式
      axisX->setLabelFormat("%d");
      //设置x轴的刻度数量
      axisX->setTickCount(5);
      //设置x轴的坐标范围
      axisX->setRange(0, 4);

      //设置纵坐标
      axisY = new QValueAxis();
      axisY->setTitleText("销量");
      axisY->setLabelFormat("%d");
      axisY->setTickCount(6);
      axisY->setRange(0, 5);

      // 将坐标轴添加到图表
      chart->addAxis(axisX, Qt::AlignBottom);
      chart->addAxis(axisY, Qt::AlignLeft);

      // 连接系列与坐标轴
      series->attachAxis(axisX);
      series->attachAxis(axisY);

      // 创建图表视图
      chartView = new QChartView(chart);
      chartView->setRenderHint(QPainter::Antialiasing);

      // 将图表视图添加到主窗口的布局中
      QVBoxLayout *layout = new QVBoxLayout();
      layout->addWidget(chartView);

      // 设置中央小部件的布局
      QWidget *widget = new QWidget();
      widget->setLayout(layout);
      setCentralWidget(widget);
}
```

### 折线图的定制和美化(拓展)

#### 设置图表主题

Qt Charts 提供了多种内置主题，可以快速改变图表的整体风格。

``` cpp
// 设置图表主题为黑暗主题
chart->setTheme(QChart::ChartThemeDark);

// 可选主题列表
// ChartThemeLight, ChartThemeBlueCerulean, ChartThemeBrownSand,
// ChartThemeBlueNcs, ChartThemeHighContrast, ChartThemeBlueIcy
```

#### 自定义坐标轴

**设置坐标轴标题**

```cpp
axisX->setTitleText("时间 (月)");
axisY->setTitleText("销量 (单位)");
```

**设置坐标轴范围和刻度**

```cpp
axisX->setRange(0, 12);  // 时间范围从0到12
axisX->setTickCount(13); // 每个月一个刻度

axisY->setRange(0, 100);
axisY->setTickCount(11); // 每10单位一个刻度
```



**设置折线颜色和宽度**

```cpp
QPen pen = series->pen();
pen.setColor(Qt::red);      // 设置折线颜色为红色
pen.setWidth(2);            // 设置折线宽度
series->setPen(pen);
```

**设置折线曲线平滑**

默认情况下，折线是直线连接的。要实现曲线平滑，可以使用 `QSplineSeries` 代替 `QLineSeries`。

```cpp
#include <QtCharts/QSplineSeries>

QSplineSeries *splineSeries = new QSplineSeries();
splineSeries->setName("平滑曲线");
splineSeries->append(0, 1);
splineSeries->append(1, 3);
splineSeries->append(2, 2);
// 添加更多数据点
chart->addSeries(splineSeries);
splineSeries->attachAxis(axisX);
splineSeries->attachAxis(axisY);
```

**平滑曲线示例**

大家可以自己制作数据，做出如下的图示

![https://cdn.llfc.club/1727336661412.jpg](https://cdn.llfc.club/1727336661412.jpg)

**答案**

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    //创建平滑曲线系列
    series = new QSplineSeries();
    //设置系列的名字
    series->setName("产品销量");
    //添加数据点
    series->append(1,3);
    series->append(2,2);
    series->append(3,5);
    series->append(4,4);
    series->append(5,3);
    series->append(6,2);
    series->append(7,5);
    series->append(8,4);
    series->append(9,9);
    series->append(10,8);
    series->append(11,7);
    series->append(12,4);


    //设置画笔颜色
    QPen pen = series->pen();
    pen.setColor(Qt::red);
    pen.setWidth(2);
    series->setPen(pen);

    //创建图表
    chart = new QChart();
    //将数据添加到图表中
    chart->addSeries(series);
    //设置图表名字
    chart->setTitle("产品销量平滑曲线图示例");
    //设置图例可见
    chart->legend()->setVisible(true);
    //设置图例在底部
    chart->legend()->setAlignment(Qt::AlignBottom);

    //创建坐标轴
    axisX = new QValueAxis();
    axisX->setTitleText("时间(月)");
    //表示1到12个月
    axisX->setRange(1,12);
    //刻度数量为12
    axisX->setTickCount(12);
    //设置刻度的文本
    axisX->setLabelFormat("%d");

    //创建坐标轴
    axisY = new QValueAxis();
    axisY->setTitleText("销量(万台)");
    //表示销量范围
    axisY->setRange(0,10);
    //刻度数量为10
    axisY->setTickCount(10);
    //设置刻度的文本
    axisY->setLabelFormat("%d");

    //将坐标轴添加到图表
    chart->addAxis(axisX, Qt::AlignBottom);
    chart->addAxis(axisY,Qt::AlignLeft);

    //连接系列和坐标系
    series->attachAxis(axisX);
    series->attachAxis(axisY);

    //创建图表
    chartView = new QChartView(chart);
    chartView->setRenderHint(QPainter::Antialiasing);

    //创建布局并且放入chartview
     auto* widget = new QWidget(this);
     auto * layout = new QVBoxLayout(widget);
     setCentralWidget(widget);
     layout->addWidget(chartView);

     this->resize(800,600);
}
```



**添加散点图**

可以通过设置 `QScatterSeries` 来添加数据点标记。

```cpp
#include <QtCharts/QScatterSeries>

// 创建散点系列
QScatterSeries *scatterSeries = new QScatterSeries();
scatterSeries->setName("数据点");
// 设置数据点为圆形
scatterSeries->setMarkerShape(QScatterSeries::MarkerShapeCircle);
scatterSeries->setMarkerSize(8.0);
scatterSeries->setColor(Qt::blue);

// 添加数据点
scatterSeries->append(0, 1);
scatterSeries->append(1, 3);
// 添加更多数据点
chart->addSeries(scatterSeries);
scatterSeries->attachAxis(axisX);
scatterSeries->attachAxis(axisY);
```



- **`QScatterSeries::MarkerShapeCircle`**：这是一个枚举值，表示数据点的形状为圆形。Qt Charts 提供了多种形状选项，例如：
  - `MarkerShapeCircle`：圆形
  - `MarkerShapeRectangle`：矩形
  - `MarkerShapeDiamond`：菱形
  - `MarkerShapeStar`：星形
  - `MarkerShapeCross`：十字形
  - `MarkerShapePixmap`：自定义图像

**示例**

在之前的曲线图基础上，添加几个散点，散点的数据和曲线的数据一样，要求实现如下效果

<img src="https://cdn.llfc.club/1727337550873.jpg" alt="https://cdn.llfc.club/1727337550873.jpg" style="zoom: 80%;" />

**实现细节**

在源代码的基础上，也就是MainWindow的构造函数里继续添加散点图的创建，并加入到chart中。

**注意**

不要忘了将散点图系列绑定到坐标

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow){   
     //... 前面省略
	//创建散点系列
     QScatterSeries* scatterSeries = new QScatterSeries();
     scatterSeries->setName("数据散点");
     scatterSeries->setMarkerShape(QScatterSeries::MarkerShapeCircle);

     //添加数据点
     scatterSeries->append(1,3);
     scatterSeries->append(2,2);
     scatterSeries->append(3,5);
     scatterSeries->append(4,4);
     scatterSeries->append(5,3);
     scatterSeries->append(6,2);
     scatterSeries->append(7,5);
     scatterSeries->append(8,4);
     scatterSeries->append(9,9);
     scatterSeries->append(10,8);
     scatterSeries->append(11,7);
     scatterSeries->append(12,4);

     //加入散点
     chart->addSeries(scatterSeries);
     //绑定到坐标
     scatterSeries->attachAxis(axisX);
     scatterSeries->attachAxis(axisY);
 }
```





#### 显示悬停提示



在用户悬停在数据点上时显示详细信息，可以使用 `QToolTip` 或自定义工具提示。

```cpp
// 在主窗口类中添加槽函数
private slots:
    void handlePointHovered(const QPointF &point, bool state);

// 在构造函数中连接信号
connect(series, &QSplineSeries::hovered, this, &MainWindow::handlePointHovered);

// 实现槽函数
#include <QToolTip>

void MainWindow::handlePointHovered(const QPointF &point, bool state)
{
    if (state) {
        QString tooltipText = QString("时间: %1 月\n销量: %2 单位").arg(point.x()).arg(point.y());
        QToolTip::showText(QCursor::pos(), tooltipText, chartView);
    } else {
        QToolTip::hideText();
    }
}
```

**hovered信号参数解释**



1. **`const QPointF &point`**:
   - **类型**: `QPointF` 是一个表示二维点的类，包含两个浮点数（`x` 和 `y`）坐标。
   - **意义**: 这个参数表示鼠标悬停的点的坐标。在散点图中，这个点通常对应于某个数据点的值。`point.x()` 表示该点在 X 轴上的值，`point.y()` 表示该点在 Y 轴上的值。
2. **`bool state`**:
   - **类型**: 布尔值（`bool`）。
   - **意义**: 这个参数表示鼠标是否悬停在某个数据点上。如果 `state` 为 `true`，这意味着鼠标正在悬停在数据点上；如果为 `false`，则表示鼠标离开了该数据点。这个参数用于控制工具提示的显示和隐藏。



**确保启用系列的悬停事件：**

```cpp
series->setPointsVisible(true); // 启用数据点可见
```

**演示案例**

基于之前的平滑曲线和散点图，我们支持鼠标悬浮显示数据提示的效果

![https://cdn.llfc.club/1727339868095.jpg](https://cdn.llfc.club/1727339868095.jpg)



**实现思路**

在mainwindow的声明里添加

``` cpp
public slots:
    //捕获鼠标悬浮事件
    void handlePointHovered(const QPointF &point, bool state);
```



在构造函数里添加

``` cpp
 //开启数据点可视
 series->setPointsVisible(true);
//连接信号和槽,捕获悬浮信号
 connect(series, &QSplineSeries::hovered, this,
         &MainWindow::handlePointHovered);

 scatterSeries->setPointsVisible(true);
 connect(scatterSeries, &QScatterSeries::hovered, this,
         &MainWindow::handlePointHovered);
```

实现槽函数

``` cpp
void MainWindow::handlePointHovered(const QPointF &point, bool state)
{
    if (state) {
        QString tooltipText = QString("时间: %1 月\n销量: %2 单位").arg(point.x()).arg(point.y());
        QToolTip::showText(QCursor::pos(), tooltipText, chartView);
    } else {
        QToolTip::hideText();
    }
}
```



#### 设定背景和网格线



**设置图表背景颜色**

```cpp
chart->setBackgroundBrush(QBrush(Qt::white)); // 设置背景为白色
```

**设置网格线**

```cpp
axisX->setGridLineVisible(true);
axisY->setGridLineVisible(true);
```

#### 启用缩放和平移



`QChartView` 提供了内置的缩放和平移功能，可以通过设置橡皮筋（RubberBand）来启用。



```cpp
// 启用矩形缩放
chartView->setRubberBand(QChartView::RectangleRubberBand);

// 或者启用水平/垂直缩放
// chartView->setRubberBand(QChartView::HorizontalRubberBand);
// chartView->setRubberBand(QChartView::VerticalRubberBand);
```



用户可以通过鼠标拖拽来选择缩放区域，或通过鼠标滚轮进行缩放。

### 动态更新折线图数据

我们可以做一个动态更新正弦波的案例，将通过以下步骤实现动态正弦曲线的绘制：



1. 创建 `QLineSeries` 并初始化正弦曲线数据。
2. 将系列添加到 `QChart`。
3. 使用 `QTimer` 定时更新数据点，实现动态效果。
4. 设置坐标轴、图表样式等。

要求达到如下图效果

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17273444507606.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17273444507606.png)

**开发思路**

创建项目sinline, 在mainwindow中声明各参数

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;
    //Qt Charts成员
    QChartView * chartView;
    QChart * chart;
    QSplineSeries * series;
    QValueAxis* axisX;
    QValueAxis* axisY;
    QTimer* timer;

    //当前的角度
    double currentAngle;
};
```

在构造函数创建图表

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    //创建视图，坐标轴等
    chartView = new QChartView(this);
    chart = new QChart();
    series = new QSplineSeries();
    axisX = new QValueAxis();
    axisY = new QValueAxis();
    //创建定时器
    timer = new QTimer(this);

    //初始弧度为0
    currentAngle = 0.0;
    ui->setupUi(this);

    //为保证数据足够充分，才能显示出更准确的曲线
    //所以将一个周期定位2*M_PI，将其分成100份作为x坐标
    auto pointsCount = 100;
    //将弧度划分100分
    auto step = 2*M_PI/pointsCount;
    //计算每个点对应的弧度
    for(int i = 0; i < pointsCount; i++){
        double angle = i * step;
        double sineValue = qSin(angle);
        series->append(angle,sineValue);
    }

    //设置series名字
    series->setName("正弦波");
 
    //将系列添加到图表
    chart->addSeries(series);
    //设置图表标题
    chart->setTitle("动态正弦曲线示例");
    //显示图例
    chart->legend()->setVisible(true);

    //设置坐标轴
    axisX->setTitleText("角度(弧度)");
    //设置范围
    axisX->setRange(0,2*M_PI);
    //设置坐标轴文本样式
    axisX->setLabelFormat("%.2f");
    //设置刻度数
    axisX->setTickCount(10);


    axisY->setTitleText("正弦值");
    axisY->setRange(-1.5, 1.5);
    axisY->setLabelFormat("%.1f");
    axisY->setTickCount(5);

    // 将坐标轴添加到图表
    chart->addAxis(axisX, Qt::AlignBottom);
    chart->addAxis(axisY, Qt::AlignLeft);

    // 连接系列与坐标轴
    series->attachAxis(axisX);
    series->attachAxis(axisY);

    // 设置图表主题
    chart->setTheme(QChart::ChartThemeDark);

    // 创建图表视图
    chartView->setChart(chart);
    chartView->setRenderHint(QPainter::Antialiasing);

    // 设置布局
    QVBoxLayout *layout = new QVBoxLayout();
    layout->addWidget(chartView);

    QWidget *widget = new QWidget();
    widget->setLayout(layout);
    setCentralWidget(widget);

    resize(1000,600);
}
```

此时运行程序能看到静态的正弦曲线了

接下来我们在构造函数中启动定时器，每隔50ms触发依次回调函数, 更新坐标轴数据信息

``` cpp
MainWindow::MainWindow():
    QMainWindow(parent),
    ui(new Ui::MainWindow){
    //...省略之前的图表操作
    
    // 配置定时器
    connect(timer, &QTimer::timeout, this, &MainWindow::updateSineWave);
    // 每50毫秒更新一次
    timer->start(50);
}

//实现定时器函数
void MainWindow::updateSineWave()
{
    // 增加当前角度
    currentAngle += 0.05; // 以步长0.05弧度递增

    // 移动角度范围为 [currentAngle, currentAngle + 2π]
    // 清空旧数据
    series->clear();

    // 生成新的正弦曲线数据
    const int pointsCount = 100;
    const double step = (2 * M_PI) / pointsCount;
    for (int i = 0; i <= pointsCount; ++i) {
        double angle = currentAngle + i * step;
        double sineValue = qSin(angle);
        series->append(angle, sineValue);
    }

    // 更新X轴范围
    axisX->setRange(currentAngle, currentAngle + 2 * M_PI);
}
```

再次运行，就可以看到正弦曲线动起来了。

### 饼状图

**核心组件**

在 Qt Charts 中，绘制饼状图主要涉及以下核心组件：



- **QPieSeries**：用于存储饼状图的数据，每个扇区（Slice）代表一个数据项。
- **QChart**：图表的核心对象，管理所有的系列、图例和标题。
- **QChartView**：用于在界面上显示 `QChart` 的视图组件，类似于 `QGraphicsView`。
- **QPieSlice**：表示饼状图中的单个扇区，包含数据值和标签等信息。

废话不多说，直接实战

**实现案例**

实现案例如下图

![https://cdn.llfc.club/1727347665975.jpg](https://cdn.llfc.club/1727347665975.jpg)

**实现思路**

新建项目Pieseries，并且添加必要的成员,  注意包含`QtCharts`以及在pro中添加charts库

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;

    // Qt Charts 成员
    QChartView *chartView;
    QChart *chart;
    QPieSeries *series;
};
```

构造函数里实现饼状图

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),
    chartView(new QChartView(this))
  , chart(new QChart())
  , series(new QPieSeries())
{
    ui->setupUi(this);

    // 初始化饼状图数据
    series->append("苹果", 30);
    series->append("香蕉", 20);
    series->append("梨子", 25);
    series->append("橘子", 15);
    series->append("葡萄", 10);

    // 可选择突出某个扇区
    QPieSlice *slice = series->slices().at(0);
    // 突出显示
    slice->setExploded(true);
    // label可见
    slice->setLabelVisible(true);
    slice->setBrush(Qt::red); // 设置扇区颜色

    // 添加系列到图表
    chart->addSeries(series);
    chart->setTitle("水果销售比例");
    // 图例可见
    chart->legend()->setVisible(true);
    // 右侧对齐
    chart->legend()->setAlignment(Qt::AlignRight);

    // 设置饼状图为圆形
    chart->setAnimationOptions(QChart::AllAnimations);

    // 设置图表到视图
    chartView->setChart(chart);
    // 抗锯齿
    chartView->setRenderHint(QPainter::Antialiasing);

    // 设置布局
    QVBoxLayout *layout = new QVBoxLayout();
    layout->addWidget(chartView);

    QWidget *widget = new QWidget();
    widget->setLayout(layout);
    setCentralWidget(widget);
    this->resize(800,600);
}
```



### 饼状图的定制与美化(拓展)



为了使饼状图更具美观性和可读性，可以进行多种定制和美化操作，包括：



- 设置扇区颜色和突出显示
- 添加标签和百分比
- 设定图表主题
- 设置动画效果
- 修改图例位置和样式



#### 设置扇区颜色



可以为不同的扇区设置不同的颜色，以增强视觉效果。



```cpp
QPieSlice *slice1 = series->slices().at(0);
slice1->setBrush(Qt::red);

QPieSlice *slice2 = series->slices().at(1);
slice2->setBrush(Qt::green);

QPieSlice *slice3 = series->slices().at(2);
slice3->setBrush(Qt::blue);

QPieSlice *slice4 = series->slices().at(3);
slice4->setBrush(Qt::yellow);

QPieSlice *slice5 = series->slices().at(4);
slice5->setBrush(Qt::cyan);
```



####  添加标签和百分比



可以为扇区添加标签，并显示百分比信息。

```cpp
foreach (QPieSlice *slice, series->slices()) {
    slice->setLabelVisible(true);
    // 显示标签和百分比
    slice->setLabel(QString("%1: %2%").arg(slice->label()).arg(slice->percentage() * 100, 0, 'f', 1));
}
```

上述代码为各个扇区设置标签，`%2%`表示

`%2`第二个参数，后面再跟一个`%`表示第二个参数的格式是小数点保留一位，小数位为0且为浮点数

![https://cdn.llfc.club/1727348611289.jpg](https://cdn.llfc.club/1727348611289.jpg)



####  设定图表主题



Qt Charts 提供了多种内置主题，可以快速改变图表的整体风格。



```cpp
chart->setTheme(QChart::ChartThemeBlueCerulean);
// 可选主题列表
// ChartThemeLight, ChartThemeBlueCerulean, ChartThemeDark, ChartThemeBrownSand,
// ChartThemeBlueNcs, ChartThemeHighContrast, ChartThemeBlueIcy
```



#### 设置动画效果



通过设置动画选项，使图表在数据变化时具有过渡效果。



```cpp
chart->setAnimationOptions(QChart::SeriesAnimations);
```



#### 修改图例位置和样式



可以调整图例的位置和样式，使其更符合界面设计需求。



```cpp
chart->legend()->setVisible(true);
chart->legend()->setAlignment(Qt::AlignRight);
chart->legend()->setFont(QFont("Arial", 10));
```



###  动态更新饼状图数据



在实际应用中，饼状图的数据可能会随着时间或事件发生变化。以下介绍如何通过定时器动态更新饼状图的数据。

**演示示例**

定时模拟随机品类的水果数量增加，并作动态显示

**实现细节**

类的声明中添加定时器以及map管理数据

``` cpp
    // 定时器用于动态更新
    QTimer *timer;

    // 模拟数据
    QMap<QString, QPieSlice*> _name_map;
```

构造函数中修改数据初始化，先加入map，再初始化扇区

``` cpp
        // 初始化饼状图数据
    series->append("苹果", 30);
    series->append("香蕉", 20);
    series->append("梨子", 25);
    series->append("橘子", 15);
    series->append("葡萄", 10);

    //设置标签
    auto index = 0;
    foreach (QPieSlice *slice, series->slices()) {

        //将索引和数据关联起来
        _name_map.insert(slice->label(),slice);

        slice->setLabelVisible(true);
        // 显示标签和百分比
        slice->setLabel(QString("%1: %2%").arg(slice->label())
                        .arg(slice->percentage() * 100, 0, 'f', 1));
        index++;
    }
```

构造函数添加定时器初始化，并且链接信号和槽，然后启动定时器，每隔两秒回调一次

``` cpp
    //创建定时器
    timer = new QTimer(this);
    // 连接定时器信号
    connect(timer, &QTimer::timeout, this, &MainWindow::updateChart);
    // 每2秒更新一次
    timer->start(2000);
```

槽函数的实现

``` cpp
void MainWindow::updateChart()
{
    // 模拟数据变化：随机增加或减少某个水果的销量
    QStringList keys = _name_map.keys();
    //随机选择一个key
    QString key = keys.at(QRandomGenerator::global()->bounded(keys.size()));
    //随机设置一个增长量，-5到+5
    int change = QRandomGenerator::global()->bounded(-5, 6);
    //获取slice
    auto *slice = _name_map[key];
    //增加后的值
    int add_val = slice->value() + change ;
    if(add_val < 0){
        add_val = 0;
    }
    //将数据设置进去
    _name_map[key]->setValue(add_val);

    //并且更新label
    _name_map[key]->setLabel(QString("%1: %2%").arg(key)
                              .arg(slice->percentage()*100,0,'f',1));

    // 可选：动态调整某些扇区的突出显示
    // 例如，突出销量最高的水果
    qreal maxValue = -1;
    QString maxKey = "";
    //遍历水果map
    for(auto iter = _name_map.begin();
        iter != _name_map.end(); iter++){
        if(iter.value()->value() > maxValue){
            //更新key
            maxKey = iter.key();
            //更新最大值
            maxValue = iter.value()->value();
            continue;
        }
    }

    //遍历map
    for(auto iter = _name_map.begin();
        iter != _name_map.end(); iter++){

        //如果key最大则展开显示
        if(iter.key() == maxKey){
            iter.value()->setExploded(true);
            iter.value()->setPen(QPen(Qt::black, 2));
        }else{
            iter.value()->setExploded(false);
            iter.value()->setPen(QPen(Qt::black, 1));
        }
    }

}
```

优化两次循环为一次循环

``` cpp
void MainWindow::updateChart2()
{
    // 模拟数据变化：随机增加或减少某个水果的销量
    QStringList keys = _name_map.keys();
    //随机选择一个key
    QString key = keys.at(QRandomGenerator::global()->bounded(keys.size()));
    //随机设置一个增长量，-5到+5
    int change = QRandomGenerator::global()->bounded(-5, 6);
    //获取slice
    auto *slice = _name_map[key];
    //增加后的值
    qreal add_val = slice->value() + change ;
    if(add_val < 0){
        add_val = 0;
    }
    //将数据设置进去
    _name_map[key]->setValue(add_val);

    //并且更新label
    _name_map[key]->setLabel(QString("%1: %2%").arg(key)
                              .arg(slice->percentage()*100,0,'f',1));

    // 可选：动态调整某些扇区的突出显示
    // 例如，突出销量最高的水果
    qreal maxValue = -1;
    QPieSlice* last_slice_max = nullptr;
    //遍历水果map
    for(auto iter = _name_map.begin();
        iter != _name_map.end(); iter++){
        //当前值比最大值大，就暂时更新展开
        if(iter.value()->value() > maxValue){

            //将上一次最大的扇区设置为不可展开
            if(last_slice_max){
               last_slice_max->setExploded(false);
               last_slice_max->setPen(QPen(Qt::black, 1));
            }

            //将本扇区设置为最大
            iter.value()->setExploded(true);
            iter.value()->setPen(QPen(Qt::black,2));
            //更新最大扇区
            last_slice_max = iter.value();
            //更新最大值
            maxValue = iter.value()->value();
            continue;
        }

        //当前值比最大值小，设置为不展开即可
        iter.value()->setExploded(false);
        iter.value()->setPen(QPen(Qt::black,1));
    }

}
```

### 捕获事件信号

饼状图也可以捕获点击事件和悬浮事件信号

被点击时饼状图会发出信号

``` cpp
[signal] void QPieSlice::clicked()
```

鼠标悬浮会发出下面这个信号

``` cpp
[signal] void QPieSlice::hovered(bool state)
```

所以我们在构造函数里连接这两个信号，并且实现对应的槽函数，大家好久没用lambda表达式了，这里带着大家用lambda表达式写槽函数

``` cpp
    //连接点击信号
    for(auto slice : _name_map){
        connect(slice,&QPieSlice::clicked,[=](){
            // 弹出提示
            QMessageBox::information(this, "扇区点击",
          QString("您点击了 %1，销量为 %2")
           .arg(slice->label()).arg(slice->value()));
        });
    }

    //连接悬浮信号
    for(auto slice : _name_map){
        connect(slice,&QPieSlice::hovered, [=](bool state){
            if (slice && state) {
                QString tooltipText = QString("%1: 销量为 %2")
                        .arg(slice->label())
                        .arg(slice->value());
                QToolTip::showText(QCursor::pos(), tooltipText, chartView);
            } else {
                QToolTip::hideText();
            }
        });
    }
```

### 柱状图

**Qt 柱状图的核心组件**

在 Qt Charts 中，绘制柱状图主要涉及以下核心组件：

- **QBarSet**：用于存储柱状图中的一组数据。
- **QBarSeries**：包含多个 `QBarSet`，代表一组柱状图。
- **QChart**：图表的核心对象，管理所有的系列、图例和标题。
- **QChartView**：用于在界面上显示 `QChart` 的视图组件，类似于 `QGraphicsView`。
- **QValueAxis** 和 **QCategoryAxis**：用于设置图表的值轴和类别轴。

#### 示例场景

完成基本的柱状图

![https://cdn.llfc.club/1727406895121.png](https://cdn.llfc.club/1727406895121.png)

Jane, John,Axel对应的就是三个QBarSet，我们分别向三个QBarSet写入六组数据，对应的就是下面六个月分产生的纵轴的值。

**解决思路**

1 先在构造函数中添加柱状图要用到的成员

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;
    // Qt Charts 成员
    QChartView *chartView;
    QChart *chart;
    QBarSeries *series;
    //三个集合，每个坐标对应三个柱子
    QBarSet *set0;
    QBarSet *set1;
    QBarSet *set2;
};
```

实现构造函数

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),
    chartView(new QChartView(this))
    , chart(new QChart())
    , series(new QBarSeries())
    , set0(new QBarSet("Jane"))
    , set1(new QBarSet("John"))
    , set2(new QBarSet("Axel"))
{
    ui->setupUi(this);

    // 初始化数据
     *set0 << 1 << 2 << 3 << 4 << 5 << 6;
     *set1 << 5 << 0 << 0 << 4 << 0 << 7;
     *set2 << 3 << 5 << 8 << 13 << 8 << 5;

     // 添加 QBarSet 到 QBarSeries
     series->append(set0);
     series->append(set1);
     series->append(set2);

     // 添加系列到图表
     chart->addSeries(series);
     chart->setTitle("简单的柱状图示例");
     chart->setAnimationOptions(QChart::SeriesAnimations);

     // 设置类别轴
     QStringList categories;
     categories << "Jan" << "Feb" << "Mar" << "Apr" << "May" << "Jun";
     QBarCategoryAxis *axisX = new QBarCategoryAxis();
     axisX->append(categories);
     chart->addAxis(axisX, Qt::AlignBottom);
     series->attachAxis(axisX);

     // 设置值轴
     QValueAxis *axisY = new QValueAxis();
     axisY->setRange(0, 15);
     chart->addAxis(axisY, Qt::AlignLeft);
     series->attachAxis(axisY);

     // 设置图表到视图
     chartView->setChart(chart);
     chartView->setRenderHint(QPainter::Antialiasing);

     // 设置布局
     QVBoxLayout *layout = new QVBoxLayout();
     layout->addWidget(chartView);

     QWidget *widget = new QWidget();
     widget->setLayout(layout);
     setCentralWidget(widget);

     resize(800,600);
}
```

###  柱状图美化(扩展内容)

为了使柱状图更具美观性和可读性，可以进行多种定制和美化操作，包括：



- 设置柱状条颜色
- 添加标签和数值
- 设置轴和标题
- 设定图表主题
- 添加动画效果

#### 设置柱状条颜色

可以为不同的柱状条设置不同的颜色，以增强视觉效果。

``` cpp
// 设置每个 QBarSet 的颜色
set0->setColor(Qt::red);
set1->setColor(Qt::green);
set2->setColor(Qt::blue);
```

将以上代码添加到 `mainwindow.cpp` 中 `// 添加 QBarSet 到 QBarSeries` 之后。



#### 添加标签和数值

为柱状条添加标签，以显示数值信息。

```cpp
// 显示每个柱状条的数值标签
set0->setLabelRotation(0);
set1->setLabelRotation(0);
set2->setLabelRotation(0);

set0->setLabelVisible(true);
set1->setLabelVisible(true);
set2->setLabelVisible(true);
```

将以上代码添加到柱状条颜色设置之后。



#### 设置轴和标题

自定义轴的范围、标题等属性。

```cpp
// 设置 X 轴标题
axisX->setTitleText("月份");

// 设置 Y 轴标题
axisY->setTitleText("销售量");
```

将以上代码添加到轴设置之后。

#### 设定图表主题

Qt Charts 提供了多种内置主题，可以快速改变图表的整体风格。

```cpp
chart->setTheme(QChart::ChartThemeQt);
```

可选主题列表包括：



- `ChartThemeLight`
- `ChartThemeBlueCerulean`
- `ChartThemeDark`
- `ChartThemeBrownSand`
- `ChartThemeBlueNcs`
- `ChartThemeHighContrast`
- `ChartThemeBlueIcy`
- `ChartThemeQt`（默认）



将以上代码添加到图表初始化部分。

#### 添加动画效果

通过设置动画选项，使图表在数据变化时具有过渡效果。

```cpp
chart->setAnimationOptions(QChart::AllAnimations);
```

###   动态更新柱状图

在MainWindow的构造函数中我们将原来加载数据的方式改为先初始化三个QVector容器，里面存储我们将要用到的数据

``` cpp
    //分别初始化三组数据，将来用作三个BarSet
    data0 = {1, 2, 3, 4, 5, 6};
    data1 = {5, 0, 0, 4, 0, 7};
    data2 = {3, 5, 8, 13, 8, 5};
```

因为三个QVector大小一致，我们可以通过一次遍历分别取出vector中的元素添加到不同的QBarSet中

``` cpp
    //初始化三个BarSet
    for(int i = 0; i < data0.size(); i++){
        //依次向三个集合添加数据
        set0->append(data0[i]);
        set1->append(data1[i]);
        set2->append(data2[i]);
    }
```

之后的逻辑和之前是一致的, 我们这里创建定时器

``` cpp
     //初始化定时器
     timer = new QTimer(this);
     //连接定时器超时逻辑
     connect(timer, &QTimer::timeout,this, &MainWindow::updateChart);

     //每隔2s更新依次
     timer->start(2000);
```

定时器的回调函数

``` cpp
void MainWindow::updateChart(){
    int maxVal = -1;
    // 模拟数据变化：随机增加或减少每个 QBarSet 的值
       for (int i = 0; i < set0->count(); ++i) {
           int change0 = QRandomGenerator::global()->bounded(-2, 3); // -2到+2
           int change1 = QRandomGenerator::global()->bounded(-2, 3);
           int change2 = QRandomGenerator::global()->bounded(-2, 3);

           data0[i] += change0;
           data1[i] += change1;
           data2[i] += change2;

           // 确保数据不为负数
           if (data0[i] < 0) data0[i] = 0;
           if (data1[i] < 0) data1[i] = 0;
           if (data2[i] < 0) data2[i] = 0;

           // 更新 QBarSet 的值
           set0->replace(i,data0[i]);
           set1->replace(i,data1[i]);
           set2->replace(i,data2[i]);

           //定义QList用来获取最大值
           QList<int> temp_list;
           temp_list << data0[i] << data1[i] << data2[i] << maxVal;
           //获取最大元素的迭代器
           auto max_iter = std::max_element(temp_list.begin(),temp_list.end());
           if(max_iter != temp_list.end()){
                maxVal = *max_iter;
           }

       }

       qDebug() << "maxval is " << maxVal;
       // 动态调整 Y 轴范围
       // 基类向子类转换用qobject_cast
       QValueAxis *axisY = qobject_cast<QValueAxis*>(chart->axisY());
       if (axisY) {
           axisY->setRange(0, maxVal + 5);
       }
}
```

再次启动程序，运行后会发现每隔两秒数据就更新一次。

### 捕获事件信号

想实现如下图的悬浮效果

![https://cdn.llfc.club/1727419521604.jpg](https://cdn.llfc.club/1727419521604.jpg)

QBarSet同样具有点击信号和悬浮信号

被点击时发出如下信号

``` cpp
[signal] void QBarSet::clicked(int index)
```

悬浮时发出信号

``` cpp
[signal] void QBarSet::hovered(bool status, int index)
```

在构造函数中连接点击信号

``` cpp
     //连接点击信号
     for(auto & bar_set : series->barSets()){
         //连接点击事件
        connect(bar_set, &QBarSet::clicked,
                this,&MainWindow::handleBarClicked);
     }
```

实现点击函数，因为信号里只有一个index，我们需要通过`sender()`方法获取发送信号的对象，`sender()`返回的是`QObject`,进而转为具体的对象类型

``` cpp
//处理点击事件
void MainWindow::handleBarClicked(int index)
{
    //此处获得信号的发送者
    QBarSet *barSet = qobject_cast<QBarSet*>(sender());
     if (barSet) {
         QMessageBox::information(this, "柱状条点击",
                QString("您点击了 %1, 数据为 %2").arg(barSet->label())
                                  .arg(barSet->at(index)));
     }
}
```

同样在构造函数中连接悬浮信号

``` cpp
     //连接信号
     for(auto & bar_set : series->barSets()){
         //连接点击事件
        connect(bar_set, &QBarSet::clicked,
                this,&MainWindow::handleBarClicked);

        //连接悬浮信号
        connect(bar_set,&QBarSet::hovered,
                this,&MainWindow::handleBarHovered);
     }
```

实现悬浮事件回调函数

``` cpp
//处理鼠标悬浮事件
void MainWindow::handleBarHovered(bool status, int index)
{
    //此处获得信号的发送者
    QBarSet *barSet = qobject_cast<QBarSet*>(sender());
    if(!barSet){
        return;
    }

    //处理未悬浮在数据的情况
    if (!status) {
        QToolTip::hideText();
     }

    auto label_str = barSet->label();
    auto num = barSet->at(index);

    QToolTip::showText(QCursor::pos(),
                       QString("%1:数据为%2").arg(label_str).arg(num));
}
```





# 第十章 多线程

## QThread简介

**多线程的优势包括：**

- **提高响应性：** 使用户界面保持流畅，即使在执行长时间运行的任务时。
- **提高性能：** 利用多核处理器，实现并行计算，加快任务完成速度。
- **资源管理：** 更灵活地管理系统资源，优化应用程序性能。



一个应用是不可能只有一个线程的，至少包括三个线程：

- 渲染线程：用来渲染界面，做ui，特效等处理。
- 网络线程：用来收发数据
- 数据处理线程：用来管理数据，计算，存储等。

这么做的好处就是逻辑解耦，不会因为界面刷新导致网络收发出现卡顿，也不会因为频繁计算导致界面卡死。

![https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234262768768.png](https://cdn.llfc.club/%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_17234262768768.png)



**Qt 提供了强大的多线程支持**，其中 `QThread` 类是实现多线程编程的核心。通过正确使用 `QThread`，开发者可以在 Qt 应用程序中实现高效的并行处理，保持用户界面的流畅响应。

## QThread 的工作原理



`QThread` 是 Qt 提供的跨平台线程类，基于操作系统的线程实现。每个 `QThread` 对象代表一个独立的线程，可以在该线程中执行耗时任务，避免阻塞主线程（通常是 UI 线程）。



**关键概念：**



- **主线程（UI 线程）：** 负责处理用户界面和事件循环。应该避免在此线程中执行耗时任务。
- **工作线程：** 独立于主线程的线程，用于执行后台任务。
- **事件循环：** 每个线程都有自己的事件循环，用于处理信号、槽和事件。



## **QThread 的基本工作流程：**



1. **创建 QThread 对象：** 可以通过继承 `QThread` 或与 `QObject` 结合使用。
2. **启动线程：** 调用 `start()` 方法，线程开始执行。
3. **执行任务：** 在新线程中执行需要的任务。
4. **结束线程：** 任务完成后，线程自动退出，或者通过代码控制结束。



**QThread 的两种主要使用方式：**



1. **继承 `QThread` 并重写 `run()` 方法：** 直接在子类中实现线程的执行逻辑。
2. **使用move方式将任务一角给QThread：** 将耗时任务封装在 `QObject` 派生类中，通过move方式移交到 `QThread`，实现任务在独立线程中执行。



后一种方法被广泛认为是更安全、更灵活的方式，避免了很多继承方式带来的问题。

## 继承方式创建QThread

这种方法通过继承 `QThread` 类并重写其 `run()` 方法来实现线程逻辑。`run()` 方法中可以包含需要在线程中执行的代码。

我们看一下QThread的构造函数

``` cpp
explicit QThread(QObject *parent = nullptr);
```

所以子类继承QThread，子类构造也写成显示构造，并且参数为`QObject*`即可。

QThread有一个run函数，我们需要在子类中重写

``` cpp
virtual void run();
```

线程启动函数为, 不传递参数就是默认启动

``` cpp
[slot] void QThread::start(QThread::Priority priority = InheritPriority)
```

传递参数 就是设置优先级, QT提供了几种设置优先级的方式

以下是 `QThread::Priority` 枚举的常量：



1. **`QThread::IdlePriority`**: 表示空闲优先级。线程将仅在系统空闲时运行。
2. **`QThread::LowestPriority`**: 表示最低优先级。线程的优先级低于正常优先级。
3. **`QThread::LowPriority`**: 表示低优先级。线程的优先级低于正常优先级，但高于最低优先级。
4. **`QThread::NormalPriority`**: 表示正常优先级。线程的默认优先级。
5. **`QThread::HighPriority`**: 表示高优先级。线程的优先级高于正常优先级。
6. **`QThread::HighestPriority`**: 表示最高优先级。线程的优先级高于所有其他优先级。
7. **`QThread::TimeCriticalPriority`**: 表示时间关键优先级。此优先级用于需要及时处理的线程。
8. **`QThread::InheritPriority`**: 表示继承优先级。线程将继承其父线程的优先级。



线程启动后是在后台运行的，如果主线程退出，也就代表了主进程退出，此时子线程也会被回收，所以有时候需要在主线程中等待子线程执行完，主线程再退出。

等待子线程退出，需要调用如下函数

``` cpp

bool wait(unsigned long time = ULONG_MAX)

```

wait函数如果不传递参数表示无限制的等待直到线程运行完成

否则传递的参数表示最多等待指定毫秒时间

**特别注意**

因为我们自己定义的线程类需要发送信号，根据前面学过的元对象机制，**我们需要在自己定义的类里添加`Q_OBJECT`宏声明**。

所以我们自定声明的线程类应该是这个样子

``` cpp
#include <QThread>

class WorkerThread : public QThread
{
    Q_OBJECT
public:
    //显示构造，并且指定父节点
    explicit WorkerThread(QObject *parent = nullptr);
    //要重写的run函数
    virtual void run() override;
};
```

接下来实现构造函数

``` cpp
WorkerThread::WorkerThread(QObject* parent):QThread(parent)
{

}
```

重写线程执行函数

``` cpp
void WorkerThread::run()
{
    qDebug() << "线程开始：" << QThread::currentThreadId();
    // 执行耗时任务
    for(int i = 0; i < 5; ++i) {
        qDebug() << "计数：" << i;
        sleep(1); // 模拟耗时操作
    }
    qDebug() << "线程结束：" << QThread::currentThreadId();
}
```

重写的函数里我们打印了5个数字，每打印1次睡眠1s。并且在开始和结束的时候打印了线程id。

然后我们在主函数中启动线程并且等待线程退出

``` cpp
#include <QApplication>
#include "workerthread.h"

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建线程
    WorkerThread thread;
    //启动线程
    thread.start();
    //等待线程退出
    thread.wait();
    return a.exec();
}
```



程序输出

``` cpp
线程开始： 0x9fe0
计数： 0
计数： 1
计数： 2
计数： 3
计数： 4
线程结束： 0x9fe0
```

因为a.exec()阻塞，所以主线程没有退出。

**进阶思考：阻塞UI**

如果我把主函数调用改成启动mainwindow，然后在`show()`函数后调用`thread.wait()`，在线程运行期间，界面能响应点击事件吗？

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建线程
    WorkerThread thread;
    //启动线程
    thread.start();
    MainWindow mainwindow;
    mainwindow.show();
    //等待线程退出
    thread.wait();
    return a.exec();
}
```

**答案是子线程运行的时候，主界面不能响应点击事件。**

这段代码运行后，会看到鼠标在主界面上转圈圈。直到子线程运行结束后，鼠标才恢复正常。

因为在线程运行期间，主线程会阻塞等待子线程`thread.wait`返回，进而不会走入a.exec()，a.exec()是执行事件循环的函数，

因为子线程运行期间，主线程没有执行事件循环，所以主线程不会响应ui事件。



**修改优化**

我们可以把等待子线程退出放在`a.exec()`之后即可

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建线程
    WorkerThread thread;
    //启动线程
    thread.start();
    MainWindow mainwindow;
    mainwindow.show();
    //a.exec()阻塞执行事件轮询
    int res = a.exec();
    //等待线程退出
    thread.wait();
    return res;
}
```

**再谈事件轮询**

`a.exec()`是执行事件轮询，而且是阻塞函数，内部执行死循环通过轮询的方式检测每隔QObject对象的事件队列，如果有未处理的就处理，直到所有的消息都处理完。

所以我们可以得出结论，只要一个对象继承了QObject，并且这个对象有任务或者事件未完成，这个`exec()`就不会返回。



**进阶思考：后台运行不等待**

如果我启动一个子线程后，主线程不等待，直接退出会怎样？

将main函数改为如下

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建线程
    WorkerThread thread;
    //启动线程
    thread.start();
    //等待任务执行完成退出
    return a.exec();
}
```

上面的程序会等到子线程执行完退出，因为子线程是继承自QThread的类，在子线程有任务未完成时，主线程的`exec()`不会退出。

上面的程序输出

``` cpp
线程开始： 0x9e40
计数： 0
计数： 1
计数： 2
计数： 3
计数： 4
线程结束： 0x9e40
```

好的，那么我们接下来不调用`a.exec()`会怎么样呢？

代码改成如下

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //创建线程
    WorkerThread thread;
    //启动线程
    thread.start();
    //无窗口则直接退出
    return 0;
}
```

程序运行后会出现如下异常

![https://cdn.llfc.club/1727427923768.jpg](https://cdn.llfc.club/1727427923768.jpg)

这段报错的意思是主线程退出的时候回收子线程，但是子线程仍然在运行。

所以程序异常结束了。

**使用心得**

所以同学们使用多线程的时候一定要注意线程的生命周期，一定要等待子线程运行结束后主线程再退出，否则会出现主线程退出强制回收子线程，如果子线程未完成任务被强制回收会导致进程异常。

## Move方式创建线程

这种方法通过将工作逻辑封装在一个 `QObject` 派生类中，并将其移动到 `QThread` 对象中执行。通过信号和槽实现线程间通信。移动过后任务类归属于QThread子线程。

QObject移动到线程的方法

``` cpp
void QObject::moveToThread(QThread *targetThread)
```



**优点：**



- 更加符合 Qt 的信号槽机制。
- 更容易管理线程生命周期。
- 提高代码的可维护性和可扩展性。

我们先实现一个自定义的Worker任务类，使其继承自QObject，但是要注意，类的声明一定要包含Q_OBJECT宏

``` cpp
class Worker : public QObject
{
    Q_OBJECT
public:
    //显示构造worker类
    explicit Worker(QObject *parent = nullptr);
signals:

public slots:
    //响应线程started信号
    void doWork();
signals:
    //任务完成后发出这个信号
    void finished();
};
```

实现构造函数

``` cpp
Worker::Worker(QObject *parent) : QObject(parent)
{

}
```

实现开始任务的槽函数

``` cpp
void Worker::doWork()
{
    qDebug() << "工作线程开始：" << QThread::currentThreadId();
    for(int i = 0; i < 5; i++){
        qDebug() << "计数：" << i;
        QThread::sleep(1); // 模拟耗时操作
    }
    //发送结束信号
    emit finished();
    qDebug() << "工作线程结束：" << QThread::currentThreadId();
}
```

在主函数中创建一个线程，并且将这个任务类移交给线程

**注意**

被移交的类一定不能有父窗口

``` cpp
    //创建一个新的线程
    QThread* worker_thread = new QThread();
    //创建任务类
    Worker* worker = new Worker();

    //将worker移动到线程里
    worker->moveToThread(worker_thread);
```

因为我们要通过线程的信号通知任务类开始工作，以及任务类要通过完成信号通知线程退出等，这里先列举几个信号

QThread线程开始信号，该信号在调用QThread的start()方法后由QThread发出

``` cpp
[signal] void QThread::started()
```

QThread线程结束信号，在线程调用quit()或者正常退出时发出这个信号

``` cpp
[signal] void QThread::finished()
```

我们先捕获线程的开始信号, 因为连接信号不是在QObject类里，所以显示调用QObject作用域连接

``` cpp
//连接线程开始信号
QObject::connect(worker_thread,&QThread::started,worker,&Worker::doWork);
```

所有QObject都有一个deleteLater槽函数

``` cpp
[slot] void QObject::deleteLater()
```

捕获线程退出信号，连接线程自己的`deleteLater`槽函数，

``` cpp
//连接线程退出信号和回收槽函数
QObject::connect(worker_thread, &QThread::finished, worker_thread, &QThread::deleteLater);
```

连接worker退出信号和回收槽函数

``` cpp
//连接worker退出信号和回收槽函数
QObject::connect(worker,&Worker::finished,worker,&Worker::deleteLater);
```

启动线程

``` cpp
//启动线程
worker_thread->start();
```

完整版代码

``` cpp
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    
    //创建一个新的线程
    QThread* worker_thread = new QThread();
    //创建任务类
    Worker* worker = new Worker();

    //将worker移动到线程里
    worker->moveToThread(worker_thread);

    //连接线程开始信号
    QObject::connect(worker_thread,&QThread::started,worker,&Worker::doWork);

    //连接任务类结束信号,调用线程退出信号
    QObject::connect(worker,&Worker::finished, worker_thread, &QThread::quit);

    //连接线程退出信号和回收槽函数
    QObject::connect(worker_thread, &QThread::finished, worker_thread, &QThread::deleteLater);

    //连接worker退出信号和回收槽函数
    QObject::connect(worker,&Worker::finished,worker,&Worker::deleteLater);

    //启动线程
    worker_thread->start();
    MainWindow mainwindow;
    mainwindow.show();
    //等待任务执行完成退出
    return a.exec();
}
```

程序运行后,输出

``` cmd
工作线程开始： 0x4124
计数： 0
计数： 1
计数： 2
计数： 3
计数： 4
工作线程结束： 0x4124
```

因为a.exec()还在等待其他事件处理，所以主线程不会退出。

## 多线程的隐患

多线程提高了并发处理问题的能力，但也引发了资源竞争，比如有两个线程，分别对同一个全局变量进行修改，那么可能会导致修改错误。

我们看下如下界面, 点击开始后启动两个线程对global_num进行自增，global_num初始值为0，每个线程对global_num执行10万次自增加1运算，

计算结束后会通知主界面显示计算结果，主界面显示的不是20万，说明多线程并行访问共享资源会出问题。



![https://cdn.llfc.club/1727586063643.jpg](https://cdn.llfc.club/1727586063643.jpg)



**实现细节**

我们创建一个项目，叫做ThreadProblem.

然后右键项目，添加头文件和源文件，叫做global.h和global.cpp

我们在global.h中添加全局变量global_num的声明，

``` cpp
extern int global_num;
```

在global.cpp中添加定义

``` cpp
int global_num = 0;
```

接下来进入mainwindow.ui将布局设置为界面所需样式

![https://cdn.llfc.club/1727580670390.jpg](https://cdn.llfc.club/1727580670390.jpg)

修改层级属性如下：

![https://cdn.llfc.club/1727580825778.jpg](https://cdn.llfc.club/1727580825778.jpg)



**接下来我们先实现ThreadWorker的声明**

``` cpp
class ThreadWorker : public QObject
{
    Q_OBJECT
public:
    explicit ThreadWorker(QObject *parent = nullptr);
public slots:
    // 线程启动后执行的任务
    void slot_work();
    // 停止工作
    void slot_stopwork();
private:
    bool _run;
signals:
    // 任务完成时发出的信号
    void sig_finished();
    // 数字变化的信号
    void sig_num_changed(int num);
};
```

ThreadWorker中我们声明了几个成员和槽函数，以及信号：

- slot_work：该槽函数用来响应线程started信号，执行对应的任务。
- slot_stopwork：该函数用来响应mainwindow发过来的sig_stop_thread信号。
- _run：表示线程是否处于运行中
- sig_finished：任务完成时会发送该信号
- sig_num_changed：ThreadWorker内部修改数字后会发出该信号



ThreadWorker构造函数,  初始化运行状态为false

``` cpp
ThreadWorker::ThreadWorker(QObject *parent) : QObject(parent),_run(false)
{

}
```

实现`slot_work`函数，任务类在线程启动后执行该函数，并且对全局变量进行自增，任务结束后发送信号通知主界面显示

任务完成后发送sig_finished信号退出

``` cpp
void ThreadWorker::slot_work()
{
    _run = true;
    int index= 0;
    while(_run && index < 100000){
        //对全局变量累加1
        global_num += 1;
        index++;
    }

    //发送数字变化信号
    emit sig_num_changed(global_num);
    //发送完成信号
    emit sig_finished();
}
```

停止工作槽函数

``` cpp
void ThreadWorker::slot_stopwork()
{
    _run = false;
}
```



接下来我们实现MainWindow构造函数，构造函数中我们创建两个线程，两个worker，将worker移动到线程里。

并且要连接几个信号：

1. 首先一个线程启动后，必须要通知到worker执行任务
2. 其次任务完成后要通知线程退出
3. 主界面点击结束按钮或者主界面退出时要发送停止信号通知worker结束任务
4. 结束任务不能直接返回，要等待线程退出。
5. 因为worker要移动到QThread中所以不要创建父节点
6. 因为QThread和QThreadWorker要被反复利用(开始和结束可交替点击)，所以工作类对象留在MainWindow析构函数回收
7. 连接两个worker的数字变化信号，这里问大家一个问题，两个线程并发的发送信号，槽函数在另一个线程，连接的方式采用的是什么？发送的信号会同时处理还是排队处理？虽然排队处理，但是要注意信号发送的时序性，后面讲



``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    //创建两个线程
    _thread1 = new QThread(this);
    _thread2 = new QThread(this);
    //创建两个worker
    _worker1 = new ThreadWorker();
    _worker2 = new ThreadWorker();
    //将worker_1移动给thread_1， 将worker_2移动给thread_2
    _worker1->moveToThread(_thread1);
    _worker2->moveToThread(_thread2);

    //连接线程开始信号
    connect(_thread1, &QThread::started, _worker1, &ThreadWorker::slot_work);
    connect(_thread2, &QThread::started, _worker2, &ThreadWorker::slot_work);

    //连接主界面退出信号
    connect(this, &MainWindow::sig_stop_thread, _worker1, &ThreadWorker::slot_stopwork);
    connect(this, &MainWindow::sig_stop_thread, _worker2, &ThreadWorker::slot_stopwork);

    //连接任务结束信号
    connect(_worker1, &ThreadWorker::sig_finished, _thread1, &QThread::quit);
    connect(_worker2, &ThreadWorker::sig_finished, _thread2, &QThread::quit);

    //默认只开启开始按钮，关闭按钮不可用
    ui->startBtn->setEnabled(true);
    ui->stopBtn->setEnabled(false);

    //连接数字变化信号和界面显示
    connect(_worker1, &ThreadWorker::sig_num_changed,this,&MainWindow::slot_num_changed);
    connect(_worker2, &ThreadWorker::sig_num_changed,this,&MainWindow::slot_num_changed);

}

```

析构函数要做几件事：

1. 如果主窗口退出，线程也要被回收
2. 线程不能被强制回收，需要等待线程任务完成
3. 因为线程任务是耗时的任务，所以要通知任务类结束工作

``` cpp
MainWindow::~MainWindow()
{
    //发送信号通知线程结束
    emit sig_stop_thread();
    //等待线程退出
    _thread1->wait();
    _thread2->wait();

    //回收worker
    _worker1->deleteLater();
    _worker2->deleteLater();
    delete ui;
}
```

开始按钮点击后：

1. 为避免重复点击开始，将开始按钮设置为不可点击，
2. 并且启动线程，然后再将停止按钮激活

``` cpp
void MainWindow::on_startBtn_clicked()
{
    //开始按钮置为false，防止重复点击
    ui->startBtn->setEnabled(false);
    //先把初始值设置为 0
    global_num = 0;
    //启动两个线程
    _thread1->start();
    _thread2->start();
    //允许关闭线程按钮被点击
    ui->stopBtn->setEnabled(true);
}
```

结束按钮点击后：

1. 为避免重复点击，将结束按钮设置为不可点击
2. 发送停止信号通知任务终止，并且等待线程退出
3. 激活开始按钮

``` cpp
void MainWindow::on_stopBtn_clicked()
{
    //关闭按钮置为false，防止重复点击
    ui->stopBtn->setEnabled(false);
    //发送信号通知线程结束
    emit sig_stop_thread();
    //等待线程退出,线程触发quit()槽函数后发出finished信号，并且wait()直接返回
    _thread1->wait();
    _thread2->wait();

    //允许开启线程按钮被点击
    ui->startBtn->setEnabled(true);
}
```

主界面响应数字变化，(虽然槽函数是通过队列处理，但是线程A计算迅速，发送信号却很慢，线程B计算慢，发送信号却很快，导致最后label刷新的是先计算的结果，为避免这种问题，我们在槽函数中访问全局变量进行刷新)。可以给学生举例（学生算的快，但是口吃的案例）

``` cpp
void MainWindow::slot_num_changed(int num)
{
    Q_UNUSED (num);
    //为避免多线程发送信号，顺序问题导致数字显示不准确
    //改为获取全局变量
    auto num_str = QString("%1").arg(global_num);
    ui->numLabel->setText(num_str);
}
```

启动程序后，点击开始，会看到界面刷新出的标签显示global_num不是20万.

## 竞态条件和同步

**线程**是程序执行的最小单位，一个进程可以包含多个线程，多个线程共享进程的资源（如内存空间）。在多线程环境中，线程之间的并发执行可能导致对共享资源的竞争。

### 竞态条件（Race Condition）

**竞态条件**指的是多个线程同时访问和修改共享资源，且操作的顺序影响最终结果。竞态条件可能导致数据不一致或程序异常。

### 同步机制

为防止竞态条件，需要使用**同步机制**来控制线程对共享资源的访问，确保在任意时刻只有一个线程可以访问或修改资源。

### Qt中的同步机制概述



Qt提供了多种同步机制，主要包括：



- **QMutex**：互斥量，用于保护共享资源，确保同一时间只有一个线程访问资源。
- **QMutexLocker**：互斥锁的自动管理类，通过RAII（资源获取即初始化）模式管理锁的生命周期，避免忘记解锁。
- **QReadWriteLock**：读写锁，允许多个线程同时读取资源，但写操作时需要独占锁。
- **QWaitCondition：** 条件变量，用来控制线程挂起和唤醒

## QMutex：互斥量

### 基本用法

`QMutex`类提供了互斥锁功能，用于保护共享资源。典型用法如下：



1. 创建一个`QMutex`对象。
2. 在访问共享资源前调用`lock()`方法锁定互斥量。
3. 访问或修改共享资源。
4. 调用`unlock()`方法解锁互斥量。

``` cpp
QMutex mutex;

// 线程A执行加锁
mutex.lock();
// 访问共享资源
// 访问结束后解锁
mutex.unlock();
```

### **案例实战**

通过QMutex我们修改之前有问题的案例，因为我们之前是两个线程并行计算，所以要用统一的一个QMutex锁管理全局变量, 最终达到的效果是精准计算后，界面显示20万

![https://cdn.llfc.club/1727593563614.jpg](https://cdn.llfc.club/1727593563614.jpg)

**解决思路**

我们在global.h中声明一个全局的互斥量

``` cpp
#include <QMutex>

extern int global_num;
//全局的互斥量
extern QMutex global_mtx;
```

在global.cpp中定义它

``` cpp
QMutex global_mtx;
```

然后在任务计算global_mutex的时候我们加锁

``` cpp
//线程开始后执行的任务
void ThreadWorker::slot_work()
{
    _run = true;
    int index= 0;
    while(_run && index < 100000){
        //加锁
        global_mtx.lock();
        //对全局变量累加1
        global_num += 1;
        //解锁
        global_mtx.unlock();
        index++;
    }

    //发送数字变化信号
    emit sig_num_changed(global_num);
    //发送完成信号
    emit sig_finished();
}
```

再次运行就能看到显示的数字是20万了，准确数字

**提问**

同学们，如果我将global_mtx.lock()

## RAII技术

RAII（Resource Acquisition Is Initialization，资源获取即初始化）是一种C++编程技术，它将资源的获取（例如分配的堆内存、打开的文件、锁定的互斥量等）与对象的生命周期绑定在一起。具体来说，RAII的核心思想是：在对象的构造函数中获取资源，并在对象的析构函数中释放资源。

### RAII的特点和优势：



1. **自动资源管理**：通过将资源的生命周期与对象的生命周期绑定，RAII确保了资源在不再需要时自动释放，避免了资源泄漏。
2. **异常安全**：RAII能够提供异常安全性。如果在资源获取或使用过程中发生异常，RAII对象会在其析构时自动释放资源，从而避免了资源的泄漏。
3. **简化代码**：使用RAII可以减少手动管理资源的复杂性，使代码更加简洁和易于维护。
4. **提高可读性**：资源的获取和释放是在对象的构造和析构中进行的，使得资源管理的逻辑更加清晰。

我们可以利用RAII思想，创建一个MyLocker类，这个类对象构造时加锁，析构时解锁。

``` cpp
#include <QMutex>
class MyLocker
{

public:
    //构造函数接受互斥量，并加锁
    explicit MyLocker(QMutex* mtx);
    //析构函数解锁
    ~ MyLocker();
    //删除拷贝构造
    MyLocker(const MyLocker& ml) = delete ;
    //删除拷贝赋值
    MyLocker& operator=(const MyLocker& ml) = delete;
    //重写移动构造
    MyLocker(MyLocker&& ml) noexcept;
private:
    //互斥量指针
    QMutex* _pointer_mtx;
};
```

具体实现

``` cpp
#include "mylocker.h"

MyLocker::MyLocker(QMutex *mtx):_pointer_mtx(mtx)
{
   //加锁
    _pointer_mtx->lock();
}

MyLocker::~MyLocker()
{
    //解锁
    _pointer_mtx->unlock();
}

//移动构造函数
MyLocker::MyLocker(MyLocker &&ml) noexcept:_pointer_mtx(ml._pointer_mtx)
{

}
```

我们将原来的任务计算功能加锁改为我们自己封装的MyLocker类

``` cpp
//线程开始后执行的任务
void ThreadWorker::slot_work()
{
    _run = true;
    int index= 0;
    while(_run && index < 100000){
        //使用我们自定义的MyLocker自动加锁
        MyLocker locker(&global_mtx);
        //对全局变量累加1
        global_num += 1;
        index++;
    }

    //发送数字变化信号
    emit sig_num_changed(global_num);
    //发送完成信号
    emit sig_finished();
}
```

**那我问一下同学们，MyLocker什么时候对互斥量global_mtx解锁的？**

再次运行，可以看到每次点击启动线程，标签都是20万，说明我们RAII封装的自动解锁很方便。

## QMutexLocker：互斥锁的自动管理

QT给我们提供了自动加锁和解锁的类`QMutexLocker`，实现了之前我们做的MyLocker的类似的功能。

`QMutexLocker`是一个辅助类，用于自动管理`QMutex`的锁定与解锁。通过RAII（资源获取即初始化）模式，确保在作用域结束时自动释放锁，避免因异常或忘记调用`unlock()`导致的死锁。

**使用步骤：**



1. 创建一个`QMutexLocker`对象，并传入一个`QMutex`指针。
2. 在`QMutexLocker`对象的作用域内访问或修改共享资源。
3. 离开作用域时，`QMutexLocker`的析构函数自动释放锁。

其使用方式基本时如下结构

``` cpp
QMutex mutex;

// 线程A执行
{
    QMutexLocker locker(&mutex);
    // 访问共享资源
} // 自动解锁

// 线程B执行
{
    QMutexLocker locker(&mutex);
    // 访问共享资源
} // 自动解锁
```

**实战案例**

我们将之前写的计算数字的程序，改用QMutexLocker试试

``` cpp
//线程开始后执行的任务
void ThreadWorker::slot_work()
{
    _run = true;
    int index= 0;
    while(_run && index < 100000){
        //使用QMutexLocker加载
        QMutexLocker locker(&global_mtx);
        //对全局变量累加1
        global_num += 1;
        index++;
    }

    //发送数字变化信号
    emit sig_num_changed(global_num);
    //发送完成信号
    emit sig_finished();
}
```

效果和之前一样，可以实现数据安全计算。

## QReadWriteLock：读写锁



### 基本用法



`QReadWriteLock`允许多个线程同时读取共享资源，但在写入时需要独占锁。这在读多写少的场景下，提高了并发性能。



**使用步骤：**



1. 创建一个`QReadWriteLock`对象。
2. 在读取操作前调用`lockForRead()`，在完成后调用`unlock()`.
3. 在写入操作前调用`lockForWrite()`, 在完成后调用`unlock()`.



### 实战案例

我们对之前的程序稍作修改，这次我们采用读写锁的方式，两个线程对global_num进行修改，不再推送sig_number_changed信号，改为UI线程定时读取global_num,  如下图所示



![https://cdn.llfc.club/1727603292398.jpg](https://cdn.llfc.club/1727603292398.jpg)



**实现细节**



在global.h中添加QReadWriteLock声明

``` cpp
//全局读写锁声明
extern QReadWriteLock global_rw_lock;
```

在global.cpp中添加定义

``` cpp
QReadWriteLock global_rw_lock;
```

接下来实现任务类定时更新global_num

``` cpp
//线程开始后执行的任务
void ThreadWorker::slot_work()
{
    _run = true;
    int index= 0;
    while(_run && index < 100000){

        //使用QReadWriteLock加写锁
        global_rw_lock.lockForWrite();
        //对全局变量累加1
        global_num += 1;
        global_rw_lock.unlock();

        index++;
        //为了让label显示变化，延时1s
        QThread::sleep(1);
    }

    //发送完成信号
    emit sig_finished();
}
```

我们在mainwindow的构造函数里启动定时器

``` cpp
//创建定时器
auto * timer = new QTimer(this);
//连接信号和回调函数
connect(timer,&QTimer::timeout,[=](){
    //读写锁加读锁
    global_rw_lock.lockForRead();
    ui->numLabel->setText(QString("%1").arg(global_num));
    global_rw_lock.unlock();
});
//每隔1s触发一次回调
timer->start(1000);
```

再次运行，发现主界面定时更新数字到label上。

## 最佳实践与注意事项



### 避免死锁



**死锁（Deadlock）**是指两个或多个线程互相等待对方释放资源，从而导致程序永远阻塞。为了避免死锁，应遵循以下原则：



- **一致的锁定顺序**：所有线程按照相同的顺序获取多个锁。
- **尽量减少锁的持有时间**：仅在必要的代码块内持有锁。
- **避免嵌套锁**：尽量减少同时持有多个锁的情况。
- **使用`QMutexLocker`**：利用RAII模式自动管理锁的释放，避免因异常或逻辑错误导致锁未释放。



### 锁的粒度



- **粗粒度锁**：锁保护较大的代码块或多个资源，容易引发性能瓶颈。
- **细粒度锁**：锁保护较小的代码块或单一资源，提高并发性能，但增加了复杂性。



根据具体情况选择合适的锁粒度，权衡性能与复杂性。



### 选择合适的同步工具



不同的同步工具适用于不同的场景：



- **`QMutex`**：适用于简单的互斥保护。
- **`QMutexLocker`**：适用于需要自动管理锁的场景。
- **`QReadWriteLock`**：适用于读多写少的场景。



## QWaitCondition：条件变量



### 基本概念与用法



**条件变量**是一种同步机制，允许线程在某个条件不满足时阻塞，直到该条件由其他线程通知满足。Qt提供了`QWaitCondition`类，用于实现条件变量的功能。通常，`QWaitCondition`与`QMutex`结合使用，以确保在等待和通知过程中对共享资源的访问是安全的。



**典型用法：**



1. 创建一个`QWaitCondition`对象和一个`QMutex`对象。
2. 在线程中，当特定条件不满足时，使用`wait()`方法等待条件变量，同时锁定互斥量。
3. 当条件满足时，其他线程通过`wakeOne()`或`wakeAll()`方法通知等待的线程。
4. 等待线程在被通知后重新获取互斥量，并继续执行。



**关键方法：**



- `wait(QMutex *mutex)`：使调用线程等待，直到被唤醒。调用该方法前必须锁定互斥量，调用后会自动解锁，并在被唤醒后重新锁定。
- `wakeOne()`：唤醒一个等待的线程。
- `wakeAll()`：唤醒所有等待的线程。

### 应用场景

条件变量经常用于控制多线程访问资源，进行条件判断的场景。比如一个线程A向队列中放入数据，一个线程B从队列中取出数据。

线程A我们叫做生产者线程，线程B我们叫做消费者线程。

如果消费者线程取出数据比生产者线程放入数据的速度快，那么队列为空时，消费者线程就无法取出数据，我们常用的做法就是判断队列为空，就跳过本次循环继续循环，比如下面的逻辑

``` cpp
//模拟消费者线程做的事情
void consumerWork(){
    //消费者无限轮询工作
    while(true){
        //判断队列是否为空
        if(queue.isEmpty()){
            continue;
        }
        //取出数据
        queue.pop()
    }   
    
}
```

对于上面的代码，如果队列为空，则直接跳过，进入下一次循环，如果短时间内队列仍旧为空，会再次continue，要是一直为空这个循环就一直在空跑，循环空跑是对cpu资源最大的浪费！

有的同学可能会说，那就让消费者线程睡眠1s呗，消费者线程会等1s睡完之后才能处理，比如下面这样

``` cpp
//模拟消费者线程做的事情
void consumerWork(){
    //消费者无限轮询工作
    while(true){
        //判断队列是否为空
        if(queue.isEmpty()){
            //睡眠1s
            QThread::sleep(1);
            continue;
        }
        //取出数据
        queue.pop()
    }   
    
}
```

那如果在这1s之内生产者线程往队列里放入数据了呢？这样就不及时了，对于很多零延迟系统(游戏，即时交易，高并发场景等)是不允许的。



如果生产数据的线程放入数据的速度比消费者线程的速度快，那么很容易把队列撑爆，实际公司的场景会对队列设置最大大小，如果队列超过最大值，那么就不让生产者将数据放入，之前谈过消费者可以跳过，那生产者是不能跳过的，因为跳过放入队列的操作，就意味着数据丢失，这次数据没放入就丢掉了。这是无法容忍的。（比如同学们玩元神，氪金648后台将你的重置信息放入队列，但是因为今天活动太火爆了，充值队列撑爆了，你的消费信息无法放入队列被丢弃了，出现的后果就是钱花了原石被到账，坑爹吧）



所以遇到这些情况就不能跳过和重试，要让这个操作阻塞，直到队列满足条件后，操作继续，这样不会丢失数据，处理也足够及时。

### 生产者消费者问题

**单一生产者和消费者**

实现如下案例,  启动生产者和消费者线程，生产者线程向队列放入数据，消费者线程从队列中取出数据，并且两个线程将数据信息发送给MainWindow显示。

![https://cdn.llfc.club/1728208792258.jpg](https://cdn.llfc.club/1728208792258.jpg)

**全局文件**

我们需要实现全局文件global.h和global.cpp，用来声明和定义要使用的全局变量

``` cpp
#ifndef GLOBAL_H
#define GLOBAL_H
#include <QQueue>
#include <atomic>
#include <QMutex>
#include <QWaitCondition>
#include <QSet>


//全局队列，生产者和消费者共享
extern QQueue<int> _global_queue;
//生产者共享的计数
extern std::atomic<int> _global_num;
//互斥量，生产者和消费者共享
extern QMutex _global_mtx;
//生产者条件变量
extern QWaitCondition _global_producer_wc;
//消费者条件变量
extern QWaitCondition _global_consumer_wc;
//队列最大值
const int MAX_SIZE = 10;


extern void printQtThreadId(QString str);
#endif // GLOBAL_H

```

定义全局变量

``` cpp
#include "global.h"
#include <QThread>
#include <QDebug>

//全局队列，生产者和消费者共享
QQueue<int> _global_queue = {};
//生产者共享的计数
std::atomic<int> _global_num = {0};
//互斥量，生产者和消费者共享
QMutex _global_mtx;
//生产者条件变量
QWaitCondition _global_producer_wc;
//消费者条件变量
QWaitCondition _global_consumer_wc;

void printQtThreadId(QString str)
{
    qDebug() << str;
    Qt::HANDLE tid = QThread::currentThreadId();

    // 将 Qt::HANDLE 转换为 uintptr_t（无符号整数类型）
    quintptr numericTid = reinterpret_cast<quintptr>(tid);

    // 使用十六进制格式打印更具辨识度
    qDebug() << "Qt Thread ID:" << QString("0x%1").arg(numericTid, 0, 16);
    qDebug() << str;
}
```

**消费者任务类**

声明消费者信号和槽函数等

``` cpp
#ifndef CONSUMER_H
#define CONSUMER_H

#include <QObject>

class Consumer : public QObject
{
    Q_OBJECT
public:
    explicit Consumer(int id, QObject *parent = nullptr);
    ~Consumer();
signals:
    //更新主界面的信号
    void sig_consume_up(int con_id, int num, bool b_empty = false);
    //任务完成信号
    void sig_finished(int id);
public slots:
    //开始消费任务函数
    void consumeWork();
    //停止执行消费任务
    void stopWork(int id);
private:
    int _id;
    bool _b_run;
};

#endif // CONSUMER_H

```

实现具体的消费者类

``` cpp
#include "consumer.h"
#include "global.h"
#include <QThread>
#include <QDebug>

Consumer::Consumer(int id, QObject *parent) : QObject(parent),_id(id),_b_run(false)
{

}

Consumer::~Consumer()
{
    qDebug() << QString(" consumer [%1] destruct").arg(_id);
}

void Consumer::consumeWork()
{
    _b_run = true;
    bool flag = false;
    while(_b_run){
        //判断队列是否满了,需要先加锁
        _global_mtx.lock();
        //队列满了，需要用while循环判断，防止虚假唤醒
        while(_global_queue.size() <= 0 && _b_run){
            //通知主界面消费者队列为空
            emit  sig_consume_up(_id, 0, true);
            //生产者线程被挂起，直到消费者线程唤醒它
            _global_consumer_wc.wait(&_global_mtx);
        }

        //队列未满，或者被消费者唤醒，或者是主界面退出唤醒
        // 二次判断是否因为主界面退出唤醒
        if(!_b_run){
            //解锁
            _global_mtx.unlock();
            //发送结束信号
            emit sig_finished(_id);
            return;
        }

        auto temp = _global_queue.front();
        _global_queue.pop_front();
        //发送信号通知主界面刷新信息
        emit sig_consume_up(_id, temp);

        flag = false;
        if(_global_queue.size() == MAX_SIZE-1){
            flag = true;
        }
        //解锁
        _global_mtx.unlock();

        //发送通知唤醒生产者
        if(flag){
            _global_producer_wc.notify_one();
        }

        //为防止循环过快，小睡一会
        QThread::msleep(500);
    }

    //发送结束信号
    emit sig_finished(_id);
    return;
}

void Consumer::stopWork(int id)
{
    //界面停止信号会连接多个消费者，需要判断id是否为自己
    if(_id != id){
        return;
    }

    _global_mtx.lock();
    //是自己则退出
    _b_run = false;
    _global_consumer_wc.notify_all();
    _global_mtx.unlock();
}

```

**生产者任务类**

实现生产者任务类的声明

``` cpp
#ifndef PRODUCER_H
#define PRODUCER_H

#include <QObject>

class Producer : public QObject
{
    Q_OBJECT
public:
    //id为生产者id
    explicit Producer(int id, QObject *parent = nullptr);
    ~Producer();

public slots:
    //槽函数响应线程启动信号，模拟生产工作
    void produceWork();
    //槽函数响应主界面停止信号，结束任务
    void stopWork(int id);
private:
    //是否运行
   std::atomic<bool> _b_run;
    //生产者id
    int _id;
signals:
    //任务完成信号
    void sig_finished(int id);
    //发送信号通知主界面显示
    void sig_up_text(int id, int num, bool full = false);

};

#endif // PRODUCER_H

```

实现具体的定义

``` cpp
#include "producer.h"
#include "global.h"
#include <QThread>
#include <QDebug>

Producer::Producer(int id, QObject *parent): QObject(parent),_id(id)
{

}

void Producer::produceWork()
{
    _b_run = true;
    bool flag = false;
    while(_b_run){
        //判断队列是否满了,需要先加锁
        _global_mtx.lock();
         _global_num++;
         auto temp = _global_num.load();
        //队列满了，需要用while循环判断，防止虚假唤醒
        while(_global_queue.size()>=MAX_SIZE && _b_run ){
            //通知主界面生产者满了
            emit  sig_up_text(_id, temp, true);
            //生产者线程被挂起，直到消费者线程唤醒它
            _global_producer_wc.wait(&_global_mtx);
        }

        //队列未满，或者被消费者唤醒，或者是主界面退出唤醒
        // 二次判断是否因为主界面退出唤醒
        if(!_b_run){
            //解锁
            _global_mtx.unlock();
            //发送结束信号
            emit sig_finished(_id);
            return;
        }


        _global_queue.push_back(temp);
        //发送信号通知主界面刷新信息
        emit sig_up_text(_id, temp);

        flag = false;

        if(_global_queue.size() == 1){
            flag = true;
        }
        //解锁
        _global_mtx.unlock();

        //通知消费者唤醒
        if(flag){
           _global_consumer_wc.notify_one();
        }

        //为防止循环过快，小睡一会
        QThread::msleep(500);
    }

    //发送结束信号
    emit sig_finished(_id);
    return;
}

Producer::~Producer()
{
    qDebug() << QString(" producer [%1] destruct").arg(_id);
}

void Producer::stopWork(int id)
{
    //界面停止信号会连接多个生产者，需要判断id是否为自己
    if(_id != id){
        return;
    }

    _global_mtx.lock();
    //是自己则退出
    _b_run = false;
    _global_producer_wc.notify_all();
    _global_mtx.unlock();
}
```

**MainWindow启动生产者和消费者**

声明

``` cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>

namespace Ui {
class MainWindow;
}

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    //点击启动消费者按钮响应的槽函数
    void on_consumerBtn_clicked();
    //点击停止消费者按钮响应的槽函数
    void on_constopBtn_clicked();
    //点击启动生产者按钮响应的槽函数
    void on_producerBtn_clicked();
    //点击停止生产者按钮响应的槽函数
    void on_prostopBtn_clicked();

    //响应生产者线程发过来的消息显示到界面上
    void slot_up_text(int id, int num, bool full);
    //响应消费者线程发过来的消息显示到界面上
    void slot_consume_text(int id, int num, bool b_empty);

private:
    Ui::MainWindow *ui;

signals:
    //停止某个生产者信号
    void sig_stop_produce(int id);
    //停止某个消费者信号
    void sig_stop_consumer(int id);
};

#endif // MAINWINDOW_H

```

具体实现

``` cpp
#include "mainwindow.h"
#include "ui_mainwindow.h"
#include <QThread>
#include "global.h"
#include "producer.h"
#include <QMessageBox>
#include <QDebug>
#include "consumer.h"

MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),_worker_id(0)
{
    ui->setupUi(this);
}

MainWindow::~MainWindow()
{
    //通知生产者结束工作
    for(auto iter = _map_producers.begin();
        iter != _map_producers.end(); iter++){
        iter.value()->stopWork(iter.key());
    }

    //等待线程退出
    for(auto& thread: _map_producer_thread){
        thread->wait();
    }

    //通知消费者结束工作
    for(auto iter = _map_consumers.begin();
        iter != _map_consumers.end(); iter++){
        iter.value()->stopWork(iter.key());
    }

    //等待线程退出
    for(auto& thread: _map_consumer_thread){
        thread->wait();
    }


    delete ui;
}

void MainWindow::on_addProducerBtn_clicked()
{
    //创建线程
    auto thread = std::make_shared<QThread>();
    //增加id
    _worker_id++;
    //创建生产者
    auto producer = new Producer(_worker_id);
    //放入线程
    producer->moveToThread(thread.get());
    //连接线程启动信号
    connect(thread.get(),&QThread::started, producer, &Producer::produceWork);
    //连接线程结束信号, 这里为了延长thread声明周期
    connect(thread.get(), &QThread::finished, this, [=]() {
            thread->wait();
        });


    //连接停止信号，注意下面的方式是错误的
    //因为producer线程任务produceWork死循环，导致无法响应其他信号
    //connect(this, &MainWindow::sig_stop_produce, producer, &Producer::stopWork);
    //改为在MainWindow发送线程触发调用，内部再调用stopWork，此时是在MainWindow所属线程触发
    connect(this, &MainWindow::sig_stop_produce,this,[producer](int id){
        producer->stopWork(id);
    });

    //连接刷新信息信号
    connect(producer,&Producer::sig_up_text,this, &MainWindow::slot_up_text);

    //连接任务退出信号,因为线程执行的是死循环任务，所以接收者不能是thread
    //而且接收者不能是mainwindow，此时mainwindow如果处于退出等待状态也会卡死
    connect(producer,&Producer::sig_finished, [=](int id){
        qDebug()<<QString("收到任务[%1]退出信号").arg(id);
        producer->deleteLater();
        thread->quit();
    });

    //线程放入容器管理
    _producer_ids.push_back(_worker_id);
    //生产者map
    _map_producer_thread.insert(_worker_id,thread);
    //生产者放入map
    _map_producers.insert(_worker_id,producer);

    //更新生产者数量
    ui->producerLb->setText(QString("%1").arg(_producer_ids.size()));

    //更新提示信息
    ui->textEdit->append(QString("创建生产者线程：[%1]").arg(_worker_id));

    thread->start();
}

void MainWindow::on_delProducerBtn_clicked()
{
    if(_producer_ids.isEmpty()){
        QMessageBox::information(nullptr, "提示信息","没有生产者线程运行");
        return;
    }
    //获取首部元素
    auto id = _producer_ids.front();
    //弹出
    _producer_ids.pop_front();
    //从map中移除thread
    _map_producer_thread.remove(id);
    //从map中移除生产者
    _map_producers.remove(id);
    //发送信号停止
    emit sig_stop_produce(id);

    //更新生产者数量
    ui->producerLb->setText(QString("%1").arg(_producer_ids.size()));
    //更新文本信息
    ui->textEdit->append(QString("销毁生产者线程[%1]").arg(id));
}

void MainWindow::slot_up_text(int id, int num, bool full)
{
    if (full) {
        this->ui->textEdit->append(QString("队列已满！！！ 线程：[%1] 无法将数据[%2]放入队列").arg(id).arg(num));
    }
    else {
        this->ui->textEdit->append(QString("线程：[%1] 将数据[%2]放入队列").arg(id).arg(num));
    }

}

void MainWindow::slot_consume_text(int id, int num, bool b_empty)
{
    if (b_empty) {
        this->ui->textEdit->append(QString("队列为空！！！ 线程：[%1] 无法取出数据").arg(id));
    }
    else {
        this->ui->textEdit->append(QString("线程：[%1] 将数据[%2]取出队列").arg(id).arg(num));
    }
}

void MainWindow::on_addConsumerBtn_clicked()
{
    //创建线程
    auto thread = std::make_shared<QThread>();
    //增加id
    _worker_id++;
    //创建生产者
    auto consumer = new Consumer(_worker_id);
    //放入线程
    consumer->moveToThread(thread.get());
    //连接线程启动信号
    connect(thread.get(),&QThread::started, consumer, &Consumer::consumeWork);
    //连接线程结束信号, 这里为了延长thread声明周期
    connect(thread.get(), &QThread::finished, this, [=]() {
            thread->wait();
        });


    //连接停止信号，注意下面的方式是错误的
    //因为producer线程任务produceWork死循环，导致无法响应其他信号
    //connect(this, &MainWindow::sig_stop_produce, producer, &Producer::stopWork);
    //改为在MainWindow发送线程触发调用，内部再调用stopWork，此时是在MainWindow所属线程触发
    connect(this, &MainWindow::sig_stop_consumer,this,[consumer](int id){
        consumer->stopWork(id);
    });

    //连接刷新信息信号
    connect(consumer,&Consumer::sig_consume_up,this, &MainWindow::slot_consume_text);

    //连接任务退出信号,因为线程执行的是死循环任务，所以接收者不能是thread
    //而且接收者不能是mainwindow，此时mainwindow如果处于退出等待状态也会卡死
    connect(consumer,&Consumer::sig_finished, [=](int id){
        qDebug()<<QString("收到任务[%1]退出信号").arg(id);
        consumer->deleteLater();
        thread->quit();
    });

    //线程放入容器管理
    _consumer_ids.push_back(_worker_id);
    //生产者map
    _map_consumer_thread.insert(_worker_id,thread);
    //生产者放入map
    _map_consumers.insert(_worker_id,consumer);

    //更新生产者数量
    ui->consumerLb->setText(QString("%1").arg(_consumer_ids.size()));

    //更新提示信息
    ui->textEdit->append(QString("创建消费者线程：[%1]").arg(_worker_id));

    thread->start();
}

void MainWindow::on_delConsumerBtn_clicked()
{
    if(_consumer_ids.isEmpty()){
        QMessageBox::information(nullptr, "提示信息","没有生产者线程运行");
        return;
    }
    //获取首部元素
    auto id = _consumer_ids.front();
    //弹出
    _consumer_ids.pop_front();
    //从map中移除thread
    _map_consumer_thread.remove(id);
    //从map中移除生产者
    _map_consumers.remove(id);
    //发送信号停止
    emit sig_stop_consumer(id);

    //更新生产者数量
    ui->consumerLb->setText(QString("%1").arg(_consumer_ids.size()));
    //更新文本信息
    ui->textEdit->append(QString("销毁消费者线程[%1]").arg(id));
}

```

**主函数启动**

主函数启动展示MainWindow

``` cpp
#include "mainwindow.h"
#include <QApplication>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    w.show();

    return a.exec();
}
```





**多生产者多消费者(课外拓展)**



我们采用的方法就是QWaitCondition, 我们可以制作如下界面，通过增减生产者，消费者达到控制速度的目的，当队列达到200时我们认为队列已满，当队列为空时我们认为不能消费。

![https://cdn.llfc.club/1728204450082.jpg](https://cdn.llfc.club/1728204450082.jpg)



**解决思路**

创建项目ProducerConsumer, 编辑mainwindow.ui，ui界面如下

![https://cdn.llfc.club/1727658656924.jpg](https://cdn.llfc.club/1727658656924.jpg)

属性结构图

![https://cdn.llfc.club/1727658729994.jpg](https://cdn.llfc.club/1727658729994.jpg)

**全局文件**

我们创建一个全局文件global.h和global.cpp，在global.h中声明如下全局变量

``` cpp
#ifndef GLOBAL_H
#define GLOBAL_H
#include <QQueue>
#include <atomic>
#include <QMutex>
#include <QWaitCondition>
#include <QSet>


//全局队列，生产者和消费者共享
extern QQueue<int> _global_queue;
//生产者共享的计数
extern std::atomic<int> _global_num;
//互斥量，生产者和消费者共享
extern QMutex _global_mtx;
//生产者条件变量
extern QWaitCondition _global_producer_wc;
//消费者条件变量
extern QWaitCondition _global_consumer_wc;
//队列最大值
const int MAX_SIZE = 10;


extern void printQtThreadId(QString str);
#endif // GLOBAL_H
```

定义如下全局变量

``` cpp
#include "global.h"
#include <QThread>
#include <QDebug>

//全局队列，生产者和消费者共享
QQueue<int> _global_queue = {};
//生产者共享的计数
std::atomic<int> _global_num = {0};
//互斥量，生产者和消费者共享
QMutex _global_mtx;
//生产者条件变量
QWaitCondition _global_producer_wc;
//消费者条件变量
QWaitCondition _global_consumer_wc;

void printQtThreadId(QString str)
{
    qDebug() << str;
    Qt::HANDLE tid = QThread::currentThreadId();

    // 将 Qt::HANDLE 转换为 uintptr_t（无符号整数类型）
    quintptr numericTid = reinterpret_cast<quintptr>(tid);

    // 使用十六进制格式打印更具辨识度
    qDebug() << "Qt Thread ID:" << QString("0x%1").arg(numericTid, 0, 16);
    qDebug() << str;
}
```

**生产者任务类**

``` cpp
#ifndef PRODUCER_H
#define PRODUCER_H

#include <QObject>

class Producer : public QObject
{
    Q_OBJECT
public:
    //id为生产者id
    explicit Producer(int id, QObject *parent = nullptr);
    ~Producer();

public slots:
    //槽函数响应线程启动信号，模拟生产工作
    void produceWork();
    //槽函数响应主界面停止信号，结束任务
    void stopWork(int id);
private:
    //是否运行
   std::atomic<bool> _b_run;
    //生产者id
    int _id;
signals:
    //任务完成信号
    void sig_finished(int id);
    //发送信号通知主界面显示
    void sig_up_text(int id, int num, bool full = false);

};

#endif // PRODUCER_H

```

具体实现

``` cpp
#include "producer.h"
#include "global.h"
#include <QThread>
#include <QDebug>

Producer::Producer(int id, QObject *parent): QObject(parent),_id(id)
{

}

void Producer::produceWork()
{
    _b_run = true;
    bool flag = false;
    while(_b_run){
        //判断队列是否满了,需要先加锁
        _global_mtx.lock();
         _global_num++;
         auto temp = _global_num.load();
        //队列满了，需要用while循环判断，防止虚假唤醒
        while(_global_queue.size()>=MAX_SIZE && _b_run ){
            //通知主界面生产者满了
            emit  sig_up_text(_id, temp, true);
            //生产者线程被挂起，直到消费者线程唤醒它
            _global_producer_wc.wait(&_global_mtx);
        }

        //队列未满，或者被消费者唤醒，或者是主界面退出唤醒
        // 二次判断是否因为主界面退出唤醒
        if(!_b_run){
            //解锁
            _global_mtx.unlock();
            //发送结束信号
            emit sig_finished(_id);
            return;
        }


        _global_queue.push_back(temp);
        //发送信号通知主界面刷新信息
        emit sig_up_text(_id, temp);

        flag = false;

        if(_global_queue.size() == 1){
            flag = true;
        }
        //解锁
        _global_mtx.unlock();

        //通知消费者唤醒
        if(flag){
           _global_consumer_wc.notify_one();
        }

        //为防止循环过快，小睡一会
        QThread::msleep(500);
    }

    //发送结束信号
    emit sig_finished(_id);
    return;
}

Producer::~Producer()
{
    qDebug() << QString(" producer [%1] destruct").arg(_id);
}

void Producer::stopWork(int id)
{
    //界面停止信号会连接多个生产者，需要判断id是否为自己
    if(_id != id){
        return;
    }

    _global_mtx.lock();
    //是自己则退出
    _b_run = false;
    _global_producer_wc.notify_all();
    _global_mtx.unlock();
}
```

**消费者任务类**

创建Consumer类声明如下

``` cpp
#ifndef CONSUMER_H
#define CONSUMER_H

#include <QObject>

class Consumer : public QObject
{
    Q_OBJECT
public:
    explicit Consumer(int id, QObject *parent = nullptr);
    ~Consumer();
signals:
    //更新主界面的信号
    void sig_consume_up(int con_id, int num, bool b_empty = false);
    //任务完成信号
    void sig_finished(int id);
public slots:
    //开始消费任务函数
    void consumeWork();
    //停止执行消费任务
    void stopWork(int id);
private:
    int _id;
    bool _b_run;
};

#endif // CONSUMER_H

```

定义如下

``` cpp
#include "consumer.h"
#include "global.h"
#include <QThread>
#include <QDebug>

Consumer::Consumer(int id, QObject *parent) : QObject(parent),_id(id),_b_run(false)
{

}

Consumer::~Consumer()
{
    qDebug() << QString(" consumer [%1] destruct").arg(_id);
}

void Consumer::consumeWork()
{
    _b_run = true;
    bool flag = false;
    while(_b_run){
        //判断队列是否满了,需要先加锁
        _global_mtx.lock();
        //队列满了，需要用while循环判断，防止虚假唤醒
        while(_global_queue.size() <= 0 && _b_run){
            //通知主界面消费者队列为空
            emit  sig_consume_up(_id, 0, true);
            //生产者线程被挂起，直到消费者线程唤醒它
            _global_consumer_wc.wait(&_global_mtx);
        }

        //队列未满，或者被消费者唤醒，或者是主界面退出唤醒
        // 二次判断是否因为主界面退出唤醒
        if(!_b_run){
            //解锁
            _global_mtx.unlock();
            //发送结束信号
            emit sig_finished(_id);
            return;
        }

        auto temp = _global_queue.front();
        _global_queue.pop_front();
        //发送信号通知主界面刷新信息
        emit sig_consume_up(_id, temp);

        flag = false;
        if(_global_queue.size() == MAX_SIZE-1){
            flag = true;
        }
        //解锁
        _global_mtx.unlock();

        //发送通知唤醒生产者
        if(flag){
            _global_producer_wc.notify_one();
        }

        //为防止循环过快，小睡一会
        QThread::msleep(500);
    }

    //发送结束信号
    emit sig_finished(_id);
    return;
}

void Consumer::stopWork(int id)
{
    //界面停止信号会连接多个消费者，需要判断id是否为自己
    if(_id != id){
        return;
    }

    _global_mtx.lock();
    //是自己则退出
    _b_run = false;
    _global_consumer_wc.notify_all();
    _global_mtx.unlock();
}
```

**实现mainwindow**

声明如下

``` cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>
#include <QVector>
#include <QMap>
#include "producer.h"
#include <memory>
#include "consumer.h"

namespace Ui {
class MainWindow;
}

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    //点击添加生产者线程按钮响应的槽函数
    void on_addProducerBtn_clicked();
    //点击删除生产者线程按钮响应的槽函数
    void on_delProducerBtn_clicked();
    //响应生产者线程发过来的消息显示到界面上
    void slot_up_text(int id, int num, bool full);
    //响应消费者线程发过来的消息显示到界面上
    void slot_consume_text(int id, int num, bool b_empty);
    //响应添加消费者线程按钮的槽函数
    void on_addConsumerBtn_clicked();
    //响应删除消费者线程按钮的槽函数
    void on_delConsumerBtn_clicked();

private:
    Ui::MainWindow *ui;
    //工人id，生产者和消费者id
    int _worker_id;
    //生产者id列表
    QVector<int> _producer_ids;
    //消费者id列表
    QVector<int> _consumer_ids;

    //生产者id对应线程的map
    QMap<int, std::shared_ptr<QThread> > _map_producer_thread;
    //生产者id对应生产者数据
    QMap<int, Producer*> _map_producers;

    //消费者id对应线程的map
    QMap<int, std::shared_ptr<QThread> > _map_consumer_thread;
    //消费者id对应生产者数据
    QMap<int, Consumer*> _map_consumers;

signals:
    //停止某个生产者信号
    void sig_stop_produce(int id);
    //停止某个消费者信号
    void sig_stop_consumer(int id);
};

#endif // MAINWINDOW_H

```

完成具体实现

``` cpp
#include "mainwindow.h"
#include "ui_mainwindow.h"
#include <QThread>
#include "global.h"
#include "producer.h"
#include <QMessageBox>
#include <QDebug>
#include "consumer.h"

MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow),_worker_id(0)
{
    ui->setupUi(this);
}

MainWindow::~MainWindow()
{
    //通知生产者结束工作
    for(auto iter = _map_producers.begin();
        iter != _map_producers.end(); iter++){
        iter.value()->stopWork(iter.key());
    }

    //等待线程退出
    for(auto& thread: _map_producer_thread){
        thread->wait();
    }

    //通知消费者结束工作
    for(auto iter = _map_consumers.begin();
        iter != _map_consumers.end(); iter++){
        iter.value()->stopWork(iter.key());
    }

    //等待线程退出
    for(auto& thread: _map_consumer_thread){
        thread->wait();
    }


    delete ui;
}

void MainWindow::on_addProducerBtn_clicked()
{
    //创建线程
    auto thread = std::make_shared<QThread>();
    //增加id
    _worker_id++;
    //创建生产者
    auto producer = new Producer(_worker_id);
    //放入线程
    producer->moveToThread(thread.get());
    //连接线程启动信号
    connect(thread.get(),&QThread::started, producer, &Producer::produceWork);
    //连接线程结束信号, 这里为了延长thread声明周期
    connect(thread.get(), &QThread::finished, this, [=]() {
            thread->wait();
        });


    //连接停止信号，注意下面的方式是错误的
    //因为producer线程任务produceWork死循环，导致无法响应其他信号
    //connect(this, &MainWindow::sig_stop_produce, producer, &Producer::stopWork);
    //改为在MainWindow发送线程触发调用，内部再调用stopWork，此时是在MainWindow所属线程触发
    connect(this, &MainWindow::sig_stop_produce,this,[producer](int id){
        producer->stopWork(id);
    });

    //连接刷新信息信号
    connect(producer,&Producer::sig_up_text,this, &MainWindow::slot_up_text);

    //连接任务退出信号,因为线程执行的是死循环任务，所以接收者不能是thread
    //而且接收者不能是mainwindow，此时mainwindow如果处于退出等待状态也会卡死
    connect(producer,&Producer::sig_finished, [=](int id){
        qDebug()<<QString("收到任务[%1]退出信号").arg(id);
        producer->deleteLater();
        thread->quit();
    });

    //线程放入容器管理
    _producer_ids.push_back(_worker_id);
    //生产者map
    _map_producer_thread.insert(_worker_id,thread);
    //生产者放入map
    _map_producers.insert(_worker_id,producer);

    //更新生产者数量
    ui->producerLb->setText(QString("%1").arg(_producer_ids.size()));

    //更新提示信息
    ui->textEdit->append(QString("创建生产者线程：[%1]").arg(_worker_id));

    thread->start();
}

void MainWindow::on_delProducerBtn_clicked()
{
    if(_producer_ids.isEmpty()){
        QMessageBox::information(nullptr, "提示信息","没有生产者线程运行");
        return;
    }
    //获取首部元素
    auto id = _producer_ids.front();
    //弹出
    _producer_ids.pop_front();
    //从map中移除thread
    _map_producer_thread.remove(id);
    //从map中移除生产者
    _map_producers.remove(id);
    //发送信号停止
    emit sig_stop_produce(id);

    //更新生产者数量
    ui->producerLb->setText(QString("%1").arg(_producer_ids.size()));
    //更新文本信息
    ui->textEdit->append(QString("销毁生产者线程[%1]").arg(id));
}

void MainWindow::slot_up_text(int id, int num, bool full)
{
    if (full) {
        this->ui->textEdit->append(QString("队列已满！！！ 线程：[%1] 无法将数据[%2]放入队列").arg(id).arg(num));
    }
    else {
        this->ui->textEdit->append(QString("线程：[%1] 将数据[%2]放入队列").arg(id).arg(num));
    }

}

void MainWindow::slot_consume_text(int id, int num, bool b_empty)
{
    if (b_empty) {
        this->ui->textEdit->append(QString("队列为空！！！ 线程：[%1] 无法取出数据").arg(id));
    }
    else {
        this->ui->textEdit->append(QString("线程：[%1] 将数据[%2]取出队列").arg(id).arg(num));
    }
}

void MainWindow::on_addConsumerBtn_clicked()
{
    //创建线程
    auto thread = std::make_shared<QThread>();
    //增加id
    _worker_id++;
    //创建生产者
    auto consumer = new Consumer(_worker_id);
    //放入线程
    consumer->moveToThread(thread.get());
    //连接线程启动信号
    connect(thread.get(),&QThread::started, consumer, &Consumer::consumeWork);
    //连接线程结束信号, 这里为了延长thread声明周期
    connect(thread.get(), &QThread::finished, this, [=]() {
            thread->wait();
        });


    //连接停止信号，注意下面的方式是错误的
    //因为producer线程任务produceWork死循环，导致无法响应其他信号
    //connect(this, &MainWindow::sig_stop_produce, producer, &Producer::stopWork);
    //改为在MainWindow发送线程触发调用，内部再调用stopWork，此时是在MainWindow所属线程触发
    connect(this, &MainWindow::sig_stop_consumer,this,[consumer](int id){
        consumer->stopWork(id);
    });

    //连接刷新信息信号
    connect(consumer,&Consumer::sig_consume_up,this, &MainWindow::slot_consume_text);

    //连接任务退出信号,因为线程执行的是死循环任务，所以接收者不能是thread
    //而且接收者不能是mainwindow，此时mainwindow如果处于退出等待状态也会卡死
    connect(consumer,&Consumer::sig_finished, [=](int id){
        qDebug()<<QString("收到任务[%1]退出信号").arg(id);
        consumer->deleteLater();
        thread->quit();
    });

    //线程放入容器管理
    _consumer_ids.push_back(_worker_id);
    //生产者map
    _map_consumer_thread.insert(_worker_id,thread);
    //生产者放入map
    _map_consumers.insert(_worker_id,consumer);

    //更新生产者数量
    ui->consumerLb->setText(QString("%1").arg(_consumer_ids.size()));

    //更新提示信息
    ui->textEdit->append(QString("创建消费者线程：[%1]").arg(_worker_id));

    thread->start();
}

void MainWindow::on_delConsumerBtn_clicked()
{
    if(_consumer_ids.isEmpty()){
        QMessageBox::information(nullptr, "提示信息","没有生产者线程运行");
        return;
    }
    //获取首部元素
    auto id = _consumer_ids.front();
    //弹出
    _consumer_ids.pop_front();
    //从map中移除thread
    _map_consumer_thread.remove(id);
    //从map中移除生产者
    _map_consumers.remove(id);
    //发送信号停止
    emit sig_stop_consumer(id);

    //更新生产者数量
    ui->consumerLb->setText(QString("%1").arg(_consumer_ids.size()));
    //更新文本信息
    ui->textEdit->append(QString("销毁消费者线程[%1]").arg(id));
}

```

**启动界面**

主函数中启动界面展示

``` cpp
#include "mainwindow.h"
#include <QApplication>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    w.show();

    return a.exec();
}

```





# 第十一章 网络编程



Qt的网络模块主要集中在`QtNetwork`模块中，提供了对TCP/IP、UDP、HTTP等多种网络协议的支持。通过这些类，开发者可以轻松实现客户端、服务器端的通信，处理网络数据传输，进行HTTP请求等操作。



注意QT 网络需要在pro中包含network库

``` cpp
QT += network
```



## **TCP 协议简介**



TCP（Transmission Control Protocol）是一种面向连接、可靠、基于字节流的传输层协议。它确保数据包按顺序到达并进行错误检查。

### **三次握手**

为了保证客户端和服务器端的可靠连接，TCP建立连接时必须要进行三次会话，也叫TCP三次握手，进行三次握手的目的是为了确认双方的接收能力和发送能力是否正常。

举个栗子
班主任 和 王同学打电话

班主任：你好！小王同学，听得到吗？（一次会话）
王同学：听到了，老师，你能听到吗 （二次会话）
班主任：听到了，你过来上课吧  （三次会话）

通过这个例子我们可以知道三次会话的目的就是为了确保双方的连接正常，同理，TCP三次握手也是这个过程，下面用图文形式来解释一下TCP三次握手。

**TCP建立连接过程**

![https://cdn.llfc.club/1728522160481.jpg](https://cdn.llfc.club/1728522160481.jpg)



最开始的时候客户端和服务器都是处于CLOSED关闭状态。主动打开连接的为客户端，被动打开连接的是服务器。

TCP服务器进程先创建传输控制块TCB，时刻准备接受客户进程的连接请求，此时服务器就进入了 LISTEN 监听状态

第一次握手 TCP客户进程也是先创建传输控制块TCB，然后向服务器发出连接请求报文，这是报文首部中的同部位SYN=1，同时选择一个初始序列号 seq=x ，此时，TCP客户端进程进入了 SYN-SENT 同步已发送状态

第二次握手 TCP服务器收到请求报文后，如果同意连接，则会向客户端发出确认报文。确认报文中应该 ACK=1，SYN=1，确认号是ack=x+1，同时也要为自己初始化一个序列号 seq=y，此时，TCP服务器进程进入了 SYN-RCVD 同步收到状态

第三次握手 TCP客户端收到确认后，还要向服务器给出确认。确认报文的ACK=1，ack=y+1，自己的序列号seq=x+1，此时，TCP连接建立，客户端进入ESTABLISHED已建立连接状态 触发三次握手

有人可能会很疑惑为什么要进行第三次握手？
主要原因：防止已经失效的连接请求报文突然又传送到了服务器，从而产生错误



### **TCP四次挥手**

建立TCP连接需要三次握手，终止TCP连接需要四次挥手

举个例子
张三和李四的对话

张三：好的，那我先走了
李四：好的，那你走吧
李四：那我也走了？
张三：好的，你走吧

![https://cdn.llfc.club/1728532876959.jpg](https://cdn.llfc.club/1728532876959.jpg)



数据传输完毕后，双方都可释放连接。最开始的时候，客户端和服务器都是处于ESTABLISHED状态，然后客户端主动关闭，服务器被动关闭。

第一次挥手 客户端发出连接释放报文，并且停止发送数据。释放数据报文首部，FIN=1，其序列号为seq=u（等于前面已经传送过来的数据的最后一个字节的序号加1），此时，客户端进入FIN-WAIT-1（终止等待1）状态

第二次挥手 服务器端接收到连接释放报文后，发出确认报文，ACK=1，ack=u+1，并且带上自己的序列号seq=v，此时，服务端就进入了CLOSE-WAIT 关闭等待状态

第三次挥手 客户端接收到服务器端的确认请求后，客户端就会进入FIN-WAIT-2（终止等待2）状态，等待服务器发送连接释放报文，服务器将最后的数据发送完毕后，就向客户端发送连接释放报文，服务器就进入了LAST-ACK（最后确认）状态，等待客户端的确认。

第四次挥手 客户端收到服务器的连接释放报文后，必须发出确认，ACK=1，ack=w+1，而自己的序列号是seq=u+1，此时，客户端就进入了TIME-WAIT（时间等待）状态，但此时TCP连接还未终止，必须要经过2MSL后（最长报文寿命），当客户端撤销相应的TCB后，客户端才会进入CLOSED关闭状态，服务器端接收到确认报文后，会立即进入CLOSED关闭状态，到这里TCP连接就断开了，四次挥手完成



**TIME_WAIT状态的作用**



在第四次挥手中，主动关闭的一方（通常是客户端）进入**TIME_WAIT**状态。这一状态的存在有两个主要目的：

1. **确保最后的ACK包能够被对方接收**：如果最后的ACK包由于网络问题丢失，**TIME_WAIT**状态允许主动关闭方在等待期间重传ACK包，确保被动方能够收到并正确关闭连接。

- 如果被动关闭方没有收到ACK包（因为ACK在传输过程中丢失），它会重新发送FIN包。
- 主动关闭方在TIME_WAIT状态下监听到这个重新发送的FIN包后，会重新发送ACK包，确保被动关闭方最终收到了确认。



1. **防止旧的重复数据包干扰新的连接**：感谢有限的端口资源和序列号重复使用，通过**TIME_WAIT**状态，确保网络上旧的包完全消失，避免干扰未来使用相同端口和序列号的新连接。



**为什么需要四次挥手**



**确保双向关闭**

由于TCP是全双工的，双方需要分别确认发送和接收的结束。如果只使用两次挥手（类似于建立连接的三次握手），可能无法确保双方都已完成数据传输，并且确认了对方的关闭请求。

**防止数据丢失**

在连接终止过程中，网络延迟、丢包等问题可能导致某些包丢失。通过四次挥手，每一步的确认确保双方都已经安全地收到了对方的关闭请求，避免数据丢失或连接状态不一致。

**保证资源释放**

四次挥手确保双方都完成了收尾工作，包括缓冲区中的数据已全部发送和接收，资源能够被正确释放。如果过早关闭连接，可能会导致数据丢失或资源泄漏。





**编码流程**

客户端和服务器通信，客户端需要执行的流程包括如下：

1 客户端创建`QTcpSocket`对象，调用connect连接到服务器。

2  获取连接状态，如果连接失败则提示或重连

3  读写收发数据



服务器的通信流程包括：

1  服务器创建`QTcpServer`对象

2  调用`listen`方法监听新的连接

3  通过捕获`newConnection`信号编写处理新连接的槽函数。或者重写`incomingConnection`槽函数处理新连接

4  基于新连接返回的QTcpSocket对象，连接读信号，并实现读处理的槽函数即可。

5  基于新连接返回的QTcpSocket对象，连接断开信号，并实现断开连接处理的槽函数。



使用TCP需要包含必要头文件

``` cpp
#include <QTcpSocket>
#include <QTcpServer>
#include <QHostAddress>
```



## **QTcpSocket 类**



`QTcpSocket` 是 Qt 提供的用于TCP客户端通信的类。主要功能包括：



- 连接到服务器（`connectToHost`）
- 读取与写入数据（`read`, `write`）
- 处理连接状态（`connected`, `disconnected` 等信号）



**常用信号：**



- `connected()`: 成功连接到服务器时发出。
- `disconnected()`: 断开连接时发出。
- `readyRead()`: 有新数据可读时发出。
- `errorOccurred(QAbstractSocket::SocketError)`: 出现错误时发出。



## **QTcpServer 类**



`QTcpServer` 是 Qt 提供的用于TCP服务器管理的类。主要功能包括：



- 监听端口（`listen`）
- 等待客户端连接（`newConnection` 信号）
- 管理多个客户端连接



**常用方法：**



- `listen(QHostAddress, quint16)`: 开始监听指定地址和端口。
- `nextPendingConnection()`: 获取下一个等待连接的`QTcpSocket`对象。



## **信号与槽机制在 TCP 编程中的应用**



Qt 的信号与槽机制是实现异步通信的关键。通过连接不同对象的信号与槽，可以在事件发生时自动触发相应的处理函数。例如，当服务器接收到新连接时，`QTcpServer` 会发出 `newConnection` 信号，连接到这个信号的槽函数可以处理新连接。

我们可以通过捕获newConnection信号，在槽函数中处理连接请求，但是这种方式

**优点：**



- **简洁易用**：通过信号和槽机制，代码结构清晰，易于理解和维护。
- **不需要继承**：不需要创建服务器类的子类，适合简单和中等复杂度的应用。



**缺点：**



- **灵活性有限**：对于需要更细粒度控制新连接处理过程的应用，可能不够灵活。



也可以通过重写**incomingConnection**处理新来的连接，这种方式和上面类似，但是更加灵活，还可以将新的连接分配到其他线程。

## 聊天室实战案例

我们实现一个客户端群聊功能，当然要实现客户端和服务器通信，服务器负责将消息转发给所有在线的客户端，客户端收到消息后显示。

服务器显示客户端发送的信息列表

![https://cdn.llfc.club/1728369582865.jpg](https://cdn.llfc.club/1728369582865.jpg)

客户端显示如下

![https://cdn.llfc.club/1728369774863.jpg](https://cdn.llfc.club/1728369774863.jpg)



**实现过程**

客户端界面如下图

![https://cdn.llfc.club/1728287524123.jpg](https://cdn.llfc.club/1728287524123.jpg)

**ui布局**

![https://cdn.llfc.club/1728287654217.jpg](https://cdn.llfc.club/1728287654217.jpg)

属性布局如下

![https://cdn.llfc.club/1728287695623.jpg](https://cdn.llfc.club/1728287695623.jpg)

**MainWindow**

做网络之前，我们先实现基本的发送响应逻辑, 最初的MainWindow声明如下

``` cpp
class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    //点击发送按钮
    void on_send_btn_clicked();
    //收到消息槽函数，添加消息到聊天框
    void slot_append_msg(QString msg);
private:
    Ui::MainWindow *ui;
signals:
};
```

构造函数实现

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    this->resize(800,600);
    //设置默认ip
    ui->address_ed->setText("127.0.0.1");
    //设置spinbox范围
    ui->port_spin->setMaximum(20000);
    //设置端口号
    ui->port_spin->setValue(10086);

    //设置textEdit文字大小
    QFont font = ui->chatEdit->font();
    font.setPointSize(16);
    ui->chatEdit->setFont(font);
    //设置textEdit只读
    ui->chatEdit->setReadOnly(true);

    //设置默认名字
    ui->name_ed->setText("疾跑流鲁班");

}
```

当发送消息的按钮被点击时执行如下槽函数

``` cpp
//发送消息按钮点击后槽函数响应如下
void MainWindow::on_send_btn_clicked()
{
    QString name = ui->name_ed->text();
    QString msg = ui->msg_ed->text();
    if(msg.isEmpty()){
        return;
    }

    if(name.isEmpty()){
        QMessageBox::information(nullptr,"提示信息","用户名为空！");
        return;
    }

    QString msgs = QString("%1 : %2").arg(name).arg(msg);
    //发送消息,todo发送TCPClient信号...
    //emit TcpClient::Inst().sig_send_msg(msgs);
    //清空编辑框
    ui->msg_ed->clear();
}
```

收到发送消息的信号后，将消息添加到聊天框

``` cpp
//添加消息
void MainWindow::slot_append_msg(QString msg)
{
    ui->chatEdit->append(msg);
}
```

**TcpClient类**

接下来我们需要实现TCPClient类，关于网络类，我们在企业中一般以单例模式使用.

为了编写边测试，我们先声明TcpClient类，因为是单例类，所以要去掉拷贝构造和拷贝赋值，并且将构造函数设为私有。

``` cpp
#ifndef TCPCLIENT_H
#define TCPCLIENT_H

#include <QObject>
#include <QTcpSocket>

class TcpClient : public QObject
{
    Q_OBJECT
public:
    //单例模式，返回静态局部变量
    static TcpClient& Inst(){
        static TcpClient client;
        return client;
    }
    ~TcpClient();

    //删除拷贝构造和拷贝赋值
    TcpClient(const TcpClient&) = delete;
    TcpClient& operator=(const TcpClient&) = delete;
    
    //连接到服务器
    void connectToServer(const QString& host, quint16 port);
private:
    //构造函数变为私有
    explicit TcpClient(QObject *parent = nullptr);

    //QTcpSocket类，用来通信的客户端
    QTcpSocket* _socket;

signals:

public slots:

    //连接成功触发的槽函数
    void slot_connected();
    //tcp缓冲区有数据可读，触发读取消息槽函数
    void slot_ready_read();
    //捕获到断开连接触发的槽函数
    void slot_disconnected();
    //捕获到出错信号触发的槽函数
    void slot_error_occured(QAbstractSocket::SocketError socketError);

    //发送消息槽函数
    void slot_send_msg(const QString& msg);

};

#endif // TCPCLIENT_H

```

在TcpClient的构造函数中添加信号和槽函数的连接处理

``` cpp
TcpClient::TcpClient(QObject *parent) : QObject(parent), _socket(new QTcpSocket(this))
{
    //连接 连接成功信号和槽函数
    connect(_socket, &QTcpSocket::connected, this, &TcpClient::slot_connected);
    //连接 读数据信号和槽函数
    connect(_socket, &QTcpSocket::readyRead, this, &TcpClient::slot_ready_read);
    //连接 断开连接信号和槽函数
    connect(_socket, &QTcpSocket::disconnected, this, &TcpClient::slot_disconnected);
    //连接 出错信号和槽函数
    connect(_socket, QOverload<QAbstractSocket::SocketError>::of(&QTcpSocket::error),
                    this, &TcpClient::slot_error_occured);
    //5.15之后的高版本才有的信号
//    connect(_socket, QOverload<QAbstractSocket::SocketError>::of(&QTcpSocket::errorOccurred),
//                this, &TcpClient::slot_error_occured);
}
```

**注意事项**

- _socket初始化通过new的方式创建指针，指定父窗口为TcpClient
- errorOccurred信号是高于5.15版本才有的信号，我们使用的是低版本，所以使用error信号。

- `QOverload` 是一个模板类，用于解决重载信号的问题。因为 Qt 中可能会有多个同名的信号（例如，`error(QAbstractSocket::SocketError)` 和 `error(QString)`），使用 `QOverload` 可以明确指定我们要连接的信号的版本。

其等价于下面的写法,

``` cpp
//连接 出错信号和槽函数
connect(_socket, static_cast<void(QTcpSocket::*)(QTcpSocket::SocketError)>(&QTcpSocket::error),
                this, &TcpClient::slot_error_occured);
```

 通过static_cast将QTcpSocket::error转化为一个成员函数的指针，这样可以指定参数类型。

我们将其他的成员函数和方法先实现，不写具体内容。

**连接服务器**

连接主界面连接服务器按钮的点击信号，调用连接功能

``` cpp
//点击连接到服务器后响应的槽函数
void MainWindow::on_conBtn_clicked()
{
    auto address = ui->address_ed->text();
    quint16 port = static_cast<quint16>(ui->port_spin->value());
    TcpClient::Inst().connectToServer(address, port);
}
```

实现connectToServer函数

``` cpp
void TcpClient::connectToServer(const QString &host, quint16 port)
{
    _socket->connectToHost(host, port);
}
```

**捕获连接信号**

我们可以为Client类设置用户名，这样发送消息可以携带用户名

新增成员变量_name，构造函数初始化为空字符串，并且提供设置名字的成员函数

``` cpp
void TcpClient::setName(const QString &msg)
{
     _name = msg;
}
```

在MainWindow构造函数中添加设置名字逻辑

``` cpp
//设置用户名
TcpClient::Inst().setName(ui->name_ed->text());
```

在MainWindow构造函数中捕获名字编辑框消失的信号，并且设置名字给客户端

``` cpp
//连接名字编辑框失去焦点信号
connect(ui->name_ed,&QLineEdit::editingFinished, this, [=](){
    //设置用户名
    TcpClient::Inst().setName(ui->name_ed->text());
});
```

回到TcpClient中, 封装成员函数发送消息，

``` cpp
void TcpClient::sendMsg(const QString &msg)
{
    //发送信号，统一交给槽函数处理，这么做的好处是多线程安全
    emit sig_send_msg(msg);
}
```

sendMsg中发送信号发消息，这么做的好处是多线程调用sendMsg不会有数据污染

所以TcpClient定义了sig_send_msg信号，以及槽函数slot_send_msg

``` cpp
void TcpClient::slot_send_msg(const QString &msg)
{
    //如果连接异常则直接返回
    if(_socket->state() != QAbstractSocket::ConnectedState){
        QMessageBox::information(nullptr,"提示消息","断开连接无法发送");
        return;
    }
    //发送消息
     _socket->write(msg.toUtf8()+"\n");
}
```

TcpClient中连接发送信号和槽函数

``` cpp
//连接 发送数据信号和槽函数
connect(this, &TcpClient::sig_send_msg, this, &TcpClient::slot_send_msg);
```

主窗口点击发送按钮后，需发送客户端的信号, 完善后的发送服务如下

``` cpp
void MainWindow::on_send_btn_clicked()
{
    QString name = ui->name_ed->text();
    QString msg = ui->msg_ed->text();
    if(msg.isEmpty()){
        return;
    }

    if(name.isEmpty()){
        QMessageBox::information(nullptr,"提示信息","用户名为空！");
        return;
    }

    QString msgs = QString("[%1] : %2").arg(name).arg(msg);
    //发送消息
    emit TcpClient::Inst().sig_send_msg(msgs);
    //清空编辑框
    ui->msg_ed->clear();
}
```

准备工作都做好了，接下来我们在连接成功的槽函数中发送信息给服务器

``` cpp
//连接成功槽函数
void TcpClient::slot_connected()
{
    QMessageBox::information(nullptr,"提示信息","连接服务器成功！");
    //发送消息
    this->sendMsg(QString("[%1] : %2").arg(_name).arg("登录成功"));
}
```

我们发送给服务器了，主界面也要显示一下自己的信息, 主界面也连接TcpClient的sig_send_msg信号

``` cpp
//连接发送消息信号
connect(&TcpClient::Inst(), &TcpClient::sig_send_msg, this, &MainWindow::slot_append_msg);
```

**捕获连接断开**

``` cpp
//捕获连接断开信号
void TcpClient::slot_disconnected()
{
    //连接断开
    QMessageBox::information(nullptr,"提示信息","连接断开！");
    this->sendMsg(QString("[%1] : %2").arg(_name).arg("连接断开"));
}
```

捕获错误信息

``` cpp
void TcpClient::slot_error_occured(QAbstractSocket::SocketError socketError)
{
    Q_UNUSED(socketError);
    //产生错误
    QMessageBox::information(nullptr,"提示信息",
                             QString("产生错误: %1 ！").arg(_socket->errorString()));
}
```

此时启动程序，点击连接服务器，过一段时间后会出现如下错误

![https://cdn.llfc.club/1728298583680.jpg](https://cdn.llfc.club/1728298583680.jpg)

为了防止用户点击了连接服务器后没来的及处理就再次点击，所以点击连接后将按钮置灰, 在产生错误时重置连接为可用。

MainWindow构造函数中

``` cpp
    //设置按钮状态
    ui->conBtn->setEnabled(true);
    ui->disConBtn->setEnabled(false);
```

点击后

``` cpp
//点击连接到服务器后响应的槽函数
void MainWindow::on_conBtn_clicked()
{
    //设置按钮状态
    ui->conBtn->setEnabled(false);
    auto address = ui->address_ed->text();
    quint16 port = static_cast<quint16>(ui->port_spin->value());
    TcpClient::Inst().connectToServer(address, port);
}
```

MainWindow增加槽函数响应是否重置按钮初始状态

``` cpp
//重置按钮状态
void MainWindow::slot_reset_btn(bool b_reset)
{
    ui->conBtn->setEnabled(b_reset);
    ui->disConBtn->setEnabled(!b_reset);
}
```

MainWindow构造函数中添加

``` cpp
//连接重置按钮信号
connect(&TcpClient::Inst(), &TcpClient::sig_reset_btn, this, &MainWindow::slot_reset_btn);
```

完善错误处理

``` cpp
void TcpClient::slot_error_occured(QAbstractSocket::SocketError socketError)
{
    Q_UNUSED(socketError);
    //产生错误
    QMessageBox::information(nullptr,"提示信息",
                             QString("产生错误: %1 ！").arg(_socket->errorString()));

    //出错则判断连接状态并重置
    if(_socket->state() != QAbstractSocket::ConnectedState){
        emit sig_reset_btn(true);
        return;
    }

    //出错就关闭连接
    _socket->close();
    emit sig_reset_btn(true);
}
```

完善连接成功处理

``` cpp
//连接成功槽函数
void TcpClient::slot_connected()
{
    QMessageBox::information(nullptr,"提示信息","连接服务器成功！");
    //重置按钮
    emit sig_reset_btn(false);
    //发送消息
    this->sendMsg(QString("[%1] : %2").arg(_name).arg("登录成功"));
}
```

读取对端发送的信息

``` cpp
//接受服务器发送的信息
void TcpClient::slot_ready_read()
{
    //读取所有数据
    QByteArray data = _socket->readAll();
    //将数据转化为字符串
    QString message = QString::fromUtf8(data).trimmed();
    //发送消息通知界面显示
    emit sig_append_msg(message);
}
```

读取消息后，为了将消息发送到主界面聊天框显示，所以定义了sig_append_msg信号。

在MainWindow中构造函数里连接这个信号

``` cpp
//连接客户端接受信息后显示的消息
connect(&TcpClient::Inst(),&TcpClient::sig_append_msg, this, &MainWindow::slot_append_msg);
```

接下来实现断开连接函数

``` cpp
//断开连接函数
void TcpClient::disconnectFromServer()
{
    if(_socket->state() != QAbstractSocket::ConnectedState){
        return;
    }

    _socket->disconnectFromHost(); // 优雅地关闭连接

    // 或者使用 socket->close(); 立即关闭连接
    if (_socket->waitForDisconnected(3000)) {
        //重置按钮状态
        emit sig_reset_btn(true);
    } else {
        QMessageBox::information(nullptr, "提示信息",
                                 QString("关闭错误%1").arg(_socket->errorString()));
    }
}
```

并且在MainWindow的点击关闭连接的槽函数中添加socket断开连接的逻辑

``` cpp
void MainWindow::on_disConBtn_clicked()
{
    //断开连接
    TcpClient::Inst().disconnectFromServer();
}
```

到此位置我们的客户端开发完成。

接下来我们做服务器

**服务器**

创建TcpServer项目，记得在pro中添加network

``` cpp
QT       += core gui network
```

添加**Tcpserver**类

构造函数实现如下：

``` cpp
#ifndef CHATSERVER_H
#define CHATSERVER_H

#include <QObject>
#include <QTcpServer>
#include <QTcpSocket>
#include <QSet>

class ChatServer : public QTcpServer
{
    Q_OBJECT
public:
    static ChatServer& Inst(){
        static ChatServer server;
        return server;
    }

    //开始服务器
    bool startServer(quint16 port);
    //删除拷贝构造和拷贝赋值
    ChatServer(const ChatServer& cs) = delete;
    ChatServer& operator=(const ChatServer& cs) = delete;
protected:
    //重写虚函数，实现新连接到来管理逻辑
    void incomingConnection(qintptr socketDescriptor) override;
signals:

public slots:
    //服务器读消息的槽函数
    void slot_ready_read();
    //获取客户端断开连接的槽函数
    void slot_disconnect();
private:
    //构造函数
    explicit ChatServer(QObject *parent = nullptr);
    //客户端连接的集合
    QSet<QTcpSocket*> clients;
    //广播消息
    void broadcastMessage(const QString &message, QTcpSocket* sender = nullptr);
};

#endif // CHATSERVER_H

```

构造函数

``` cpp
ChatServer::ChatServer(QObject *parent) : QTcpServer(parent)
{

}

```

实现启动服务的逻辑

``` cpp
//启动服务
bool ChatServer::startServer(quint16 port)
{
    if (!this->listen(QHostAddress::Any, port)) {
        QMessageBox::information(nullptr,"提示信息","服务器启动失败！");
        return false;
    } else {
        QMessageBox::information(nullptr,"提示信息","服务器启动成功！");
        return true;
    }
}
```

获取新的连接

``` cpp
//获取新来的连接
void ChatServer::incomingConnection(qintptr socketDescriptor)
{
    QTcpSocket* clientSocket = new QTcpSocket(this);
    if (!clientSocket->setSocketDescriptor(socketDescriptor)) {
        qDebug() << "Failed to set socket descriptor";
        clientSocket->deleteLater();
        return;
    }

    //将客户端加入集合
    clients.insert(clientSocket);

    //连接读取信息信号
    connect(clientSocket, &QTcpSocket::readyRead, this, &ChatServer::slot_ready_read);
    //连接客户端断开信号
    connect(clientSocket, &QTcpSocket::disconnected, this, &ChatServer::slot_disconnect);

    //打印对端地址
    qDebug() << "New client connected:" << clientSocket->peerAddress().toString();
}
```

读取客户端发送信息

``` cpp
//读取客户端发送的数据
void ChatServer::slot_ready_read()
{
    //将发送信号的对象转化为QTcpSocket类型
    QTcpSocket* clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (!clientSocket)
        return;

    //读取信息
    QByteArray data = clientSocket->readAll();
    //去除信息前后空格
    QString message = QString::fromUtf8(data).trimmed();

    //广播消息
    broadcastMessage(message,clientSocket);

    qDebug() << "Received:" << message;
    //通知主界面添加消息
    emit sig_append_msg(message);
}
```

广播消息

``` cpp
//广播消息
void ChatServer::broadcastMessage(const QString &message, QTcpSocket* senderSocket)
{
    QByteArray data = message.toUtf8() + "\n";
    //遍历clients并且判断是否为发送者，如果不是源消息发送者则推送消息
    for(auto & client : clients){
        if(client != senderSocket){
            client->write(data);
        }
    }
}
```

处理客户端断开连接的消息

``` cpp
//获取客户端断开连接槽函数
void ChatServer::slot_disconnect()
{
    //获取发送者转为QTcpSocket类型
    QTcpSocket* clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (!clientSocket)
        return;

    //获取对端地址
    auto address = clientSocket->peerAddress().toString();
    //从客户端移除
    clients.remove(clientSocket);
    //删除socket
    clientSocket->deleteLater();
    //推广离开信息
    QString leftMessage = QString("%1 left the chat.").arg(address);
    broadcastMessage(leftMessage);
	//发送消息通知主界面显示离开信息
    emit sig_append_msg(leftMessage);
    qDebug() << "Client disconnected:" << address;
}
```

**实现主界面**

添加页面布局

![https://cdn.llfc.club/1728355712673.jpg](https://cdn.llfc.club/1728355712673.jpg)

层级属性

![https://cdn.llfc.club/1728355931100.jpg](https://cdn.llfc.club/1728355931100.jpg)

**MainWindow**

MainWindow构造函数

``` cpp
MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);

    this->resize(800,600);
    //设置默认ip
    ui->addressEd->setText("0.0.0.0");
    //设置spinbox范围
    ui->portSpin->setMaximum(20000);
    //设置端口号
    ui->portSpin->setValue(10086);

    //设置textEdit文字大小
    QFont font = ui->chatEdit->font();
    font.setPointSize(16);
    ui->chatEdit->setFont(font);
    //设置textEdit只读
    ui->chatEdit->setReadOnly(true);
}
```

添加启动服务按钮的响应槽函数

``` cpp
//响应启动按钮
void MainWindow::on_startBtn_clicked()
{
    //设置按钮状态
    ui->startBtn->setEnabled(false);
    bool res = ChatServer::Inst().startServer(
                static_cast<quint16>(ui->portSpin->value()));
    //设置按钮状态
    ui->startBtn->setEnabled(!res);
    ui->closeBtn->setEnabled(res);
}
```

实现关闭服务的函数

``` cpp
//关闭服务
bool ChatServer::stopServer()
{
    //判断服务是否在运行
    if(!(this->isListening())){
        QMessageBox::information(nullptr,"提示信息","服务未启动！");
        return false;
    }

    //关闭服务
    this->close();
    QMessageBox::information(nullptr,"提示信息","服务关闭成功！");
    return true;
}
```

此时启动服务能看到如下界面

![https://cdn.llfc.club/17283590588719.png](https://cdn.llfc.club/17283590588719.png)

关闭服务能看到如下界面

![https://cdn.llfc.club/17283591988187.png](https://cdn.llfc.club/17283591988187.png)

服务器MainWindow构造函数中连接信号

``` cpp
//连接服务器发送的添加文本的信号
connect(&ChatServer::Inst(),&ChatServer::sig_append_msg,this,&MainWindow::slot_append_msg);
```

实现添加消息的槽函数

``` cpp
//添加消息槽函数
void MainWindow::slot_append_msg(QString msg){
    ui->chatEdit->append(msg);
}
```



**测试**

运行服务程序，启动服务器，并且运行客户端，配置服务器地址连接到服务器。

当不同的客户端登录的时候，服务器都会收到信息

可以设置Qt Creator支持多程序启动

![https://cdn.llfc.club/1728375904449.jpg](https://cdn.llfc.club/1728375904449.jpg)



服务器会显示收到的消息，并且广播给其他客户端

![https://cdn.llfc.club/1728369582865.jpg](https://cdn.llfc.club/1728369582865.jpg)

多个客户端会看到共享的聊天信息

![https://cdn.llfc.club/1728369774863.jpg](https://cdn.llfc.club/1728369774863.jpg)



## **TCP粘包问题概述**



在网络编程中，尤其是基于TCP协议的通信中，**粘包（Sticky Packet）**问题是一个常见且需要解决的挑战。粘包问题指的是在传输过程中，多个连续的逻辑数据包被合并为一个数据包发送，或者一个逻辑数据包被拆分为多个数据包接收，导致接收端无法准确区分各个独立的消息边界。



### **1. 什么是TCP粘包问题？**



**TCP协议**（Transmission Control Protocol）是面向连接、可靠、基于字节流的传输层协议。它确保数据在传输过程中按顺序、无差错地到达接收端。然而，**TCP是面向字节流的**，并不维护消息的边界。这意味着发送端发送的每一个`send`或`write`操作的数据，接收端不一定会一一对应地以相同的`read`或`recv`操作接收。这就导致了粘包和分包（拆包）现象的发生。



**粘包**指的是多个独立的逻辑消息被接收端当作一个连续的数据块接收。例如，发送端连续发送两个字符串"Hello"和"World"，接收端可能一次性接收到"HelloWorld"。



**分包**指的是一个逻辑消息被分割成多个数据块接收。例如，发送端发送一个较长的字符串"HelloWorld"，接收端可能分成"Hello"和"World"两次接收。

举个例子，同学A作为客户端向我的服务器发送“**武汉市长江大桥**”，因为分包，导致我收到了两次数据，第一次是"**武汉市长**"，第二次是“**江大桥**”，服务器如果做语法解析会产生歧义，认为武汉的市长叫江大桥。

同样同学B作为客户端向我发送“**南京市长江大桥**”，因为分包，导致我收到了两次，分别是“**南京市长**”以及“**江大桥**”。



### **2. 为什么会发生粘包问题？**



粘包问题的发生主要由以下几个因素引起：



1. **TCP的流式特性**：TCP将数据视为一个连续的字节流，没有明确的消息边界。
2. **发送端的发送策略**：频繁的小数据发送可能导致接收端将多个小数据合并成一个大数据包。(同学们自己查下Nangle算法)
3. **网络传输的优化**：TCP为了提高传输效率，可能会对数据进行合并或拆分。(TCP最大报文单元是1500字节=MTU)
4. **缓冲区管理**：发送和接收双方的缓冲区大小和处理速度不同步，也可能导致粘包或分包现象。



### **3. 粘包问题的影响**



粘包问题会导致以下问题：



- **数据解析错误**：接收端无法准确区分消息边界，导致数据解析错误或不完整。
- **协议混乱**：基于消息的协议（如聊天协议、文件传输协议等）可能无法正确处理接收到的数据。
- **应用程序异常**：业务逻辑可能因为数据错误而出现异常或崩溃。



### **4. 如何解决TCP粘包问题？**



为了解决粘包问题，通常需要在应用层设计一种**协议**来明确消息边界。以下是几种常见的解决方案：



#### **4.1 定长消息协议**



每个消息的长度固定，无论内容多长，始终占用相同的字节数。



**优点**：



- 实现简单，解析方便。



**缺点**：



- 灵活性差，不适用于长度不固定的消息。
- 会浪费带宽，因为短消息需要填充固定长度。



**示例**：



假设每个消息固定长度为100字节：



```plaintext
消息1: "Hello" + 95个填充字节
消息2: "World" + 95个填充字节
```



接收端每次读取100字节，直接解析为一个完整的消息。



#### **4.2 分隔符协议**



在每个消息的末尾添加一个特殊的分隔符（如`\n`、`\r\n`或其他不出现在消息内容中的字符序列）。



**优点**：



- 灵活性高，适用于变长消息。
- 实现相对简单。



**缺点**：



- 需要确保消息内容中不出现分隔符，或对分隔符进行转义处理。



**示例**：



使用换行符作为分隔符：



```plaintext
消息1: "Hello\n"
消息2: "World\n"
```



接收端通过查找换行符来分割消息。



#### **4.3 消息头协议**



每个消息前添加一个固定长度的头部，头部中包含消息体的长度信息。

这是**企业级**常常使用的方案，叫做**TLV协议(TypeID+Len+Value)**， 一般来说就是固定长度的头部+变长的包体

![https://cdn.llfc.club/1728372688899.jpg](https://cdn.llfc.club/1728372688899.jpg)

头部固定四字节，前两个字节表示消息id的类型，比如登录消息是1001，pvp消息是1002等。

头部后两个字节表示消息体的长度，所以我们再往后读取len字节的内容就是消息体了。

消息体长度len存储的是消息内容

**优点**：



- 高效且灵活，适用于大多数场景。
- 能够处理非常大的消息。



**缺点**：



- 实现稍复杂，需要先解析头部再解析消息体。

我们聊天服务不涉及多个协议，所以id字段可以省略，比如我们用四字节表示头部，头部存储的就是后面消息体的长度。

**示例**：



假设头部为4字节，表示消息体的长度：



```plaintext
消息1: [00000005] "Hello"
消息2: [00000005] "World"
```



接收端首先读取4字节头部，解析出消息体长度，再读取相应长度的消息体。

**注意**

学到这里还没结束，存储长度的头部是4字节的，在不同的计算机中字节存储的顺序是不一致的，比如我发送如下

``` cpp
消息1: [00000005] "Hello"
```

对方收到后会根据自己的存储顺序，把`00000005`转化为`05000000`

而`05000000` 转化为10进制会变为`83886080`长度不对了。

这就要引出**大端字节序**和**小端字节序**的概念了



## 大小端字节序

在计算机系统中，**字节序（Endianness）** 指的是多字节数据在内存中存储的顺序。主要分为**大端（Big-Endian）**和**小端（Little-Endian）**两种字节序。了解字节序对于网络编程、跨平台数据交换以及底层系统开发等领域至关重要。



### 大端（Big-Endian）



在**大端**字节序中，**高位字节存储在低地址**，低位字节存储在高地址。也就是说，最重要的字节（MSB）排在最前面。



**示例：**
 假设有一个32位整数 `0x12345678`，在大端系统中的存储方式如下：



| 地址 | 数据 |
| ---- | ---- |
| 0x00 | 0x12 |
| 0x01 | 0x34 |
| 0x02 | 0x56 |
| 0x03 | 0x78 |



### 小端（Little-Endian）



在**小端**字节序中，**低位字节存储在低地址**，高位字节存储在高地址。也就是说，最不重要的字节（LSB）排在最前面。



**示例：**
 同样的32位整数 `0x12345678`，在小端系统中的存储方式如下：



| 地址 | 数据 |
| ---- | ---- |
| 0x00 | 0x78 |
| 0x01 | 0x56 |
| 0x02 | 0x34 |
| 0x03 | 0x12 |

### 为什么会有不同的字节序



不同的字节序主要源于不同计算机体系结构的设计选择：



- **历史原因**：早期的计算机制造商如IBM、DEC等基于不同的设计理念，选择了不同的字节序。
- **性能优化**：在某些架构中，选择特定的字节序可以优化特定类型的计算或数据访问。
- **兼容性考虑**：为了与现有系统和协议保持一致，不同的字节序被采用。



当前，大多数现代计算机（如x86架构）采用小端字节序，而网络协议通常采用大端字节序（也称为网络字节序），这要求在网络通信中进行字节序的转换。

### 字节序的影响



- **跨平台数据交换**：不同系统之间传输二进制数据时，需要确保双方采用相同的字节序，或进行适当的转换。
- **文件格式**：某些文件格式规定了特定的字节序，如BMP文件通常采用小端字节序。
- **网络通信**：网络协议如TCP/IP使用大端字节序，客户端和服务器在传输数据前需要进行字节序转换。
- **硬件接口**：在与不同硬件设备通信时，字节序的一致性是确保数据正确解读的前提。



### C++ 如何判断系统的字节序



**示例代码：**



```cpp
#include <iostream>

bool isLittleEndian() {
    unsigned int x = 1;
    // 将x的地址强制转换为字节指针，并检查第一个字节的值
    return reinterpret_cast<unsigned char*>(&x)[0] == 1;
}

int main() {
    if (isLittleEndian()) {
        std::cout << "系统字节序：小端" << std::endl;
    } else {
        std::cout << "系统字节序：大端" << std::endl;
    }
    return 0;
}
```



**解释**：



- 定义一个`unsigned int`变量，其最低有效字节为1。
- 将其地址转换为`unsigned char*`指针，通过访问第一个字节判断字节序。



### Qt 中处理字节序的方法



Qt提供了`QDataStream`类，用于在读写数据时处理字节序。默认情况下，`QDataStream`使用**大端字节序**，即网络字节序。



**设置字节序**

您可以通过`setByteOrder()`方法设置`QDataStream`的字节序。



**示例代码：**

``` cpp
#include <QCoreApplication>
#include <QDataStream>
#include <QByteArray>
#include <QDebug>

int main(int argc, char *argv[])
{
    QCoreApplication a(argc, argv);

    QByteArray byteArray;
    QDataStream out(&byteArray, QIODevice::WriteOnly);

    // 设置为小端字节序
    out.setByteOrder(QDataStream::LittleEndian);

    quint32 number = 0x12345678;
    out << number;

    // 读取字节
    for (char byte : byteArray) {
        //宽度为2，且为16进制，并且用0补位
        qDebug() << QString("0x%1").arg(static_cast<unsigned char>(byte), 2, 16, QChar('0'));
    }

    return 0;
}
```

**使用`qToBigEndian`和`qToLittleEndian`**

Qt提供了一些辅助函数，用于在编译时或运行时进行字节序转换。



**示例代码：**



```cpp
#include <QCoreApplication>
#include <QtEndian>
#include <QDebug>

int main(int argc, char *argv[])
{
    QCoreApplication a(argc, argv);

    quint32 number = 0x12345678;

    // 转换为大端字节序
    quint32 bigEndianNumber = qToBigEndian(number);
    qDebug() << "大端字节序：" << QString::number(bigEndianNumber, 16).toUpper();

    // 转换为小端字节序
    quint32 littleEndianNumber = qToLittleEndian(number);
    qDebug() << "小端字节序：" << QString::number(littleEndianNumber, 16).toUpper();

    // 检查系统字节序
    if (qIsBigEndian()) {
        qDebug() << "系统字节序：大端";
    }
    else {
        qDebug() << "系统字节序：小端";
    }

    return 0;
}
```



**输出（假设系统为小端）**：



```bash
大端字节序： "12345678"
小端字节序： "78563412"
系统字节序： "小端"
```

### 网络与主机字节序转换



在网络编程中，Qt的`QHostAddress`和相关类通常使用网络字节序（大端）。当处理不同字节序的数据时，可以使用上述方法进行转换。



**示例：发送数据前转换为网络字节序**



```cpp
#include <QTcpSocket>
#include <QtEndian>

void sendData(QTcpSocket *socket, quint32 number) {
    QByteArray data;
    QDataStream out(&data, QIODevice::WriteOnly);
    
    // 转换为大端字节序（网络字节序）
    quint32 networkNumber = qToBigEndian(number);
    out << networkNumber;
    
    socket->write(data);
}
```



**示例：接收数据后转换为主机字节序**



```cpp
#include <QTcpSocket>
#include <QtEndian>

void readData(QTcpSocket *socket) {
    QDataStream in(socket);
    quint32 networkNumber;
    in >> networkNumber;
    
    // 转换为主机字节序
    quint32 hostNumber = qFromBigEndian(networkNumber);
    
    qDebug() << "接收到的数字：" << hostNumber;
}
```

## 完善聊天室程序(TLV拓展)

**服务器TLV模式**

首先我们服务器收到的消息可能是不完整的，所以就要存储从每个客户端socket收到的信息。

所以将Chatserver中的客户端集合，由下方

``` cpp
//客户端连接的集合
QSet<QTcpSocket*> clients;
```

改为下方, 我们通过map存储每个socket对应的接受缓冲区

``` cpp
// 存储每个客户端的接收缓冲区
QMap<QTcpSocket*, QByteArray> _bufferMap;
```

我们修改ChatServer的读取功能

``` cpp
//读取客户端发送的数据
void ChatServer::slot_ready_read()
{
    //将发送信号的对象转化为QTcpSocket类型
    QTcpSocket* clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (!clientSocket)
        return;

    //读取信息
    QByteArray data = clientSocket->readAll();
    //存储收到的数据
    _bufferMap[clientSocket].append(data);
    //处理数据
    processData(clientSocket);
}
```

在读取函数中我们将读到的数据先存起来，然后调用processData进行处理

``` cpp
void ChatServer::processData(QTcpSocket* client)
{
    //获取socket对应的数据
    QByteArray& buffer = _bufferMap[client];

    while (buffer.size() >= 4) { // 至少有头部长度
        // 读取头部
        QByteArray head = buffer.left(4);
        QDataStream ds(head);
        ds.setByteOrder(QDataStream::BigEndian);
        quint32 bodyLength;
        ds >> bodyLength;

        if (buffer.size() >= 4 + bodyLength) {
            // 完整的消息体已经接收
            QByteArray body = buffer.mid(4, bodyLength);
            buffer = buffer.mid(4 + bodyLength);

            QString message = QString::fromUtf8(body);
            qDebug() << "Received message:" << message;

            //通知主界面添加消息
            emit sig_append_msg(message);

            // 广播消息给所有客户端
            broadcastMessage(body, bodyLength, client);
        } else {
            // 消息体未完全接收，等待更多数据
            break;
        }
    }
}
```

因为修改了clients从set到map的结构，所以广播函数要做下修改

``` cpp
//广播消息
void ChatServer::broadcastMessage(QByteArray body, int bodyLength, QTcpSocket *client)
{
    // 广播消息给所有客户端
    QByteArray response;
    // 写数据流绑定到字节数组中，所有向流写入的数据都会写入到response数组
    QDataStream responseStream(&response, QIODevice::WriteOnly);
    // 设置大端模式
    responseStream.setByteOrder(QDataStream::BigEndian);
    // 写入长度
    responseStream << bodyLength;
    // 追加包体内容
    response.append(body);
    // 遍历
    foreach (QTcpSocket* clientSocket, _bufferMap.keys()) {
        // 不发送给源客户端
        if (clientSocket != client) {
            clientSocket->write(response);
        }
    }
}
```

修改其他几处处理socket的逻辑

``` cpp
//获取新来的连接
void ChatServer::incomingConnection(qintptr socketDescriptor)
{
    QTcpSocket* clientSocket = new QTcpSocket(this);
    if (!clientSocket->setSocketDescriptor(socketDescriptor)) {
        qDebug() << "Failed to set socket descriptor";
        clientSocket->deleteLater();
        return;
    }

    //将客户端加入集合
    _bufferMap.insert(clientSocket,QByteArray());

    //连接读取信息信号
    connect(clientSocket, &QTcpSocket::readyRead, this, &ChatServer::slot_ready_read);
    //连接客户端断开信号
    connect(clientSocket, &QTcpSocket::disconnected, this, &ChatServer::slot_disconnect);

    //打印对端地址
    qDebug() << "New client connected:" << clientSocket->peerAddress().toString();
}

```

更新断开连接

``` cpp
//获取客户端断开连接槽函数
void ChatServer::slot_disconnect()
{
    //获取发送者转为QTcpSocket类型
    QTcpSocket* clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (!clientSocket)
        return;

    //获取对端地址
    auto address = clientSocket->peerAddress().toString();
    //从客户端移除
    _bufferMap.remove(clientSocket);
    //删除socket
    clientSocket->deleteLater();
    //推广离开信息
    QString leftMessage = QString("%1 left the chat.").arg(address);
    auto byteArray = leftMessage.toUtf8();
    broadcastMessage(byteArray, byteArray.size(), clientSocket);
    //发送消息通知主界面显示离开信息
    emit sig_append_msg(leftMessage);
    qDebug() << "Client disconnected:" << address;
}
```

到此为止，服务器改造完毕。

**客户端TLV模式**

客户端TcpClient新增成员_buffer用来缓冲收到的数据

``` cpp
//缓存收到的数据
QByteArray _buffer;
```

修改发送数据的函数

``` cpp
//发送数据槽函数
void TcpClient::slot_send_msg(const QString &msg)
{
    //如果连接异常则直接返回
    if(_socket->state() != QAbstractSocket::ConnectedState){
        QMessageBox::information(nullptr,"提示消息","断开连接无法发送");
        return;
    }

    //将msg转化为字节数组
    QByteArray body = msg.toUtf8();
    //获取body的长度
    quint32 bodyLength = body.size();

    //创建字节数组
    QByteArray data;
    //绑定字节数组
    QDataStream stream(&data, QIODevice::WriteOnly);
    //设置大端模式
    stream.setByteOrder(QDataStream::BigEndian);
    //写入长度
    stream << bodyLength;
    //写入包体
    data.append(body);

    //发送消息
     _socket->write(data);
}
```

收到数据后先缓存起来，因为数据可能没收完整，或者多个包粘连在一起

``` cpp
//接受服务器发送的信息
void TcpClient::slot_ready_read()
{
    //读取所有数据
    QByteArray data = _socket->readAll();

    //将数据缓存起来
    _buffer.append(data);

    //处理收到的数据
    processData();
}
```

实现数据处理

``` cpp
void TcpClient::processData()
{
    while(_buffer.size() >= 4){
        //先取出四字节头部
        auto head_byte = _buffer.left(4);
        QDataStream stream(head_byte);
        //设置为大端模式
        stream.setByteOrder(QDataStream::BigEndian);
        //读取长度
        quint32 body_length;
        stream >> body_length;
        if(_buffer.size() >= 4+body_length){
            //完整的消息体已经接受
            QByteArray body = _buffer.mid(4,body_length);
            //去掉完整的消息包
            _buffer = _buffer.mid(4+body_length);
            //发送消息给MainWindow显示
            emit sig_append_msg(QString::fromUtf8(body));
        }else{
            //消息未完全接受，所以中断
            break;
        }
    }
}
```

再次运行客户端和服务器，可以看到TLV模式生效了

![https://cdn.llfc.club/1728383034338.jpg](https://cdn.llfc.club/1728383034338.jpg)



## UDP协议(拓展选学)

- **UDP（用户数据报协议）**：无连接，提供尽力而为的包传输，适用于对实时性要求高但对数据可靠性要求相对较低的应用。



### **1.2 UDP协议概述**



**UDP**是一种简单的传输层协议，具有以下特点：



- **无连接**：发送数据前不需要建立连接，直接发送数据包。
- **不保证可靠性**：数据包可能丢失、重复或失序，且不进行重传。
- **低开销**：由于没有连接管理和流量控制，适合需要高性能的应用。
- **数据报传输**：以单个数据报的形式发送，每个数据报独立处理。



**应用场景**：



- 实时视频/音频传输
- DNS查询
- 物联网设备通信



### **1.3 Qt网络模块中的UDP支持**



Qt通过`QUdpSocket`类提供对UDP通信的支持，使得开发跨平台的UDP应用更加简便。



------



## **QUdpSocket类详解**



`QUdpSocket`是Qt中专门用于UDP网络通信的类。它继承自`QAbstractSocket`，提供了一系列用于发送和接收UDP数据报的方法和信号。



### **1 QUdpSocket的基本功能**



- **发送数据**：通过`writeDatagram()`方法发送数据报。
- **接收数据**：通过绑定套接字并监听数据到达，接收到的数据通过信号`readyRead()`通知。
- **绑定端口**：通过`bind()`方法绑定本地端口进行接收。



### **2 关键方法解析**



- `void bind(const QHostAddress &address = QHostAddress::Any, quint16 port = 0, BindMode mode = DefaultForPlatform)`
  - 绑定本地地址和端口，以便接收数据。
- `qint64 writeDatagram(const QByteArray &datagram, const QHostAddress &host, quint16 port)`
  - 发送数据报到指定的主机和端口。
- `qint64 writeDatagram(const char *data, qint64 size, const QHostAddress &host, quint16 port)`
  - 重载形式，发送指定大小的数据。
- `void close()`
  - 关闭套接字。



### **3 QUdpSocket的信号**



- `void readyRead()`
  - 当有新的数据报到达时发出。
- `void datagramWritten(qint64 bytes)`
  - 当数据报被成功发送时发出。
- `void errorOccurred(QAbstractSocket::SocketError socketError)`
  - 当发生错误时发出。



### **4 QUdpSocket与TCP编程的对比**



| 特性     | TCP                                      | UDP                            |
| -------- | ---------------------------------------- | ------------------------------ |
| 连接性   | 面向连接，需建立连接                     | 无连接，直接发送数据报         |
| 可靠性   | 高，保证数据按序传输，无数据丢失         | 低，数据包可能丢失、重复、无序 |
| 传输方式 | 字节流                                   | 数据报                         |
| 开销     | 高，需管理连接和状态                     | 低，无需连接管理               |
| 适用场景 | 文件传输、网页浏览、电子邮件，在线游戏等 | 实时视频、音频等               |

## 聊天室案例UDP版(课外拓展)

UDP应用的场景有限，大多是对数据安全性不高的场景，我们的聊天服务也可以改为UDP版本, 效果如下图

![https://cdn.llfc.club/1728455833686.jpg](https://cdn.llfc.club/1728455833686.jpg)



**客户端实现**

我们可以自定义一个UdpClient类

``` cpp
#ifndef UDPCLIENT_H
#define UDPCLIENT_H

#include <QObject>
#include <QUdpSocket>

class UdpClient : public QObject
{
    Q_OBJECT
public:
    static UdpClient& Inst(){
        static UdpClient udpclient;
        return udpclient;
    }

    void bindPort(QString serverip, quint16 serverport, quint16 selfport);
    void processPendingDatagrams();
    void setName(QString);
private:
    explicit UdpClient(QObject *parent = nullptr);
    UdpClient(const UdpClient& uc) = delete;
    UdpClient& operator=(const UdpClient&) = delete;
    ~UdpClient();
    //udp socket用来通信
    QUdpSocket * _udpSocket;
    //服务器地址
    QHostAddress _server_address;
    //服务器端口
    quint16 _server_port;
    //客户端用户名
    QString  _name;
signals:
    //通知MainWindow显示信息
    void sig_append_msg(QString);
public slots:
    //发送消息的槽函数
    void slot_send_msg(QString);
};

#endif // UDPCLIENT_H

```

具体实现

``` cpp
#include "udpclient.h"
#include <QUdpSocket>
#include <QTextStream>

UdpClient::UdpClient(QObject *parent) : QObject(parent),_server_address(QHostAddress("127.0.0.1")),
    _server_port(20001)
{
    _udpSocket = new QUdpSocket(this);

    //连接信息到来的信号
    connect(_udpSocket, &QUdpSocket::readyRead, this, &UdpClient::processPendingDatagrams);
}

UdpClient::~UdpClient()
{

}

void UdpClient::slot_send_msg(QString message)
{
    message = QString("[%1] : %2").arg(_name).arg(message);

    //发送消息
    _udpSocket->writeDatagram(message.toUtf8(),
                              _server_address,
                              _server_port);

    //通知界面显示
    emit sig_append_msg(message);
}

//接受数据
void UdpClient::bindPort(QString serverip, quint16 serverport, quint16 selfport)
{
    //服务地址
    _server_address = QHostAddress(serverip);
    //服务器端口
    _server_port = serverport;
    // 绑定地址和端口
    _udpSocket->bind(QHostAddress::Any,selfport,QAbstractSocket::ShareAddress);
}

void UdpClient::processPendingDatagrams()
{
    while (_udpSocket->hasPendingDatagrams()) {
        QByteArray datagram;
        //udp不需要tlv，可以直接读取包的大小
        datagram.resize(static_cast<int>(_udpSocket->pendingDatagramSize()));
        QHostAddress sender;
        quint16 senderPort;
        //读取对端发送的数据，并且获取对端的ip和端口
        _udpSocket->readDatagram(datagram.data(), datagram.size(), &sender, &senderPort);
        QString message = QString::fromUtf8(datagram);
        qDebug() << "收到来自" << sender.toString() << ":" << senderPort << "的数据：" << message;
        //发送消息给MainWindow
        emit sig_append_msg(message);
    }
}

void UdpClient::setName(QString name)
{
    _name = name;
}

```

MainWindow声明

``` cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>

namespace Ui {
class MainWindow;
}

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private:
    Ui::MainWindow *ui;

public slots:
    //客户端端口改变
    void slot_client_port_changed(int value);
    //服务器端口改变
    void slot_server_port_changed(int value);
    //客户端地址改变
    void slot_server_address_changed();
    //追加消息
    void slot_append_msg(QString msg);
private slots:
    //发送按钮点击槽函数
    void on_send_btn_clicked();

signals:
    //通知udpclient发送消息的信号
    void sig_send_msg(QString);
};

#endif // MAINWINDOW_H

```

MainWindow界面拷贝之前的TcpClient版本的MainWindow就行了，稍作修改，增加一个自己的端口号，一般不用修改

![https://cdn.llfc.club/1728438939218.jpg](https://cdn.llfc.club/1728438939218.jpg)

MainWindow具体实现

``` cpp
#include "mainwindow.h"
#include "ui_mainwindow.h"
#include <QRandomGenerator>
#include "udpclient.h"

MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    this->setWindowTitle("客户端");
    ui->address_ed->setText("127.0.0.1");
    ui->name_ed->setText("尼采");
    ui->port_spin->setMaximum(25000);
    ui->port_spin->setValue(20001);
    ui->clientPort->setMaximum(20000);

    //设置textEdit文字大小
    QFont font = ui->chatEdit->font();
    font.setPointSize(16);
    ui->chatEdit->setFont(font);
    ui->chatEdit->setReadOnly(true);

    // 创建一个 QRandomGenerator 实例
    QRandomGenerator *generator = QRandomGenerator::global();
    int randomInRange = generator->bounded(0, 20000);
    ui->clientPort->setValue(randomInRange);

    //显示调用一下槽函数用来绑定端口
    slot_client_port_changed(randomInRange);

    UdpClient::Inst().setName(ui->name_ed->text());

    //选择int类型版本的信号
    connect(ui->clientPort, QOverload<int>::of(&QSpinBox::valueChanged),
            this, &MainWindow::slot_client_port_changed);

    //连接int类型版本的信号
    connect(ui->port_spin, QOverload<int>::of(&QSpinBox::valueChanged), this,
            &MainWindow::slot_server_port_changed);

    //连接服务修改
    connect(ui->address_ed,&QLineEdit::editingFinished,this,&MainWindow::slot_server_address_changed);

    //连接发送数据的信号
    connect(this, &MainWindow::sig_send_msg, &UdpClient::Inst(), &UdpClient::slot_send_msg);

    //名字编辑
    connect(ui->name_ed, &QLineEdit::editingFinished, this, [=](){
        UdpClient::Inst().setName(ui->name_ed->text());
    });

    //发送信号更新界面
    connect(&UdpClient::Inst(), &UdpClient::sig_append_msg,
            this, &MainWindow::slot_append_msg);
}

MainWindow::~MainWindow()
{
    delete ui;
}

void MainWindow::slot_client_port_changed(int value)
{
    UdpClient::Inst().bindPort(ui->address_ed->text(),
                               static_cast<quint16>(ui->port_spin->value()),
                               static_cast<quint16>(value));
}

void MainWindow::slot_server_port_changed(int value)
{
    UdpClient::Inst().bindPort(ui->address_ed->text(),
                               static_cast<quint16>(value),
                               static_cast<quint16>(ui->clientPort->value()));
}

void MainWindow::slot_server_address_changed()
{
    UdpClient::Inst().bindPort(ui->address_ed->text(),
                               static_cast<quint16>(ui->port_spin->value()),
                               static_cast<quint16>(ui->clientPort->value()));
}

void MainWindow::on_send_btn_clicked()
{
    auto message = ui->msg_ed->text();
    emit sig_send_msg(message);
}

void MainWindow::slot_append_msg(QString msg){
    ui->chatEdit->append(msg);
}
```

**服务器**

udpserver类声明

``` cpp
#ifndef UDPSERVER_H
#define UDPSERVER_H

#include <QObject>
#include <QUdpSocket>
#include <QHash>
#include <QHostAddress>

class UdpServer : public QObject
{
    Q_OBJECT
public:
    static UdpServer& Inst();
    //启动服务
    void startServer(int port);
    //关闭服务
    void closeServer();
    //广播消息
    void broadCastMsg(QString key, QByteArray datagram);
private:
    explicit UdpServer(QObject *parent = nullptr);
    UdpServer(const UdpServer& ) = delete;
    UdpServer& operator=(const UdpServer&) = delete;
    QUdpSocket * _udpSocket;
    quint16 _listenPort;

    struct ClientInfo{
        QHostAddress _address;
        quint16 _port;
    };

    //ip端口字符串到具体地址的映射
    QHash<QString, ClientInfo> _ip_ports;
signals:
    //通知MainWindow显示消息
    void sig_append_msg(QString);
public slots:
    //处理udp收到的消息
    void processPendingDatagrams();
};

#endif // UDPSERVER_H

```

udpserver的具体实现

``` cpp
#include "udpserver.h"
#include <QMessageBox>

UdpServer &UdpServer::Inst()
{
    static UdpServer udpserver;
    return udpserver;
}

void UdpServer::startServer(int port)
{
    if (!_udpSocket->bind(QHostAddress::Any, static_cast<quint16>(port))) {
        QMessageBox::information(nullptr, "提示信息","绑定端口失败!");
        return;
    }

    QMessageBox::information(nullptr,"提示信息",
                             QString("实时数据UDP服务器已启动，监听端口[%1]").arg(port));
}

void UdpServer::closeServer()
{
    _udpSocket->close();
    QMessageBox::information(nullptr,"提示信息",
                             QString("实时数据UDP服务器已关闭"));
}

//广播消息
void UdpServer::broadCastMsg(QString key, QByteArray datagram)
{
    for(auto & ip_port : _ip_ports.keys()){
        //如果是消息源客户端则不发送
        if(ip_port == key){
            continue;
        }
        //获取用户信息
        auto client_info = _ip_ports[ip_port];
        //发送信息给其他用户
        _udpSocket->writeDatagram(datagram, client_info._address, client_info._port);
    }
}

UdpServer::UdpServer(QObject *parent) : QObject(parent)
{
    //创建udpsocket
    _udpSocket = new QUdpSocket(this);
    //连接读取信息的信号
    connect(_udpSocket, &QUdpSocket::readyRead, this, &UdpServer::processPendingDatagrams);
}

void UdpServer::processPendingDatagrams()
{
    //获取对端发送的消息
    while (_udpSocket->hasPendingDatagrams()) {
          QByteArray datagram;
          //重置大小
          datagram.resize(static_cast<int>(_udpSocket->pendingDatagramSize()));
          QHostAddress sender;
          quint16 senderPort;

          _udpSocket->readDatagram(datagram.data(), datagram.size(), &sender, &senderPort);
          QString message = QString::fromUtf8(datagram);
          qDebug() << "收到来自" << sender.toString() << ":" << senderPort << "的消息：" << message;
          //发送消息给主界面
          emit sig_append_msg(message);

          //记录来自客户端的地址和端口，拼接成串
          auto key = sender.toString()+ QString::number(senderPort);
          //客户端地址信息
          ClientInfo client_info;
          client_info._address = sender;
          client_info._port = senderPort;
          _ip_ports.insert(key, client_info);

          //广播消息
          broadCastMsg(key,datagram);
      }
}

```

MainWindow界面稍作修改，因为udpserve只需要绑定端口就行了

![https://cdn.llfc.club/1728456585078.jpg](https://cdn.llfc.club/1728456585078.jpg)

mainwindow的声明

``` cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>

namespace Ui {
class MainWindow;
}

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    //点击开始后按钮
    void on_startBtn_clicked();
    //点击关闭按钮
    void on_closeBtn_clicked();
    //追加消息到屏幕
    void slot_append_msg(QString);

private:
    Ui::MainWindow *ui;
};

#endif // MAINWINDOW_H

```

MainWindow具体实现

``` cpp
#include "mainwindow.h"
#include "ui_mainwindow.h"
#include "udpserver.h"
#include "udpserver.h"

MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    this->setWindowTitle("服务器");
    ui->addressEd->setText("0.0.0.0");
    ui->portSpin->setMaximum(25000);
    ui->portSpin->setValue(20001);
    ui->chatEdit->setReadOnly(true);

    //设置textEdit文字大小
    QFont font = ui->chatEdit->font();
    font.setPointSize(16);
    ui->chatEdit->setFont(font);

    ui->startBtn->setEnabled(true);
    ui->closeBtn->setEnabled(false);

    connect(&UdpServer::Inst(),&UdpServer::sig_append_msg,
            this, &MainWindow::slot_append_msg);
}

void MainWindow::slot_append_msg(QString msg){
    ui->chatEdit->append(msg);
}

MainWindow::~MainWindow()
{
    delete ui;
}

//启动服务器
void MainWindow::on_startBtn_clicked()
{
    //启动服务
    UdpServer::Inst().startServer(static_cast<int>(ui->portSpin->value()));
    ui->startBtn->setEnabled(false);
    ui->closeBtn->setEnabled(true);
}

void MainWindow::on_closeBtn_clicked()
{
    //关闭服务
    UdpServer::Inst().closeServer();
    ui->startBtn->setEnabled(true);
    ui->closeBtn->setEnabled(false);
}

```

此时运行服务器，启动多个客户端，修改为不同的名字，将消息发送给服务器，可以看到服务器收到消息并回复给其他客户端。



## **HTTP协议简介**(课外拓展)



### **HTTP的基本概念**



**HTTP（HyperText Transfer Protocol）** 是用于分布式、协作式和超媒体信息系统的应用层协议。它是万维网的基础，定义了浏览器与服务器之间传输数据的规则。

HTTP是基于tcp实现的短链接，服务器收到客户端处理后将消息推送给客户端，然后关闭单方连接，客户端收到后也关闭单方连接。



### **HTTP协议的工作原理**



1. **客户端发起请求**：浏览器或其他客户端向服务器发送HTTP请求。
2. **服务器处理请求**：服务器接收到请求后进行相应的处理，如读取文件、执行脚本等。
3. **服务器返回响应**：处理完成后，服务器返回HTTP响应给客户端。
4. **客户端处理响应**：客户端接收到响应后，渲染页面或进行其他操作。



### **常见的HTTP方法和状态码**



- **HTTP方法**：
  - `GET`：请求指定的资源。
  - `POST`：向指定资源提交数据。
  - `PUT`：更新指定资源。
  - `DELETE`：删除指定资源。
  - `HEAD`：获取资源的头部信息。
  - `OPTIONS`：获取服务器支持的HTTP方法。
- **HTTP状态码**：
  - `200 OK`：请求成功。
  - `201 Created`：资源创建成功。
  - `400 Bad Request`：客户端请求有语法错误。
  - `401 Unauthorized`：未经授权。
  - `404 Not Found`：资源未找到。
  - `500 Internal Server Error`：服务器内部错误。



### HTTP 头部的基本格式



1. **请求/响应行**（Request/Response Line）

   - 请求行

     （Request Line）：包含请求方法、请求 URI 和 HTTP 版本。

     - 例子：`GET /index.html HTTP/1.1`

   - 响应行

     （Response Line）：包含 HTTP 版本、状态码和状态消息。

     - 例子：`HTTP/1.1 200 OK`

2. **头部字段**（Header Fields）

   - 每个头部字段由一个字段名和一个字段值组成，中间用冒号 `:` 分隔。字段名和字段值之间可以有空格。

   - 头部字段的格式如下：

     ```makefile
     Field-Name: Field-Value
     ```

   - 头部字段可以有多行，通常使用换行符（CRLF）来分隔。

3. **空行**（Empty Line）

   - 请求/响应行和头部字段之间用一个空行分隔，表示头部的结束。



### HTTP 请求示例



```http
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Connection: keep-alive
```



### HTTP 响应示例



```http
HTTP/1.1 200 OK
Date: Wed, 21 Oct 2015 07:28:00 GMT
Server: Apache/2.4.1 (Unix)
Last-Modified: Wed, 21 Oct 2015 07:28:00 GMT
Content-Type: text/html; charset=UTF-8
Content-Length: 1234
Connection: close

<html>
<head><title>Example</title></head>
<body><h1>Hello, World!</h1></body>
</html>
```



### 常用 HTTP 头部字段



#### 请求头部字段



- `Host`: 指定请求的主机名和端口号。
- `User-Agent`: 指定发起请求的客户端软件信息。
- `Accept`: 指定客户端能够接收的内容类型。
- `Authorization`: 用于提供身份验证凭据。
- `Content-Type`: 指定请求体的媒体类型（通常在 POST 请求中使用）。



#### 响应头部字段



- `Content-Type`: 指定响应体的媒体类型。
- `Content-Length`: 指定响应体的字节长度。
- `Set-Cookie`: 用于设置 HTTP cookies。
- `Cache-Control`: 指定缓存机制。
- `Location`: 用于重定向，指定新的 URL。



以下是一些常见的 HTTP 请求内容类型及其用途：



1. **application/json**：
   - 用于发送 JSON 格式的数据。广泛用于 RESTful API。
   - 示例：`Content-Type: application/json`
2. **application/x-www-form-urlencoded**：
   - 用于表单提交时，数据以 URL 编码的形式发送。每个键值对通过 `&` 符号连接，键和值通过 `=` 符号连接。
   - 示例：`Content-Type: application/x-www-form-urlencoded`
3. **multipart/form-data**：
   - 用于表单提交时，尤其是当表单包含文件上传时。它允许在同一请求中发送多种类型的数据。
   - 示例：`Content-Type: multipart/form-data; boundary=---011000010111000001110001`
4. **text/plain**：
   - 用于发送纯文本数据，不带格式。
   - 示例：`Content-Type: text/plain`
5. **application/xml**：
   - 用于发送 XML 格式的数据。
   - 示例：`Content-Type: application/xml`
6. **text/html**：
   - 用于发送 HTML 格式的数据。
   - 示例：`Content-Type: text/html`
7. **application/octet-stream**：
   - 用于发送二进制数据，通常用于文件下载或未指定类型的内容。
   - 示例：`Content-Type: application/octet-stream`



### **Qt5与Qt6的差异**



在Qt6中，引入了更高级的HTTP服务器类（如`QHttpServer`），简化了HTTP服务器的实现过程。而在Qt5.12中，需要使用`QTcpServer`和`QTcpSocket`结合手动解析HTTP请求和构建响应。这不仅增加了实现的复杂度，但也提供了更多的学习和理解HTTP协议的机会。

### 跨域问题



跨域问题（CORS，Cross-Origin Resource Sharing）是指浏览器的同源策略限制了一个网页能够请求不同源（域名、协议或端口不同）的资源。由于安全原因，浏览器默认不允许跨域请求，以防止恶意网站窃取用户数据或进行其他恶意操作。



### 什么是同源策略？



同源策略是指在一个网页中，脚本只能访问与其同源的资源。所谓同源是指：



- 协议相同（http、https）
- 域名相同（[example.com](http://example.com/)、[sub.example.com](http://sub.example.com/)）
- 端口相同（80、443等）



例如，以下两个 URL 是同源的：



- `http://example.com/page1`
- `http://example.com/page2`



而以下两个 URL 则是不同源的：



- `http://example.com/page1`
- `http://another.com/page2`



### 跨域请求的场景



跨域请求通常发生在以下几种场景中：



1. **AJAX 请求**：当网页通过 JavaScript 使用 `XMLHttpRequest` 或 `fetch` API 发起请求时，如果请求的 URL 不同于当前网页的 URL，就会发生跨域请求。
2. **Web 字体**：如果网页使用了来自不同源的字体文件，浏览器会进行跨域请求。
3. **图片、视频等媒体资源**：如果网页中引用了来自不同源的图片或视频，也会涉及跨域请求。



### 如何解决跨域问题？



1. **CORS（跨源资源共享）**：

   - 服务器可以通过设置 HTTP 响应头来允许特定的源访问资源。常用的 CORS 头包括：
     - `Access-Control-Allow-Origin`: 指定允许哪些源进行访问，可以是具体的域名或 `*`（表示允许所有源）。
     - `Access-Control-Allow-Methods`: 指定允许的 HTTP 方法（GET, POST, OPTIONS等）。
     - `Access-Control-Allow-Headers`: 指定允许的请求头。

   例如，以下响应头允许来自任意源的 GET 和 POST 请求：

   ```makefile
   Access-Control-Allow-Origin: *
   Access-Control-Allow-Methods: GET, POST
   ```

2. **JSONP（JSON with Padding）**：

   - 通过 `<script>` 标签加载数据，利用 JavaScript 的动态脚本加载特性来实现跨域请求。虽然这种方法可以解决跨域问题，但它只支持 GET 请求，并且存在安全隐患。

3. **代理服务器**：

   - 在同源的服务器上设置一个代理，客户端请求代理服务器，代理服务器再去请求目标资源。这样可以绕过浏览器的同源策略。

4. **使用 WebSocket**：

   - WebSocket 协议不受同源策略的限制，可以用于实现跨域通信。







### 实现HttpServer

**HttpServer**

接下来我们基于QTcpServer和QTcpSocket实现一个http服务

``` cpp
#ifndef HTTPSERVER_H
#define HTTPSERVER_H

#include <QObject>
#include <QTcpServer>
#include <QTcpSocket>

class HttpServer : public QObject
{
    Q_OBJECT
public:
    explicit HttpServer(quint16 port, QObject *parent = nullptr);
    bool start();

private slots:
    // 新连接建立触发
    void onNewConnection();
    // 读就绪触发的槽函数
    void onReadyRead();
    // 断开连接触发的槽函数
    void onDisconnected();

private:
    QTcpServer *tcpServer;
    quint16 listenPort;

    // 简单的请求处理方法
    void handleRequest(QTcpSocket *socket, const QString &request);
    // 处理post请求
    void handlePostRequest(QTcpSocket *socket, const QString &request);
};

#endif // HTTPSERVER_H

```

添加实现

构造函数里创建QTcpServer对象，并且连接信号

``` cpp
HttpServer::HttpServer(quint16 port, QObject *parent)
    : QObject(parent), listenPort(port)
{
    tcpServer = new QTcpServer(this);
    connect(tcpServer, &QTcpServer::newConnection, this, &HttpServer::onNewConnection);
}
```

新连接触发的槽函数

``` cpp
void HttpServer::onNewConnection()
{
    while (tcpServer->hasPendingConnections()) {
        QTcpSocket *clientSocket = tcpServer->nextPendingConnection();
        qDebug() << "新的连接来自" << clientSocket->peerAddress().toString() << ":" << clientSocket->peerPort();

        connect(clientSocket, &QTcpSocket::readyRead, this, [=]() { onReadyRead(); });
        connect(clientSocket, &QTcpSocket::disconnected, this, [=]() { onDisconnected(); });
    }
}
```

开始启动

``` cpp
bool HttpServer::start()
{
    if (!tcpServer->listen(QHostAddress::Any, listenPort)) {
        qCritical() << "无法启动服务器:" << tcpServer->errorString();
        return false;
    }
    qDebug() << "HTTP服务器已启动，监听端口" << listenPort;
    return true;
}
```

读取数据和断开连接

``` cpp
//读取数据
void HttpServer::onReadyRead()
{
    QTcpSocket *clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (!clientSocket)
        return;

    while (clientSocket->canReadLine()) {
        QByteArray requestData = clientSocket->readAll();
        QString requestString(requestData);
        qDebug() << "收到请求：" << requestString;

        handleRequest(clientSocket, requestString);
    }
}

//断开连接
void HttpServer::onDisconnected()
{
    QTcpSocket *clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (clientSocket) {
        qDebug() << "连接断开：" << clientSocket->peerAddress().toString() << ":" << clientSocket->peerPort();
        clientSocket->deleteLater();
    }
}
```

处理get和post请求

``` cpp
// 修改 handleRequest 方法以调用 handlePostRequest
void HttpServer::handleRequest(QTcpSocket *socket, const QString &request)
{
    // 解析请求行
    QStringList requestLines = request.split("\r\n");
    if (requestLines.isEmpty()) {
        // 无效请求
        return;
    }

    QString requestLine = requestLines.at(0);
    QStringList requestParts = requestLine.split(" ");
    if (requestParts.size() < 3) {
        // 无效请求行
        return;
    }

    QString method = requestParts.at(0);
    QString path = requestParts.at(1);
    QString httpVersion = requestParts.at(2);

    // 添加 CORS 头, 支持跨域访问
    QString corsHeaders = "Access-Control-Allow-Origin: *\r\n" // 允许所有来源
                          "Access-Control-Allow-Methods: GET, POST, OPTIONS\r\n" // 允许的方法
                          "Access-Control-Allow-Headers: Content-Type\r\n"; // 允许的请求头

    if (method == "OPTIONS") {
        // 处理预检请求
        QString response = "HTTP/1.1 204 No Content\r\n"
                           "Connection: close\r\n"
                           + corsHeaders + "\r\n";
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
        return;
    }

    if (method == "GET") {
        // 处理GET请求（之前的逻辑）
        if (path == "/") {
            QString body = "欢迎使用Qt 5.12 创建的简单HTTP服务器！\n";
            QString response = QString("HTTP/1.1 200 OK\r\n"
                                       "Content-Type: text/plain; charset=utf-8\r\n"
                                       "Content-Length: %1\r\n"
                                       "Connection: close\r\n"
                                       + corsHeaders + "\r\n%2")
                                  .arg(body.length())
                                  .arg(body);
            socket->write(response.toUtf8());
            socket->flush();
            socket->disconnectFromHost();
            return;
        }
        else if (path == "/api/hello") {
            QString body = "{\"message\": \"Hello, World!\"}\n";
            QString response = QString("HTTP/1.1 200 OK\r\n"
                                       "Content-Type: application/json\r\n"
                                       "Content-Length: %1\r\n"
                                       "Connection: close\r\n"
                                       + corsHeaders + "\r\n%2")
                                  .arg(body.length())
                                  .arg(body);
            socket->write(response.toUtf8());
            socket->flush();
            socket->disconnectFromHost();
            return;
        }
        else {
            // 处理404
            QString body = "404 - Not Found\n";
            QString response = QString("HTTP/1.1 404 Not Found\r\n"
                                       "Content-Type: text/plain\r\n"
                                       "Content-Length: %1\r\n"
                                       "Connection: close\r\n"
                                       + corsHeaders + "\r\n%2")
                                  .arg(body.length())
                                  .arg(body);
            socket->write(response.toUtf8());
            socket->flush();
            socket->disconnectFromHost();
            return;
        }
    }
    else if (method == "POST") {
        // 处理POST请求
        handlePostRequest(socket, request);
    }
    else {
        // 不支持的方法
        QString response = "HTTP/1.1 501 Not Implemented\r\n"
                           "Content-Length: 0\r\n"
                           "Connection: close\r\n"
                           + corsHeaders + "\r\n";
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
        return;
    }
}
```

处理post请求

``` cpp
//处理post请求
void HttpServer::handlePostRequest(QTcpSocket *socket, const QString &request)
{
    qDebug() << "hello world!";
    // 简化示例：假设请求体是JSON格式，并且以空行结束
    QStringList requestLines = request.split("\r\n\r\n");
    if (requestLines.size() < 2) {
        // 无效请求
        return;
    }

    QString headersPart = requestLines.at(0);
    QString bodyPart = requestLines.at(1);

    // 处理请求行
    QStringList headerLines = headersPart.split("\r\n");
    if (headerLines.isEmpty()) {
        return;
    }

    QString requestLine = headerLines.at(0);
    QStringList requestParts = requestLine.split(" ");
    if (requestParts.size() < 3) {
        return;
    }

    QString method = requestParts.at(0);
    QString path = requestParts.at(1);
    QString httpVersion = requestParts.at(2);

    // 添加 CORS 头
    QString corsHeaders = "Access-Control-Allow-Origin: *\r\n" // 允许所有来源
                          "Access-Control-Allow-Methods: GET, POST, OPTIONS\r\n" // 允许的方法
                          "Access-Control-Allow-Headers: Content-Type\r\n"; // 允许的请求头

    if (method != "POST") {
        // 仅处理POST请求
        return;
    }

    // 解析JSON体
    QJsonDocument jsonDoc = QJsonDocument::fromJson(bodyPart.toUtf8());
    if (!jsonDoc.isObject()) {
        QString response = "HTTP/1.1 400 Bad Request\r\n"
                           "Content-Type: text/plain\r\n"
                           "Content-Length: 0\r\n"
                           "Connection: close\r\n"
                           +corsHeaders+"\r\n";
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
        return;
    }

    if(path != "/api/post"){

        QString responseBody = "Not Found";
        QString response = QString("HTTP/1.1 404 Not Found\r\n"
                                   "Content-Type: text/plain\r\n"
                                   "Content-Length: %1\r\n"
                                   "Connection: close\r\n"
                                   +corsHeaders+"\r\n%2")
                              .arg(responseBody.length())
                              .arg(responseBody);
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
        return;
    }

    QJsonObject jsonObj = jsonDoc.object();
    QString name = jsonObj.value("name").toString("Guest");

    // 构建响应
    QString responseBody = QString("{\"message\": \"Hello, %1!\"}").arg(name);
    QString response = QString("HTTP/1.1 200 OK\r\n"
                               "Content-Type: application/json\r\n"
                               "Content-Length: %1\r\n"
                               "Connection: close\r\n"
                               +corsHeaders+"\r\n%2")
                          .arg(responseBody.length())
                          .arg(responseBody);

    // 发送响应
    socket->write(response.toUtf8());
    socket->flush();
    socket->disconnectFromHost();
}

```

main函数中启动

``` cpp
#include "mainwindow.h"
#include <QApplication>
#include "httpserver.h"

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    quint16 port = 8080; // 定义监听端口
    HttpServer server(port);

    if (!server.start()) {
        return -1;
    }

    MainWindow mw;
    mw.show();
    return a.exec();
}

```

我们在浏览器中分别输入不同的路由，发送get请求给服务器

比如发送`localhost:8080/api/hello`



![https://cdn.llfc.club/1728466924724.jpg](https://cdn.llfc.club/1728466924724.jpg)

或者访问根目录`localhost:8080`

![https://cdn.llfc.club/1728467090225.jpg](https://cdn.llfc.club/1728467090225.jpg)

点击教案文件夹内的index.html，输入姓名，点击发送按钮，能收到服务器回馈的json格式的数据

![https://cdn.llfc.club/1728467399858.jpg](https://cdn.llfc.club/1728467399858.jpg)

### HttpServer优化

**多线程模式**

我们之前实现的httpserver是单线程模式，同一时刻只能处理一个请求，为了提升并发能力，我们可以改为多线程模式，在收到连接后，我们为新的连接创建一个新的线程处理读写

httpserver简化

``` cpp
#ifndef HTTPSERVER_H
#define HTTPSERVER_H

#include <QObject>
#include <QTcpServer>
#include <QTcpSocket>
#include <QJsonDocument>

class HttpServer : public QObject
{
    Q_OBJECT
public:
    explicit HttpServer(quint16 port, QObject *parent = nullptr);
    bool start();


private slots:
    // 新连接建立触发
    void onNewConnection();

    // 断开连接触发的槽函数
    void onDisconnected();

private:
    QTcpServer *tcpServer;
    quint16 listenPort;


};

#endif // HTTPSERVER_H

```

HttpServer具体实现

``` cpp
#include "httpserver.h"
#include <QDebug>
#include <QJsonDocument>
#include <QJsonObject>
#include <QThread>
#include "clienthandler.h"

HttpServer::HttpServer(quint16 port, QObject *parent)
    : QObject(parent), listenPort(port)
{
    tcpServer = new QTcpServer(this);
    connect(tcpServer, &QTcpServer::newConnection, this, &HttpServer::onNewConnection);
}

bool HttpServer::start()
{
    if (!tcpServer->listen(QHostAddress::Any, listenPort)) {
        qCritical() << "无法启动服务器:" << tcpServer->errorString();
        return false;
    }
    qDebug() << "HTTP服务器已启动，监听端口" << listenPort;
    return true;
}

void HttpServer::onNewConnection()
{
    while (tcpServer->hasPendingConnections()) {
        QTcpSocket *clientSocket = tcpServer->nextPendingConnection();
        qDebug() << "新的连接来自" << clientSocket->peerAddress().toString() << ":" << clientSocket->peerPort();

        // 创建一个新的线程
            QThread *thread = new QThread;

            ClientHandler *handler = new ClientHandler(clientSocket);
            //没有父节点的对象才可移动到其他线程
            clientSocket->setParent(nullptr);
            //需要将对象移动到子线程中
            clientSocket->moveToThread(thread);
            handler->moveToThread(thread);

            connect(thread, &QThread::started, handler, &ClientHandler::process);
            connect(handler, &ClientHandler::finished, thread, &QThread::quit);
            connect(handler, &ClientHandler::finished, handler, &ClientHandler::deleteLater);
            connect(thread, &QThread::finished, thread, &QThread::deleteLater);

            thread->start();
    }
}

//断开连接
void HttpServer::onDisconnected()
{
    QTcpSocket *clientSocket = qobject_cast<QTcpSocket*>(sender());
    if (clientSocket) {
        qDebug() << "连接断开：" << clientSocket->peerAddress().toString() << ":" << clientSocket->peerPort();
        clientSocket->deleteLater();
    }
}
```

优化clienthandler

``` cpp
#ifndef CLIENTHANDLER_H
#define CLIENTHANDLER_H

#include <QObject>
#include <QTcpSocket>
class HttpServer;
class ClientHandler : public QObject
{
    Q_OBJECT
public:
    explicit ClientHandler(QTcpSocket *socket, QObject *parent = nullptr);
    ~ ClientHandler();
    void process();

signals:
    void finished();

private slots:
    void onReadyRead();
    void onDisconnected();

private:
    QTcpSocket *clientSocket;
    HttpServer* _hs;

    // 简单的请求处理方法
    void handleRequest(const QString &request);
    //处理post请求
    void handlePostRequest(const QString &path, const QString &bodyPart);


};

#endif // CLIENTHANDLER_H

```

clienthandler具体实现

``` cpp
#include "clienthandler.h"
#include <QDebug>
#include <QHostAddress>
#include "httpserver.h"
#include <QJsonObject>
#include "global.h"

ClientHandler::ClientHandler(QTcpSocket *socket, QObject *parent)
    : QObject(parent), clientSocket(socket)
{
    connect(clientSocket, &QTcpSocket::readyRead, this, &ClientHandler::onReadyRead);
    connect(clientSocket, &QTcpSocket::disconnected, this, &ClientHandler::onDisconnected);
    registerRoutes();
}

ClientHandler::~ClientHandler()
{

}

void ClientHandler::process()
{
    // 可以在此处进行初始化操作
}

void ClientHandler::onReadyRead()
{
    QByteArray requestData = clientSocket->readAll();
    QString requestString(requestData);
    qDebug() << "收到请求：" << requestString;

    handleRequest(requestString);
}

void ClientHandler::onDisconnected()
{
    qDebug() << "连接断开：" << clientSocket->peerAddress().toString() << ":" << clientSocket->peerPort();
    clientSocket->deleteLater();
    emit finished();
}

void ClientHandler::handlePostRequest(const QString &path, const QString &bodyPart)
{
    // 添加 CORS 头
    QString corsHeaders = "Access-Control-Allow-Origin: *\r\n" // 允许所有来源
                          "Access-Control-Allow-Methods: GET, POST, OPTIONS\r\n" // 允许的方法
                          "Access-Control-Allow-Headers: Content-Type\r\n"; // 允许的请求头
    // 解析JSON体
    QJsonDocument jsonDoc = QJsonDocument::fromJson(bodyPart.toUtf8());
    if (!jsonDoc.isObject()) {
        QString response = "HTTP/1.1 400 Bad Request\r\n"
                           "Content-Type: text/plain\r\n"
                           "Content-Length: 0\r\n"
                           "Connection: close\r\n"
                           +corsHeaders+"\r\n";
        clientSocket->write(response.toUtf8());
        clientSocket->flush();
        clientSocket->disconnectFromHost();
        return;
    }

    //判断路由是否存在
    if(!routesPost.contains(path)){
        QString responseBody = "Not Found";
        QString response = QString("HTTP/1.1 404 Not Found\r\n"
                                   "Content-Type: text/plain\r\n"
                                   "Content-Length: %1\r\n"
                                   "Connection: close\r\n"
                                   +corsHeaders+"\r\n%2")
                              .arg(responseBody.length())
                              .arg(responseBody);
        clientSocket->write(response.toUtf8());
        clientSocket->flush();
        clientSocket->disconnectFromHost();
        return;
    }

    //处理请求
    routesPost[path](clientSocket,jsonDoc);
}



// 修改 handleRequest 方法以调用 handlePostRequest
void ClientHandler::handleRequest(const QString &request)
{
    // 解析请求行
    QStringList requestLines = request.split("\r\n");
    if (requestLines.isEmpty()) {
        // 无效请求
        return;
    }

    QString requestLine = requestLines.at(0);
    QStringList requestParts = requestLine.split(" ");
    if (requestParts.size() < 3) {
        // 无效请求行
        return;
    }

    QString method = requestParts.at(0);
    QString path = requestParts.at(1);
    QString httpVersion = requestParts.at(2);

    // 添加 CORS 头, 支持跨域访问
    QString corsHeaders = "Access-Control-Allow-Origin: *\r\n" // 允许所有来源
                          "Access-Control-Allow-Methods: GET, POST, OPTIONS\r\n" // 允许的方法
                          "Access-Control-Allow-Headers: Content-Type\r\n"; // 允许的请求头

    if (method == "OPTIONS") {
        // 处理预检请求
        QString response = "HTTP/1.1 204 No Content\r\n"
                           "Connection: close\r\n"
                           + corsHeaders + "\r\n";
        clientSocket->write(response.toUtf8());
        clientSocket->flush();
        clientSocket->disconnectFromHost();
        return;
    }

    if (method == "GET") {

        if(!routesGet.contains(path)){
            // 处理404
            QString body = "404 - Not Found\n";
            QString response = QString("HTTP/1.1 404 Not Found\r\n"
                                       "Content-Type: text/plain\r\n"
                                       "Content-Length: %1\r\n"
                                       "Connection: close\r\n"
                                       + corsHeaders + "\r\n%2")
                                  .arg(body.length())
                                  .arg(body);
            clientSocket->write(response.toUtf8());
            clientSocket->flush();
            clientSocket->disconnectFromHost();
            return;
        }

        routesGet[path](clientSocket,request);
    }
    else if (method == "POST") {
        QString bodyPart = requestLines.at(requestLines.length()-1);

        // 处理POST请求
        handlePostRequest(path, bodyPart);
    }
    else {
        // 不支持的方法
        QString response = "HTTP/1.1 501 Not Implemented\r\n"
                           "Content-Length: 0\r\n"
                           "Connection: close\r\n"
                           + corsHeaders + "\r\n";
        clientSocket->write(response.toUtf8());
        clientSocket->flush();
        clientSocket->disconnectFromHost();
        return;
    }
}
```

新增global.h和global.cpp

``` cpp
#ifndef GLOBAL_H
#define GLOBAL_H

#include <QObject>
#include <functional>
#include <QTcpSocket>

  //注册路由
extern   void registerRoutes();
//存储get和post路由
extern QMap<QString, std::function<void(QTcpSocket*, const QString&)>> routesGet;
extern QMap<QString, std::function<void(QTcpSocket*, const QJsonDocument &)>> routesPost;

#endif // GLOBAL_H

```

gloal.cpp

``` cpp
#include "global.h"
#include <QJsonDocument>
#include <QJsonObject>

//注册路由
void registerRoutes(){
    // 添加 CORS 头, 支持跨域访问
    QString corsHeaders = "Access-Control-Allow-Origin: *\r\n" // 允许所有来源
                          "Access-Control-Allow-Methods: GET, POST, OPTIONS\r\n" // 允许的方法
                          "Access-Control-Allow-Headers: Content-Type\r\n"; // 允许的请求头

    //注册路由和回调函数，写入map
    routesGet["/"] = [=](QTcpSocket *socket, const QString &request){
        Q_UNUSED(request);
        QString body = "欢迎使用Qt 5.12 创建的简单HTTP服务器！\n";
        QString response = QString("HTTP/1.1 200 OK\r\n"
                                   "Content-Type: text/plain; charset=utf-8\r\n"
                                   "Content-Length: %1\r\n"
                                   "Connection: close\r\n"
                                   + corsHeaders + "\r\n%2")
                              .arg(body.length())
                              .arg(body);
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
    };

    //注册路由和回调函数
    routesGet["/api/hello"] = [=](QTcpSocket *socket, const QString &request){
         Q_UNUSED(request);

         QString body = "{\"message\": \"Hello, World!\"}\n";
         QString response = QString("HTTP/1.1 200 OK\r\n"
                                   "Content-Type: application/json\r\n"
                                   "Content-Length: %1\r\n"
                                   "Connection: close\r\n"
                                   + corsHeaders + "\r\n%2")
                              .arg(body.length())
                              .arg(body);
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
    };

    //注册post请求
    routesPost["/api/post"] = [=](QTcpSocket *socket,
            const QJsonDocument& jsonDoc){
        //解析document
        QJsonObject jsonObj = jsonDoc.object();
        QString name = jsonObj.value("name").toString("Guest");

        // 构建响应
        QString responseBody = QString("{\"message\": \"Hello, %1!\"}").arg(name);
        QString response = QString("HTTP/1.1 200 OK\r\n"
                                   "Content-Type: application/json\r\n"
                                   "Content-Length: %1\r\n"
                                   "Connection: close\r\n"
                                   +corsHeaders+"\r\n%2")
                              .arg(responseBody.length())
                              .arg(responseBody);

        // 发送响应
        socket->write(response.toUtf8());
        socket->flush();
        socket->disconnectFromHost();
    };
}

//存储get和post路由

QMap<QString, std::function<void(QTcpSocket*, const QString&)>> routesGet;

QMap<QString, std::function<void(QTcpSocket*, const QJsonDocument &)>> routesPost;

```

main函数中添加调用

``` cpp
#include "mainwindow.h"
#include <QApplication>
#include "httpserver.h"

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    quint16 port = 8080; // 定义监听端口
    HttpServer server(port);

    if (!server.start()) {
        return -1;
    }

    MainWindow mw;
    mw.show();
    return a.exec();
}
```

### 发送http请求

Qt 的网络模块 (`QtNetwork`) 提供了一组高级 API，用于处理网络通信，包括 HTTP、FTP 等协议。对于 HTTP 客户端功能，`QNetworkAccessManager` 是核心类，配合 `QNetworkRequest` 和 `QNetworkReply` 使用，可以方便地发送各种 HTTP 请求并处理响应。

关键特点



- **异步操作**：所有网络请求都是异步的，不会阻塞主线程。
- **信号与槽机制**：使用 Qt 的信号与槽机制，轻松处理请求完成、错误等事件。
- **支持多种协议**：不仅支持 HTTP，还支持 HTTPS、FTP 等。

### 主要类介绍

**`QNetworkAccessManager`**



负责管理网络请求，可以发送 GET、POST、PUT、DELETE 等 HTTP 请求。



**常用方法：**



- `get(const QNetworkRequest &request)`
- `post(const QNetworkRequest &request, const QByteArray &data)`
- `put(const QNetworkRequest &request, const QByteArray &data)`
- `deleteResource(const QNetworkRequest &request)`



**`QNetworkRequest`**



表示网络请求，主要包含请求的 URL、请求头等信息。



**常用方法：**



- `setHeader(QNetworkRequest::KnownHeaders header, const QVariant &value)`
- `setRawHeader(const QByteArray &headerName, const QByteArray &headerValue)`



**`QNetworkReply`**



表示网络响应，包含响应数据、状态码等信息。通常与信号 `finished()`、`readyRead()`、`errorOccurred()` 等配合使用。



### 发送 GET 请求



``` cpp
#include "mainwindow.h"
#include <QApplication>
#include <QNetworkAccessManager>
#include <QNetworkReply>

// 创建网络访问管理器

QNetworkAccessManager manager;

void get_req(QString url_req){
    // 创建请求对象
    QUrl url(url_req);
    QNetworkRequest request(url);

    // 发送 GET 请求
    QNetworkReply *reply = manager.get(request);

    // 连接请求完成的信号
    QObject::connect(reply, &QNetworkReply::finished, [=]() {
        if (reply->error() == QNetworkReply::NoError) {
            // 读取响应数据
            QByteArray responseData = reply->readAll();
            qDebug() << "GET 响应数据:" << QString::fromUtf8(responseData);
        } else {
            // 输出错误信息
            qDebug() << "错误:" << reply->errorString();
        }
        reply->deleteLater();
    });

}

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    get_req("http://localhost:8080");
    MainWindow mw;
    mw.show();
    return a.exec();
}
```

**解释：**



1. **创建 `QNetworkAccessManager` 实例**：用于管理网络请求。
2. **创建 `QNetworkRequest` 对象**：指定请求的 URL。
3. **发送 GET 请求**：调用 `manager.get(request)` 发送请求，返回一个 `QNetworkReply` 对象。
4. **连接信号**：通过连接 `finished` 信号，处理响应或错误。
5. **读取响应数据**：如果没有错误，读取并输出响应数据。



GET 请求用于从服务器获取数据，通常不会带有请求体。

### 发送 POST 请求



POST 请求用于向服务器发送数据，通常包含请求体（例如 JSON 数据）。

``` cpp
#include <QCoreApplication>
#include <QNetworkAccessManager>
#include <QNetworkRequest>
#include <QNetworkReply>
#include <QUrl>
#include <QDebug>
#include <QJsonDocument>
#include <QJsonObject>

void post_req(QString url_req, QJsonObject json){
    // 创建请求对象
        QUrl url(url_req);
        QNetworkRequest request(url);

        // 设置请求头，例如内容类型为 JSON
        request.setHeader(QNetworkRequest::ContentTypeHeader, "application/json");

        // 转为json对象为json文档
        QJsonDocument jsonDoc(json);
        // 转成字节流数组
        QByteArray jsonData = jsonDoc.toJson();

        // 发送 POST 请求
        QNetworkReply *reply = manager.post(request, jsonData);

        // 连接请求完成的信号
        QObject::connect(reply, &QNetworkReply::finished, [=]() {
            if (reply->error() == QNetworkReply::NoError) {
                // 读取响应数据
                QByteArray responseData = reply->readAll();
                qDebug() << "POST 响应数据:" << responseData;
            } else {
                // 输出错误信息
                qDebug() << "错误:" << reply->errorString();
            }
            reply->deleteLater();
        });
}

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    //构造json数据
    QJsonObject jsonobj;
    jsonobj["name"] = "zack";
    post_req("http://localhost:8080/api/post",jsonobj);
    MainWindow mw;
    mw.show();
    return a.exec();
}
```

**解释：**



1. **设置请求头**：指定内容类型为 `application/json`。
2. **构建 JSON 数据**：使用 `QJsonObject` 和 `QJsonDocument` 构建 JSON 格式的请求体。
3. **发送 POST 请求**：调用 `manager.post(request, jsonData)`，将 JSON 数据作为请求体发送。
4. **处理响应**：与 GET 请求类似，通过信号处理响应或错误。



### 处理响应与错误



在上述示例中，通过连接 `finished` 信号来处理响应。除了 `finished` 信号外，还可以连接其他信号来实时处理数据或错误。



**常用信号**



- **`readyRead()`**：当有新的数据可读时触发，可以用来逐步读取响应数据。
- **`errorOccurred(QNetworkReply::NetworkError code)`**：当发生错误时触发，提供错误类型。

``` cpp
void get_req_error(QString url_req){
    // 创建请求对象
    QUrl url(url_req);
    QNetworkRequest request(url);

    // 发送 GET 请求
    QNetworkReply *reply = manager.get(request);

    // 连接请求完成的信号
    QObject::connect(reply, &QNetworkReply::finished, [=]() {
        if (reply->error() == QNetworkReply::NoError) {
            // 读取响应数据
            QByteArray responseData = reply->readAll();
            qDebug() << "GET 响应数据:" << QString::fromUtf8(responseData);
        } else {
            // 输出错误信息
            qDebug() << "错误:" << reply->errorString();
        }
        reply->deleteLater();
    });

    // 连接错误信号
        QObject::connect(reply, QOverload<QNetworkReply::NetworkError>::of(&QNetworkReply::error),
                         [&](QNetworkReply::NetworkError code){
            qDebug() << "发生错误，错误码:" << code << "错误信息:" << reply->errorString();

        });
}
```

**说明：**



1. **连接 `errorOccurred` 信号**：当发生网络错误时，输出错误码和错误信息。
2. **故意使用无效 URL**：触发错误，演示错误处理。



# 第十二章 多媒体

## Qt  多媒体框架概述



Qt 5.12 提供了一套强大的多媒体框架，支持音频和视频的播放、录制、处理等功能。该框架主要由以下模块组成：



- **Qt Multimedia**：核心模块，提供音视频的播放与录制功能。
- **Qt Multimedia Widgets**：基于 Widgets 的多媒体控件，如 `QVideoWidget`。
- **Qt Quick Multimedia**：基于 QML 的多媒体功能，适用于 Qt Quick 应用。

### 主要功能



- **音频播放**：支持多种音频格式，如 MP3、WAV 等。
- **视频播放**：支持多种视频格式，能够嵌入到应用程序界面中。
- **音视频录制**：支持音频和视频的录制功能。
- **摄像头访问**：访问和控制摄像头设备。
- **音频效果与处理**：提供音频效果处理的接口，如均衡器、混响等。

## 关键类与组件



在 Qt 5.12 中进行音视频播放，主要涉及以下类和组件：



### QMediaPlayer



`QMediaPlayer` 是 Qt 中最核心的类，用于管理和控制媒体的播放。它支持多种媒体格式和协议。



**主要功能：**



- 播放、暂停、停止媒体文件。
- 设置媒体源（本地文件或网络流）。
- 控制音量、播放速度等。
- 处理媒体状态变化的信号。



### QVideoWidget



`QVideoWidget` 是一个基于 Widgets 的控件，用于显示视频画面。它与 `QMediaPlayer` 配合使用，实现视频的可视化播放。



### QMediaPlaylist



`QMediaPlaylist` 用于管理媒体播放列表，支持播放列表的添加、删除、排序等操作。它与 `QMediaPlayer` 集成，实现顺序播放、循环播放等功能。



### QAudioOutput



虽然 `QAudioOutput` 是 Qt 6 引入的类，但在 Qt 5.12 中，音量控制通过 `QMediaPlayer` 提供的接口实现，无需使用 `QAudioOutput`。



### QSound



`QSound` 是一个简单的类，用于播放短音效。适用于简单的音频播放需求，但不适合复杂的音频控制。

## 项目配置



在项目的 `.pro` 文件中添加必要的模块支持。



**示例 `.pro` 文件**

``` cpp
QT += core gui multimedia multimediawidgets

greaterThan(QT_MAJOR_VERSION, 4): QT += widgets

TARGET = MediaPlayerDemo
TEMPLATE = app

SOURCES += main.cpp
```

**确保 Qt 的多媒体模块正确安装，并且能够支持所需的音视频格式。某些平台可能需要安装额外的编解码器。**



## 基础音频播放示例

以下示例展示如何使用 `QMediaPlayer` 类播放一个音频文件。

![https://cdn.llfc.club/1728548980543.jpg](https://cdn.llfc.club/1728548980543.jpg)

### 1 示例代码



```cpp
// main.cpp
#include <QApplication>
#include <QWidget>
#include <QPushButton>
#include <QVBoxLayout>
#include <QMediaPlayer>
#include <QFileDialog>
#include <QHBoxLayout>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    // 创建主窗口
    QWidget window;
    window.setWindowTitle("Qt 音频播放示例");
    window.resize(300, 150);

    // 创建布局
    QVBoxLayout *mainLayout = new QVBoxLayout(&window);

    // 创建播放控制按钮
    QPushButton *playButton = new QPushButton("播放");
    QPushButton *pauseButton = new QPushButton("暂停");
    QPushButton *stopButton = new QPushButton("停止");
    QPushButton *openButton = new QPushButton("打开文件");

    QHBoxLayout *controlLayout = new QHBoxLayout;
    controlLayout->addWidget(playButton);
    controlLayout->addWidget(pauseButton);
    controlLayout->addWidget(stopButton);
    controlLayout->addWidget(openButton);

    mainLayout->addLayout(controlLayout);

    // 创建QMediaPlayer实例
    QMediaPlayer *player = new QMediaPlayer(&window);

    // 连接打开文件按钮
    QObject::connect(openButton, &QPushButton::clicked, [&](){
        QString fileName = QFileDialog::getOpenFileName(&window, "选择音频文件", "", "音频文件 (*.mp3 *.wav *.ogg)");
        if (!fileName.isEmpty()) {
            player->setMedia(QUrl::fromLocalFile(fileName));
        }
    });

    // 连接播放按钮
    QObject::connect(playButton, &QPushButton::clicked, player, &QMediaPlayer::play);

    // 连接暂停按钮
    QObject::connect(pauseButton, &QPushButton::clicked, player, &QMediaPlayer::pause);

    // 连接停止按钮
    QObject::connect(stopButton, &QPushButton::clicked, player, &QMediaPlayer::stop);

    // 显示窗口
    window.show();

    return app.exec();
}
```



### 2 代码说明



1. **创建主窗口和布局**：使用 `QWidget` 和 `QVBoxLayout` 创建简易的用户界面。

2. **创建播放控制按钮**：包含“播放”、“暂停”、“停止”和“打开文件”四个按钮。

3. **创建 `QMediaPlayer` 实例**：用于音频播放控制。

4. 连接信号与槽

   ：

   - `openButton` 用于选择音频文件并设置为播放源。
   - `playButton` 连接到 `QMediaPlayer::play` 方法，开始播放。
   - `pauseButton` 连接到 `QMediaPlayer::pause` 方法，暂停播放。
   - `stopButton` 连接到 `QMediaPlayer::stop` 方法，停止播放。

5. **运行应用程序**：启动应用程序的主事件循环。



### 3 运行效果



运行程序后，点击“打开文件”按钮选择一个音频文件，然后点击“播放”按钮开始播放音频。可以通过“暂停”和“停止”按钮控制播放状态。

![https://cdn.llfc.club/1728548980543.jpg](https://cdn.llfc.club/1728548980543.jpg)



##  基础视频播放示例



以下示例展示如何使用 `QMediaPlayer` 和 `QVideoWidget` 类播放一个视频文件。

![https://cdn.llfc.club/1728553459280.jpg](https://cdn.llfc.club/1728553459280.jpg)

### 1 示例代码



```cpp
// main.cpp
#include <QApplication>
#include <QWidget>
#include <QPushButton>
#include <QVBoxLayout>
#include <QMediaPlayer>
#include <QVideoWidget>
#include <QFileDialog>
#include <QHBoxLayout>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    // 创建主窗口
    QWidget window;
    window.setWindowTitle("Qt 视频播放示例");
    window.resize(800, 600);

    // 创建布局
    QVBoxLayout *mainLayout = new QVBoxLayout(&window);

    // 创建视频显示控件
    QVideoWidget *videoWidget = new QVideoWidget;
    mainLayout->addWidget(videoWidget);

    // 创建播放控制按钮
    QPushButton *playButton = new QPushButton("播放");
    QPushButton *pauseButton = new QPushButton("暂停");
    QPushButton *stopButton = new QPushButton("停止");
    QPushButton *openButton = new QPushButton("打开文件");

    QHBoxLayout *controlLayout = new QHBoxLayout;
    controlLayout->addWidget(playButton);
    controlLayout->addWidget(pauseButton);
    controlLayout->addWidget(stopButton);
    controlLayout->addWidget(openButton);

    mainLayout->addLayout(controlLayout);

    // 创建QMediaPlayer实例
    QMediaPlayer *player = new QMediaPlayer(&window);
    player->setVideoOutput(videoWidget);

    // 连接打开文件按钮
    QObject::connect(openButton, &QPushButton::clicked, [&](){
        QString fileName = QFileDialog::getOpenFileName(&window, "选择视频文件", "",
                                  "视频文件 (*.mp4 *.avi *.mkv *.mov)");
        if (!fileName.isEmpty()) {
            player->setMedia(QUrl::fromLocalFile(fileName));
            player->play(); // 自动开始播放
        }
    });

    // 连接错误信息
    QObject::connect(player, QOverload<QMediaPlayer::Error>::of(&QMediaPlayer::error),
        [&](QMediaPlayer::Error error){
            qDebug() << "播放错误：" << player->errorString();
        });

    // 连接播放按钮
    QObject::connect(playButton, &QPushButton::clicked, player, &QMediaPlayer::play);

    // 连接暂停按钮
    QObject::connect(pauseButton, &QPushButton::clicked, player, &QMediaPlayer::pause);

    // 连接停止按钮
    QObject::connect(stopButton, &QPushButton::clicked, player, &QMediaPlayer::stop);

    // 显示窗口
    window.show();

    return app.exec();
}

```

上述代码运行报错

![https://cdn.llfc.club/1728551340552.jpg](https://cdn.llfc.club/1728551340552.jpg)

原因：QT使用windows默认解码器，如果没有安装有相关DirectShowService解码器，则运行程序也是没法播放视频的，必须安装相关directshow解码器，安装位置在你的[qt安装](https://so.csdn.net/so/search?q=qt安装&spm=1001.2101.3001.7020)目录。

LAVFilter解码器下载地址

[https://github.com/Nevcairiel/LAVFilters/releases](https://github.com/Nevcairiel/LAVFilters/releases)

下载installer.exe安装

安装目录选择Qt目录

![https://cdn.llfc.club/1728551858158.jpg](https://cdn.llfc.club/1728551858158.jpg)

接着按照默认配置无脑安装即可。

安装完成后重启下电脑



### 2 代码说明



1. **创建视频显示控件**：使用 `QVideoWidget` 作为视频内容的显示区域。

2. **创建播放控制按钮**：包含“播放”、“暂停”、“停止”和“打开文件”四个按钮。

3. **创建 `QMediaPlayer` 实例**：用于视频播放控制，并将视频输出设置为 `QVideoWidget`。

4. 连接信号与槽

   ：

   - `openButton` 用于选择视频文件并设置为播放源。
   - `playButton` 连接到 `QMediaPlayer::play` 方法，开始播放视频。
   - `pauseButton` 连接到 `QMediaPlayer::pause` 方法，暂停播放视频。
   - `stopButton` 连接到 `QMediaPlayer::stop` 方法，停止播放视频。

5. **运行应用程序**：启动应用程序的主事件循环。



### 3 运行效果

![https://cdn.llfc.club/1728553459280.jpg](https://cdn.llfc.club/1728553459280.jpg)

运行程序后，点击“打开文件”按钮选择一个视频文件，然后点击“播放”按钮开始播放视频。可以通过“暂停”和“停止”按钮控制播放状态。



> **注意**：确保所选视频文件的编码格式被 Qt 支持，必要时安装相应的编解码器。



## 进阶功能实现



在掌握了基础的音视频播放后，可以进一步实现一些进阶功能，如更丰富的播放控制、播放列表管理、音量控制和错误处理等。



### 播放控制



实现更丰富的播放控制功能，如快进、快退、跳转到指定时间等。

![https://cdn.llfc.club/1728555991936.jpg](https://cdn.llfc.club/1728555991936.jpg)

示例代码



```cpp
// main.cpp
#include <QApplication>
#include <QWidget>
#include <QPushButton>
#include <QSlider>
#include <QLabel>
#include <QVBoxLayout>
#include <QHBoxLayout>
#include <QMediaPlayer>
#include <QVideoWidget>
#include <QFileDialog>
#include <QTime>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    // 创建主窗口
    QWidget window;
    window.setWindowTitle("Qt 高级视频播放示例");
    window.resize(800, 600);

    // 创建布局
    QVBoxLayout *mainLayout = new QVBoxLayout(&window);

    // 创建视频显示控件
    QVideoWidget *videoWidget = new QVideoWidget;
    videoWidget->setFixedHeight(400);
    mainLayout->addWidget(videoWidget);
    videoWidget->setStyleSheet("background-color: black;");

    // 创建播放控制按钮
    QPushButton *openButton = new QPushButton("打开文件");
    QPushButton *playButton = new QPushButton("播放");
    QPushButton *pauseButton = new QPushButton("暂停");
    QPushButton *stopButton = new QPushButton("停止");
    QPushButton *forwardButton = new QPushButton("快进 10 秒");
    QPushButton *backwardButton = new QPushButton("快退 10 秒");

    QHBoxLayout *controlLayout = new QHBoxLayout;
    controlLayout->addWidget(openButton);
    controlLayout->addWidget(playButton);
    controlLayout->addWidget(pauseButton);
    controlLayout->addWidget(stopButton);
    controlLayout->addWidget(backwardButton);
    controlLayout->addWidget(forwardButton);

    mainLayout->addLayout(controlLayout);

    // 创建进度条和时间标签
    QSlider *positionSlider = new QSlider(Qt::Horizontal);
    positionSlider->setRange(0, 0);
    QLabel *currentTimeLabel = new QLabel("00:00");
    QLabel *totalTimeLabel = new QLabel("00:00");

    QHBoxLayout *sliderLayout = new QHBoxLayout;
    sliderLayout->addWidget(currentTimeLabel);
    sliderLayout->addWidget(positionSlider);
    sliderLayout->addWidget(totalTimeLabel);

    mainLayout->addLayout(sliderLayout);

    // 创建QMediaPlayer实例
    QMediaPlayer *player = new QMediaPlayer(&window);
    player->setVideoOutput(videoWidget);

    // 连接打开文件按钮
    QObject::connect(openButton, &QPushButton::clicked, [&](){
        QString fileName = QFileDialog::getOpenFileName(&window, "选择视频文件", "", "视频文件 (*.mp4 *.avi *.mkv *.mov)");
        if (!fileName.isEmpty()) {
            player->setMedia(QUrl::fromLocalFile(fileName));
             player->pause();
        }
    });

    // 连接播放按钮
    QObject::connect(playButton, &QPushButton::clicked, player, &QMediaPlayer::play);

    // 连接暂停按钮
    QObject::connect(pauseButton, &QPushButton::clicked, player, &QMediaPlayer::pause);

    // 连接停止按钮
    QObject::connect(stopButton, &QPushButton::clicked, player, &QMediaPlayer::stop);

    // 连接快进按钮
    QObject::connect(forwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        qint64 duration = player->duration();
        player->setPosition(qMin(current + 10000, duration));
    });

    // 连接快退按钮
    QObject::connect(backwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        player->setPosition(qMax(current - 10000, 0LL));
    });

    // 更新进度条和时间标签
    QObject::connect(player, &QMediaPlayer::positionChanged, [&](qint64 position){
        positionSlider->setValue(position);
        QTime currentTime(0, (position / 60000) % 60, (position / 1000) % 60);
        currentTimeLabel->setText(currentTime.toString("mm:ss"));
    });

    QObject::connect(player, &QMediaPlayer::durationChanged, [&](qint64 duration){
        positionSlider->setRange(0, duration);
        QTime totalTime(0, (duration / 60000) % 60, (duration / 1000) % 60);
        totalTimeLabel->setText(totalTime.toString("mm:ss"));
    });

    // 允许用户通过滑动进度条跳转
    QObject::connect(positionSlider, &QSlider::sliderMoved, [&](int position){
        player->setPosition(position);
    });

    // 显示窗口
    window.show();

    return app.exec();
}

```



#### 代码说明



1. **播放控制按钮**：增加了“快进 10 秒”和“快退 10 秒”按钮，实现音视频的前进和后退功能。

2. 进度条和时间标签

   ：

   - `QSlider` 用于显示和控制媒体播放进度。
   - `QLabel` 显示当前播放时间和总时长。

3. 信号与槽连接

   ：

   - `positionChanged` 信号用于实时更新进度条和当前播放时间。
   - `durationChanged` 信号用于设置进度条的最大值和显示总时长。
   - 通过连接 `QSlider::sliderMoved` 信号，实现用户拖动进度条跳转到指定位置。

4. 快进和快退实现

   ：

   - 快进：当前播放位置加上 10,000 毫秒（10 秒），并确保不超过总时长。
   - 快退：当前播放位置减去 10,000 毫秒（10 秒），并确保不低于 0。

### 播放列表管理



使用 `QMediaPlaylist` 管理多个媒体文件的播放，支持顺序播放、循环播放等模式。



#### 示例代码



```cpp
// main.cpp
#include <QApplication>
#include <QWidget>
#include <QPushButton>
#include <QListWidget>
#include <QVBoxLayout>
#include <QHBoxLayout>
#include <QMediaPlayer>
#include <QMediaPlaylist>
#include <QVideoWidget>
#include <QFileDialog>
#include <QMessageBox>
#include <QLabel>
#include <QTime>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    // 创建主窗口
    QWidget window;
    window.setWindowTitle("Qt 播放列表示例");
    window.resize(800, 600);

    // 创建布局
    QVBoxLayout *mainLayout = new QVBoxLayout(&window);

    // 创建视频显示控件
    QVideoWidget *videoWidget = new QVideoWidget;
    videoWidget->setFixedHeight(600);
    mainLayout->addWidget(videoWidget);
    videoWidget->setStyleSheet("background-color: black;");


    // 创建进度条和时间标签
    QSlider *positionSlider = new QSlider(Qt::Horizontal);
    positionSlider->setRange(0, 0);
    QLabel *currentTimeLabel = new QLabel("00:00");
    QLabel *totalTimeLabel = new QLabel("00:00");

    QHBoxLayout *sliderLayout = new QHBoxLayout;
    sliderLayout->addWidget(currentTimeLabel);
    sliderLayout->addWidget(positionSlider);
    sliderLayout->addWidget(totalTimeLabel);

    mainLayout->addLayout(sliderLayout);

    // 创建播放控制按钮
    QPushButton *addButton = new QPushButton("添加媒体");
    QPushButton *removeButton = new QPushButton("移除媒体");
    QPushButton *playButton = new QPushButton("播放");
    QPushButton *pauseButton = new QPushButton("暂停");
    QPushButton *stopButton = new QPushButton("停止");
    QPushButton *nextButton = new QPushButton("下一首");
    QPushButton *prevButton = new QPushButton("上一首");
    QPushButton *forwardButton = new QPushButton("快进 10 秒");
    QPushButton *backwardButton = new QPushButton("快退 10 秒");

    QHBoxLayout *controlLayout = new QHBoxLayout;
    controlLayout->addWidget(addButton);
    controlLayout->addWidget(removeButton);
    controlLayout->addWidget(playButton);
    controlLayout->addWidget(pauseButton);
    controlLayout->addWidget(stopButton);
    controlLayout->addWidget(prevButton);
    controlLayout->addWidget(nextButton);
    controlLayout->addWidget(backwardButton);
    controlLayout->addWidget(forwardButton);

    mainLayout->addLayout(controlLayout);

    // 创建播放列表视图
    QListWidget *playlistWidget = new QListWidget;
    mainLayout->addWidget(playlistWidget);

    // 创建QMediaPlayer和QMediaPlaylist实例
    QMediaPlayer *player = new QMediaPlayer(&window);
    QMediaPlaylist *playlist = new QMediaPlaylist;
    player->setPlaylist(playlist);
    player->setVideoOutput(videoWidget);

    // 连接添加媒体按钮
    QObject::connect(addButton, &QPushButton::clicked, [&](){
        QStringList files = QFileDialog::getOpenFileNames(&window, "选择媒体文件", "", "音视频文件 (*.wav *.mp4 *.avi *.mkv *.mov)");
        if (!files.isEmpty()) {
            for (const QString &file : files) {
                playlist->addMedia(QUrl::fromLocalFile(file));
                playlistWidget->addItem(file);
            }
        }
    });

    // 连接移除媒体按钮
    QObject::connect(removeButton, &QPushButton::clicked, [&](){
        int currentRow = playlistWidget->currentRow();
        if (currentRow >= 0) {
            playlist->removeMedia(currentRow);
            delete playlistWidget->takeItem(currentRow);
        } else {
            QMessageBox::warning(&window, "移除媒体", "请选择要移除的媒体项目。");
        }
    });

    // 更新进度条和时间标签
    QObject::connect(player, &QMediaPlayer::positionChanged, [&](qint64 position){
        positionSlider->setValue(position);
        QTime currentTime(0, (position / 60000) % 60, (position / 1000) % 60);
        currentTimeLabel->setText(currentTime.toString("mm:ss"));
    });

    QObject::connect(player, &QMediaPlayer::durationChanged, [&](qint64 duration){
        positionSlider->setRange(0, duration);
        QTime totalTime(0, (duration / 60000) % 60, (duration / 1000) % 60);
        totalTimeLabel->setText(totalTime.toString("mm:ss"));
    });

    // 允许用户通过滑动进度条跳转
    QObject::connect(positionSlider, &QSlider::sliderMoved, [&](int position){
        player->setPosition(position);
    });

    // 连接播放按钮
    QObject::connect(playButton, &QPushButton::clicked,  [&]() {
        int currentRow = playlistWidget->currentRow();

        // 如果没有选中项，选择第一个项目
        if (currentRow == -1 && playlist->mediaCount() > 0) {
            currentRow = 0;
            playlistWidget->setCurrentRow(currentRow); // 设置为选中
        }

        // 播放选中的媒体
        if (currentRow >= 0) {
            playlist->setCurrentIndex(currentRow); // 设置播放列表中的当前索引
            player->play();
        } else {
            QMessageBox::warning(&window, "播放", "播放列表为空。");
        }
    });

    // 连接暂停按钮
    QObject::connect(pauseButton, &QPushButton::clicked, player, &QMediaPlayer::pause);

    // 连接停止按钮
    QObject::connect(stopButton, &QPushButton::clicked, player, &QMediaPlayer::stop);

    // 连接下一首按钮
    QObject::connect(nextButton, &QPushButton::clicked, playlist, &QMediaPlaylist::next);

    // 连接上一首按钮
    QObject::connect(prevButton, &QPushButton::clicked, playlist, &QMediaPlaylist::previous);

    // 连接快进按钮
    QObject::connect(forwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        qint64 duration = player->duration();
        player->setPosition(qMin(current + 10000, duration));
    });

    // 连接快退按钮
    QObject::connect(backwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        player->setPosition(qMax(current - 10000, 0LL));
    });


    // 同步播放列表视图与 QMediaPlaylist
    QObject::connect(playlist, &QMediaPlaylist::currentIndexChanged, [&](int index){
        playlistWidget->setCurrentRow(index);
    });

    // 设置播放模式
    // 可选：QMediaPlaylist::Sequential, QMediaPlaylist::Loop, QMediaPlaylist::Random
    playlist->setPlaybackMode(QMediaPlaylist::Loop);

    // 显示窗口
    window.show();

    return app.exec();
}
```



#### 代码说明



1. **播放列表视图**：使用 `QListWidget` 显示当前播放列表中的媒体文件。

2. 添加与移除媒体文件

   ：

   - **添加媒体**：通过 `QFileDialog` 选择多个媒体文件，添加到 `QMediaPlaylist` 和 `QListWidget` 中。
   - **移除媒体**：移除选定的媒体文件。

3. **播放控制按钮**：增加了“下一首”和“上一首”按钮，实现切换媒体功能。

4. **播放模式设置**：通过 `QMediaPlaylist::setPlaybackMode` 设置播放模式，如循环播放。

5. **同步播放列表**：通过连接 `currentIndexChanged` 信号，将 `QMediaPlaylist` 的当前索引与 `QListWidget` 的选择同步。

6. **错误提示**：在移除媒体时，如果没有选中任何项目，会弹出警告提示框。



### 音量控制



通过 `QMediaPlayer` 提供的音量控制接口，实现音量的调整。

![https://cdn.llfc.club/1728560295385.jpg](https://cdn.llfc.club/1728560295385.jpg)



#### 示例代码



```cpp
// main.cpp
#include <QApplication>
#include <QWidget>
#include <QPushButton>
#include <QListWidget>
#include <QVBoxLayout>
#include <QHBoxLayout>
#include <QMediaPlayer>
#include <QMediaPlaylist>
#include <QVideoWidget>
#include <QFileDialog>
#include <QMessageBox>
#include <QLabel>
#include <QTime>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    // 创建主窗口
    QWidget window;
    window.setWindowTitle("Qt 播放列表示例");
    window.resize(800, 600);

    // 创建布局
    QVBoxLayout *mainLayout = new QVBoxLayout(&window);

    // 创建视频显示控件
    QVideoWidget *videoWidget = new QVideoWidget;
    videoWidget->setFixedHeight(600);
    mainLayout->addWidget(videoWidget);
    videoWidget->setStyleSheet("background-color: black;");


    // 创建进度条和时间标签
    QSlider *positionSlider = new QSlider(Qt::Horizontal);
    positionSlider->setRange(0, 0);
    QLabel *currentTimeLabel = new QLabel("00:00");
    QLabel *totalTimeLabel = new QLabel("00:00");

    QHBoxLayout *sliderLayout = new QHBoxLayout;
    sliderLayout->addWidget(currentTimeLabel);
    sliderLayout->addWidget(positionSlider);
    sliderLayout->addWidget(totalTimeLabel);

    mainLayout->addLayout(sliderLayout);

    // 创建播放控制按钮
    QPushButton *addButton = new QPushButton("添加媒体");
    QPushButton *removeButton = new QPushButton("移除媒体");
    QPushButton *playButton = new QPushButton("播放");
    QPushButton *pauseButton = new QPushButton("暂停");
    QPushButton *stopButton = new QPushButton("停止");
    QPushButton *nextButton = new QPushButton("下一首");
    QPushButton *prevButton = new QPushButton("上一首");
    QPushButton *forwardButton = new QPushButton("快进 10 秒");
    QPushButton *backwardButton = new QPushButton("快退 10 秒");

    QHBoxLayout *controlLayout = new QHBoxLayout;
    controlLayout->addWidget(addButton);
    controlLayout->addWidget(removeButton);
    controlLayout->addWidget(playButton);
    controlLayout->addWidget(pauseButton);
    controlLayout->addWidget(stopButton);
    controlLayout->addWidget(prevButton);
    controlLayout->addWidget(nextButton);
    controlLayout->addWidget(backwardButton);
    controlLayout->addWidget(forwardButton);

    mainLayout->addLayout(controlLayout);
    // 创建音量控制滑块和标签
    QLabel *volumeLabel = new QLabel("音量:");
    QSlider *volumeSlider = new QSlider(Qt::Horizontal);
    volumeSlider->setRange(0, 100);
    volumeSlider->setValue(50); // 默认音量为50%

    QLabel *volumeValueLabel = new QLabel("50%");

    QHBoxLayout *volumeLayout = new QHBoxLayout;
    volumeLayout->addWidget(volumeLabel);
    volumeLayout->addWidget(volumeSlider);
    volumeLayout->addWidget(volumeValueLabel);

    mainLayout->addLayout(volumeLayout);

    // 创建播放列表视图
    QListWidget *playlistWidget = new QListWidget;
    mainLayout->addWidget(playlistWidget);

    // 创建QMediaPlayer和QMediaPlaylist实例
    QMediaPlayer *player = new QMediaPlayer(&window);
    QMediaPlaylist *playlist = new QMediaPlaylist;
    player->setPlaylist(playlist);
    player->setVideoOutput(videoWidget);

    // 连接添加媒体按钮
    QObject::connect(addButton, &QPushButton::clicked, [&](){
        QStringList files = QFileDialog::getOpenFileNames(&window, "选择媒体文件", "", "音视频文件 (*.wav *.mp4 *.avi *.mkv *.mov)");
        if (!files.isEmpty()) {
            for (const QString &file : files) {
                playlist->addMedia(QUrl::fromLocalFile(file));
                playlistWidget->addItem(file);
            }

            int currentRow = playlistWidget->currentRow();
            // 如果没有选中项，选择第一个项目
            if (currentRow == -1 && playlist->mediaCount() > 0) {
                currentRow = 0;
                playlistWidget->setCurrentRow(currentRow); // 设置为选中
            }

            // 播放选中的媒体
            if (currentRow >= 0) {
                playlist->setCurrentIndex(currentRow); // 设置播放列表中的当前索引
                player->pause();
            }
        }
    });

    // 连接移除媒体按钮
    QObject::connect(removeButton, &QPushButton::clicked, [&](){
        int currentRow = playlistWidget->currentRow();
        if (currentRow >= 0) {
            playlist->removeMedia(currentRow);
            delete playlistWidget->takeItem(currentRow);
        } else {
            QMessageBox::warning(&window, "移除媒体", "请选择要移除的媒体项目。");
        }
    });

    // 更新进度条和时间标签
    QObject::connect(player, &QMediaPlayer::positionChanged, [&](qint64 position){
        positionSlider->setValue(position);
        QTime currentTime(0, (position / 60000) % 60, (position / 1000) % 60);
        currentTimeLabel->setText(currentTime.toString("mm:ss"));
    });

    QObject::connect(player, &QMediaPlayer::durationChanged, [&](qint64 duration){
        positionSlider->setRange(0, duration);
        QTime totalTime(0, (duration / 60000) % 60, (duration / 1000) % 60);
        totalTimeLabel->setText(totalTime.toString("mm:ss"));
    });

    // 允许用户通过滑动进度条跳转
    QObject::connect(positionSlider, &QSlider::sliderMoved, [&](int position){
        player->setPosition(position);
    });

    // 连接播放按钮
    QObject::connect(playButton, &QPushButton::clicked,  [&]() {
        int currentRow = playlistWidget->currentRow();

        // 如果没有选中项，选择第一个项目
        if (currentRow == -1 && playlist->mediaCount() > 0) {
            currentRow = 0;
            playlistWidget->setCurrentRow(currentRow); // 设置为选中
        }

        // 播放选中的媒体
        if (currentRow >= 0) {
            playlist->setCurrentIndex(currentRow); // 设置播放列表中的当前索引
            player->play();
        } else {
            QMessageBox::warning(&window, "播放", "播放列表为空。");
        }
    });

    // 连接暂停按钮
    QObject::connect(pauseButton, &QPushButton::clicked, player, &QMediaPlayer::pause);

    // 连接停止按钮
    QObject::connect(stopButton, &QPushButton::clicked, player, &QMediaPlayer::stop);

    // 连接下一首按钮
    QObject::connect(nextButton, &QPushButton::clicked, playlist, &QMediaPlaylist::next);

    // 连接上一首按钮
    QObject::connect(prevButton, &QPushButton::clicked, playlist, &QMediaPlaylist::previous);

    // 连接快进按钮
    QObject::connect(forwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        qint64 duration = player->duration();
        player->setPosition(qMin(current + 10000, duration));
    });

    // 连接快退按钮
    QObject::connect(backwardButton, &QPushButton::clicked, [&](){
        qint64 current = player->position();
        player->setPosition(qMax(current - 10000, 0LL));
    });


    // 同步播放列表视图与 QMediaPlaylist
    QObject::connect(playlist, &QMediaPlaylist::currentIndexChanged, [&](int index){
        playlistWidget->setCurrentRow(index);
    });

    // 设置播放模式
    // 可选：QMediaPlaylist::Sequential, QMediaPlaylist::Loop, QMediaPlaylist::Random
    playlist->setPlaybackMode(QMediaPlaylist::Loop);

    // 连接音量滑块
     QObject::connect(volumeSlider, &QSlider::valueChanged, [&](int value){
         player->setVolume(value);
         volumeValueLabel->setText(QString::number(value) + "%");
     });

     // 设置初始音量
     player->setVolume(volumeSlider->value());

    // 显示窗口
    window.show();

    return app.exec();
}

```



#### 代码说明



1. **音量滑块和标签**：使用 `QSlider` 实现音量的调整，范围设置为 0 到 100。`QLabel` 显示当前音量百分比。

2. 连接滑块与音量

   ：

   - 当滑块的值改变时，连接到 `QMediaPlayer::setVolume` 方法，实时调整音量。
   - 更新 `QLabel` 显示当前音量百分比。

3. **初始化音量**：根据滑块的默认值设置初始音量。

### 错误处理



在音视频播放过程中，可能会遇到各种错误，如文件格式不支持、媒体文件损坏等。通过连接 `QMediaPlayer` 的 `error` 信号，可以实现错误的捕捉与处理。

在原来的代码基础上添加这个错误捕获信号就行了

``` cpp
  // 连接错误信号
    QObject::connect(player, QOverload<QMediaPlayer::Error>::of(&QMediaPlayer::error),
                     [&](QMediaPlayer::Error error){
        if (error != QMediaPlayer::NoError) {
            QString errorMessage;
            switch (error) {
            case QMediaPlayer::NoError:
                break;
            case QMediaPlayer::ResourceError:
                errorMessage = "资源错误：无法加载媒体资源。";
                break;
            case QMediaPlayer::FormatError:
                errorMessage = "格式错误：媒体格式不支持。";
                break;
            case QMediaPlayer::NetworkError:
                errorMessage = "网络错误：无法访问媒体网络资源。";
                break;
            case QMediaPlayer::AccessDeniedError:
                errorMessage = "访问被拒绝：无权限访问媒体资源。";
                break;
            case QMediaPlayer::ServiceMissingError:
                errorMessage = "服务缺失：缺少必要的多媒体服务。";
                break;
            default:
                errorMessage = "未知错误。";
                break;
            }
            QMessageBox::critical(&window, "播放错误", errorMessage);
        }
    });
```



## 摄像头录制

摄像头录制也要包含`multimedia multimediawidgets`

``` cpp
QT       += core gui multimedia multimediawidgets
```

### 主要类和步骤



- **QCamera**：选择并控制摄像头设备。
- **QCameraViewfinder**：显示摄像头捕获的实时视频。
- **QCameraImageCapture**（可选）：捕获摄像头图像。

我们实现如下界面

![https://cdn.llfc.club/1728621441067.jpg](https://cdn.llfc.club/1728621441067.jpg)



``` cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>
#include <QCamera>
#include <QCameraViewfinder>
#include <QMediaRecorder>
#include <QPushButton>
#include <QVBoxLayout>
#include <QHBoxLayout>
#include <QMessageBox>

QT_BEGIN_NAMESPACE
namespace Ui { class MainWindow; }
QT_END_NAMESPACE

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    void startCamera();
    void stopCamera();
    void startRecording();
    void stopRecording();
    void handleMediaRecorderError(QMediaRecorder::Error error);
    void onStateChanged(QMediaRecorder::State state);
private:
    Ui::MainWindow *ui;

    QCamera *camera;
    QCameraViewfinder *viewfinder;
    QMediaRecorder *mediaRecorder;

    QPushButton *startCameraButton;
    QPushButton *stopCameraButton;
    QPushButton *startRecordingButton;
    QPushButton *stopRecordingButton;
};

#endif // MAINWINDOW_H

```

具体实现

``` cpp
#include "mainwindow.h"
// #include "ui_mainwindow.h" // Not used since we're building UI programmatically
#include <QFileDialog>
#include <QStandardPaths>
#include <QDir>
#include <QFileInfo>
#include <QDebug>

MainWindow::MainWindow(QWidget *parent)
    : QMainWindow(parent),
      ui(nullptr),
      camera(nullptr),
      viewfinder(nullptr),
      mediaRecorder(nullptr),
      startCameraButton(nullptr),
      stopCameraButton(nullptr),
      startRecordingButton(nullptr),
      stopRecordingButton(nullptr)
{
    // Set up the main window
    setWindowTitle("Qt Video Recorder");
    resize(800, 600);

    // Create central widget and layout
    QWidget *centralWidget = new QWidget(this);
    QVBoxLayout *mainLayout = new QVBoxLayout(centralWidget);

    // Initialize camera and viewfinder
    camera = new QCamera(this);
    viewfinder = new QCameraViewfinder(this);
    camera->setViewfinder(viewfinder);

    // Initialize media recorder
    mediaRecorder = new QMediaRecorder(camera, this);
    // Optional: You can set encoding settings here
    // QAudioEncoderSettings audioSettings;
    // QVideoEncoderSettings videoSettings;
    // mediaRecorder->setAudioSettings(audioSettings);
    // mediaRecorder->setVideoSettings(videoSettings);

    // Add viewfinder to the layout
    mainLayout->addWidget(viewfinder, 1); // Stretch factor 1 to make it expandable

    // Create buttons
    startCameraButton = new QPushButton("Start Camera", this);
    stopCameraButton = new QPushButton("Stop Camera", this);
    startRecordingButton = new QPushButton("Start Recording", this);
    stopRecordingButton = new QPushButton("Stop Recording", this);

    // Disable stop buttons initially
    stopCameraButton->setEnabled(false);
    startRecordingButton->setEnabled(false);
    stopRecordingButton->setEnabled(false);

    // Create a horizontal layout for buttons
    QHBoxLayout *buttonLayout = new QHBoxLayout();
    buttonLayout->addWidget(startCameraButton);
    buttonLayout->addWidget(stopCameraButton);
    buttonLayout->addWidget(startRecordingButton);
    buttonLayout->addWidget(stopRecordingButton);

    // Add button layout to the main layout
    mainLayout->addLayout(buttonLayout);

    // Set central widget
    setCentralWidget(centralWidget);

    // Connect buttons to slots
    connect(startCameraButton, &QPushButton::clicked, this, &MainWindow::startCamera);
    connect(stopCameraButton, &QPushButton::clicked, this, &MainWindow::stopCamera);
    connect(startRecordingButton, &QPushButton::clicked, this, &MainWindow::startRecording);
    connect(stopRecordingButton, &QPushButton::clicked, this, &MainWindow::stopRecording);

    // Connect media recorder error signal
    connect(mediaRecorder, QOverload<QMediaRecorder::Error>::of(&QMediaRecorder::error),
            this, &MainWindow::handleMediaRecorderError);

    connect(mediaRecorder, &QMediaRecorder::stateChanged, this, &MainWindow::onStateChanged);
}

void MainWindow::onStateChanged(QMediaRecorder::State state)
{
    qDebug() << "MediaRecorder state changed to:" << state;

    switch (state) {
        case QMediaRecorder::RecordingState:
            QMessageBox::information(this, "Recording State", "Recording has started.");
            startRecordingButton->setEnabled(false);
            stopRecordingButton->setEnabled(true);
            break;
        case QMediaRecorder::PausedState:
            // Handle paused state if applicable
            break;
        case QMediaRecorder::StoppedState:
            QMessageBox::information(this, "Recording State", "Recording has stopped.");
            startRecordingButton->setEnabled(true);
            stopRecordingButton->setEnabled(false);
            break;
    }
}

MainWindow::~MainWindow()
{
    if (camera->state() == QCamera::ActiveState)
        camera->stop();

    delete mediaRecorder;
    delete viewfinder;
    delete camera;
    delete startCameraButton;
    delete stopCameraButton;
    delete startRecordingButton;
    delete stopRecordingButton;
    delete ui;
}

void MainWindow::startCamera()
{
    camera->start();

    if (camera->error() != QCamera::NoError) {
        QMessageBox::warning(this, "Camera Error", camera->errorString());
        return;
    }

    // Update button states
    startCameraButton->setEnabled(false);
    stopCameraButton->setEnabled(true);
    startRecordingButton->setEnabled(true);

    qDebug() << "Camera started.";
}

void MainWindow::stopCamera()
{
    camera->stop();

    // Stop recording if it's active
    if (mediaRecorder->state() == QMediaRecorder::RecordingState) {
        mediaRecorder->stop();
    }

    // Update button states
    startCameraButton->setEnabled(true);
    stopCameraButton->setEnabled(false);
    startRecordingButton->setEnabled(false);
    stopRecordingButton->setEnabled(false);

    qDebug() << "Camera stopped.";
}

void MainWindow::startRecording()
{
    if (mediaRecorder->state() == QMediaRecorder::StoppedState) {
        // Get default movies directory
        QString defaultPath = QStandardPaths::writableLocation(QStandardPaths::MoviesLocation);
        if (defaultPath.isEmpty()) {
            defaultPath = QDir::homePath();
        }

        // Open file dialog to select save location
        QString fileName = QFileDialog::getSaveFileName(this, "Save Video", defaultPath, "MP4 Files (*.mp4)");
        if (fileName.isEmpty())
            return;

        QFileInfo fileInfo(fileName);
        QString absolutePath = fileInfo.absoluteFilePath();

        // Set output location
        mediaRecorder->setOutputLocation(QUrl::fromLocalFile(absolutePath));
        mediaRecorder->setContainerFormat("mp4");

        // Optionally, set codecs
        // mediaRecorder->setVideoCodec("video/h264");
        // mediaRecorder->setAudioCodec("audio/aac");

        // Start recording
        mediaRecorder->record();

        if (mediaRecorder->error() != QMediaRecorder::NoError) {
            QMessageBox::warning(this, "Recording Error", mediaRecorder->errorString());
            return;
        }

        // Update button states
        startRecordingButton->setEnabled(false);
        stopRecordingButton->setEnabled(true);

        QMessageBox::information(this, "Recording Started", "Recording has started.");
        qDebug() << "Recording started. state is : " << mediaRecorder->state();
    }
}

void MainWindow::stopRecording()
{
     qDebug() << "stopRecording. state is : " << mediaRecorder->state();
    if (mediaRecorder->state() == QMediaRecorder::RecordingState) {
        mediaRecorder->stop();

        QString filePath = mediaRecorder->outputLocation().toLocalFile();
        QFile file(filePath);
        if (file.exists() && file.size() > 0) {
            QMessageBox::information(this, "Recording Stopped", "Video has been saved to:\n" + filePath);
            qDebug() << "Recording stopped. Saved to:" << filePath;
        } else {
            QMessageBox::warning(this, "Recording Failed", "Video was not saved correctly.");
            qDebug() << "Recording stopped. File does not exist or is empty.";
        }

        // Update button states
        startRecordingButton->setEnabled(true);
        stopRecordingButton->setEnabled(false);
    }
}

void MainWindow::handleMediaRecorderError(QMediaRecorder::Error error)
{
    if (error != QMediaRecorder::NoError) {
        QMessageBox::critical(this, "Media Recorder Error", mediaRecorder->errorString());
        qDebug() << "MediaRecorder Error:" << mediaRecorder->errorString();

        // Update button states if necessary
        if (mediaRecorder->state() == QMediaRecorder::RecordingState) {
            stopRecording();
        }
    }
}

```

主函数调用

``` cpp
#include "mainwindow.h"
#include <QApplication>
#include <QTimer>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);
    MainWindow w;
    w.show();
    return a.exec();
}

```





# 第十四章 串口编程

### 理论知识讲解



#### 1. 串口通信基础



- **概念**：串口（Serial Port）是一种常用的设备间数据传输方式，常用于计算机与外部设备（如传感器、Arduino板等）之间的通讯。
- **协议**：常见的串口通信协议包括RS-232、RS-485等，它们定义了数据传输的物理层和链路层规范。
- **参数设置**：串口通信的关键参数有波特率（Baud Rate）、数据位（Data Bits）、停止位（Stop Bits）和校验位（Parity）等，双方设备需设置相同才能正常通信。



#### 2. Qt中的串口编程



- **QSerialPort类**：Qt提供`QSerialPort`类来处理串口通信，它封装了打开、配置、读写串口等操作。
- **信号与槽机制**：利用Qt的信号与槽机制可以方便地处理串口数据的接收和发送事件。



### 代码案例：简单串口通信示例



#### 目标



创建一个简单的Qt应用程序，能够向串口发送数据并接收显示返回的数据。



#### 步骤



1. **创建Qt Widgets Application**：使用Qt Creator新建一个Qt Widgets Application项目，命名为SerialCommExample。
2. **添加UI元素**：在设计模式下，为窗口添加一个LineEdit用于输入发送的数据，一个PushButton用于触发发送操作，以及一个TextBrowser用于显示接收的数据。
3. **引入QSerialPort**：在`.pro`文件中添加`QT += serialport`，确保项目能够使用串口功能。
4. **编写逻辑代码**：在相应的头文件和源文件中实现串口的初始化、配置、读写等功能。



**mainwindow.h**



```cpp
#ifndef MAINWINDOW_H
#define MAINWINDOW_H

#include <QMainWindow>
#include <QSerialPort>
#include <QSerialPortInfo>

namespace Ui {
class MainWindow;
}

class MainWindow : public QMainWindow
{
    Q_OBJECT

public:
    explicit MainWindow(QWidget *parent = nullptr);
    ~MainWindow();

private slots:
    void on_pushButtonSend_clicked();
    void handleReadyRead();

private:
    Ui::MainWindow *ui;
    QSerialPort serial;

    void initSerialPort();
};
#endif // MAINWINDOW_H
```



**mainwindow.cpp**



```cpp
#include "mainwindow.h"
#include "ui_mainwindow.h"

MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
    initSerialPort();
    connect(&serial, &QSerialPort::readyRead, this, &MainWindow::handleReadyRead);
}

MainWindow::~MainWindow()
{
    delete ui;
}

void MainWindow::initSerialPort()
{
    foreach (const QSerialPortInfo &info, QSerialPortInfo::availablePorts()) {
        if(info.hasVendorIdentifier() && info.hasProductIdentifier()){
            if(info.vendorIdentifier() == YOUR_VENDOR_ID && info.productIdentifier() == YOUR_PRODUCT_ID){
                serial.setPort(info);
                break;
            }
        } else {
            qDebug() << "No Vendor ID and Product ID found.";
        }
    }

    if(serial.isOpen()){
        serial.close();
    }

    serial.setBaudRate(QSerialPort::Baud9600); // 设置波特率为9600
    serial.setDataBits(QSerialPort::Data8);     // 数据位为8
    serial.setParity(QSerialPort::NoParity);   // 无校验位
    serial.setStopBits(QSerialPort::OneStop);  // 停止位为1
    serial.setFlowControl(QSerialPort::NoFlowControl);

    if (!serial.open(QIODevice::ReadWrite)) {
        qDebug() << "Failed to open the port!";
    }
}

void MainWindow::on_pushButtonSend_clicked()
{
    QString text = ui->lineEditInput->text();
    serial.write(text.toUtf8());
}

void MainWindow::handleReadyRead()
{
    QByteArray data = serial.readAll();
    ui->textBrowserReceived->append(QString(data));
}
```



注意：上述代码中的`YOUR_VENDOR_ID`和`YOUR_PRODUCT_ID`需要根据实际使用的串口设备的硬件信息进行替换或调整查找逻辑。



这个示例展示了如何使用Qt的`QSerialPort`类进行基本的串口通信设置、数据发送和接收。在准备教案时，可以根据学生的水平详细解释每个步骤的原理和作用，并通过实践让学生动手尝试，加深理解。





# 第十五章 打包发布
## QSS美化

QSS（Qt Style Sheets）是 Qt 框架中用于定制用户界面外观的一种样式表语言，类似于 CSS（层叠样式表）。使用 QSS，您可以为 Qt 应用程序中的各种控件设置样式，以改变它们的外观和感觉。以下是 QSS 的一些基本知识和用法：



### 1. 基本语法



QSS 的基本语法与 CSS 类似。您可以选择控件类型、类、ID 和属性来定义样式。例如：



```css
QPushButton {
    background-color: #4CAF50; /* 背景颜色 */
    color: white;              /* 字体颜色 */
    border: none;              /* 边框样式 */
    padding: 10px;             /* 内边距 */
    border-radius: 5px;       /* 边框圆角 */
}

QPushButton:hover {
    background-color: #45a049; /* 鼠标悬停时的背景颜色 */
}
```



### 2. 选择器



QSS 支持多种选择器：



- **控件类型选择器**：如 `QPushButton`, `QLabel` 等，选择所有该类型的控件。
- **类选择器**：如 `.myClass`，选择所有具有指定类的控件。
- **ID 选择器**：如 `#myId`，选择具有指定 ID 的控件。
- **层叠选择器**：可以组合选择器，例如 `QPushButton#myId` 选择具有指定 ID 的 QPushButton。



### 3. 属性



QSS 允许设置多种控件属性，例如：



- `background-color`：背景颜色
- `color`：文本颜色
- `font-size`：字体大小
- `border`：边框样式
- `padding`：内边距
- `margin`：外边距
- `border-radius`：边框圆角



### 4. 应用 QSS



您可以通过 `QWidget` 的 `setStyleSheet` 方法应用 QSS。例如：



```cpp
QPushButton *button = new QPushButton("Click Me");
button->setStyleSheet("background-color: blue; color: white;");
```



### 5. 动态样式



QSS 支持动态样式，您可以根据控件的状态（如鼠标悬停、被按下等）来定义不同的样式。例如：



```css
QPushButton:pressed {
    background-color: #005f5f; /* 按下时的背景颜色 */
}
```



### 6. 继承与重用



QSS 支持样式的继承，您可以为父控件设置样式，子控件将自动继承这些样式。例如：



```css
QWidget {
    background-color: #f0f0f0;
}

QPushButton {
    color: black; /* 所有按钮将使用黑色文本 */
}
```



### 7. 注意事项



- QSS 不支持所有 CSS 功能，如复杂的选择器和动画。
- QSS 的性能可能会受到影响，尤其是在有大量控件时，因此应谨慎使用。
- 有些控件的样式可能会受到操作系统主题的影响。



### 示例



以下是一个完整的示例，展示如何在 Qt 应用程序中使用 QSS：



```cpp
#include <QApplication>
#include <QPushButton>
#include <QVBoxLayout>
#include <QWidget>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);

    QWidget window;
    window.setWindowTitle("QSS Example");

    QVBoxLayout *layout = new QVBoxLayout(&window);
    QPushButton *button1 = new QPushButton("Button 1");
    QPushButton *button2 = new QPushButton("Button 2");

    layout->addWidget(button1);
    layout->addWidget(button2);

    // 设置 QSS
    QString styleSheet = "QPushButton { background-color: #4CAF50; color: white; }"
                         "QPushButton:hover { background-color: #45a049; }"
                         "QPushButton:pressed { background-color: #005f5f; }";
    app.setStyleSheet(styleSheet);

    window.show();
    return app.exec();
}
```



通过以上示例，您可以看到如何使用 QSS 来定制 Qt 应用程序的外观。希望这些信息对您有所帮助！如果您有任何具体问题或需要进一步的示例，请告诉我。

## windows打包QT程序

### 步骤 1：构建您的 Qt 应用程序



首先，确保您的 Qt 项目已经成功构建并且可以正常运行。您可以使用 Qt Creator 或命令行工具进行构建。



```bash
qmake your_project.pro
make
```



### 步骤 2：使用 `windeployqt` 工具



在构建完成后，使用 `windeployqt` 工具来复制所有必要的 Qt 依赖项到您的应用程序目录。



1. **打开命令提示符**：

   - 按 `Win + R`，输入 `cmd`，然后按 Enter。

2. **导航到您的可执行文件所在的目录**：

   ```bash
   cd path\to\your\build\directory
   ```

3. **运行 `windeployqt`**：

   ```bash
   windeployqt your_application.exe
   ```

   这将自动复制 Qt DLL、插件等到与您的可执行文件相同的目录。



### 步骤 3：准备 Inno Setup 脚本



接下来，您需要创建一个 Inno Setup 脚本文件（例如 `setup_script.iss`），该文件定义了安装程序的行为。



以下是一个示例脚本：



```ini
; Inno Setup Script
[Setup]
AppName=YourAppName
AppVersion=1.0
DefaultDirName={pf}\YourAppName
DefaultGroupName=YourAppName
OutputDir=Output
OutputBaseFilename=YourAppInstaller
Compression=lzma
SolidCompression=yes

[Files]
; 添加您的可执行文件
Source: "path\to\your\build\directory\your_application.exe"; DestDir: "{app}"; Flags: ignoreversion
; 添加所有 windeployqt 复制的 Qt DLL 和其他文件
Source: "path\to\your\build\directory\*"; DestDir: "{app}"; Flags: ignoreversion recursesubdirs createallsubdirs

[Icons]
Name: "{group}\YourAppName"; Filename: "{app}\your_application.exe"
Name: "{commondesktop}\YourAppName"; Filename: "{app}\your_application.exe"; Tasks: desktopicon

[Run]
Filename: "{app}\your_application.exe"; Description: "{cm:LaunchProgram,YourAppName}"; Flags: nowait postinstall skipifsilent
```



### 步骤 4：编译 Inno Setup 脚本



1. **安装 Inno Setup**：
    从 [Inno Setup 官网](https://jrsoftware.org/isinfo.php) 下载并安装 Inno Setup。
2. **打开 Inno Setup Compiler**：
    启动 Inno Setup Compiler，打开您刚才创建的脚本文件。
3. **编译脚本**：
    点击菜单栏中的“编译”按钮（或按 F9），Inno Setup 将根据您的脚本生成安装程序。



### 步骤 5：测试安装程序



在编译完成后，您将在指定的 `Output` 目录中找到生成的安装程序（例如 `YourAppInstaller.exe`）。运行该安装程序以测试安装过程，确保您的应用程序能够正常运行。



## Linux 打包QT程序

在 Linux 上打包 Qt 应用程序可以通过多种方式实现，具体取决于您的需求和目标平台。以下是一个常用的方法，使用 `AppImage` 和 `linuxdeployqt` 工具来打包 Qt 应用程序。



### 步骤 1：构建您的 Qt 应用程序



首先，确保您的 Qt 项目已经成功构建并且可以正常运行。您可以使用 Qt Creator 或命令行工具进行构建。



```bash
qmake your_project.pro
make
```



### 步骤 2：安装 `linuxdeployqt`



`linuxdeployqt` 是一个方便的工具，可以帮助您将 Qt 应用程序打包为 AppImage 格式。您可以从 GitHub 上下载它。



1. **下载 `linuxdeployqt`**：

   ```bash
   wget https://github.com/probonopd/linuxdeployqt/releases/download/continuous/linuxdeployqt-<version>-x86_64.AppImage
   chmod +x linuxdeployqt-<version>-x86_64.AppImage
   ```

   请将 `<version>` 替换为您要下载的版本号。



### 步骤 3：使用 `linuxdeployqt` 打包应用程序



1. **运行 `linuxdeployqt`**：
    在您的应用程序可执行文件所在的目录中运行以下命令：

   ```bash
   ./linuxdeployqt-<version>-x86_64.AppImage your_application -appimage
   ```

   这将创建一个 AppImage 文件，包含所有必需的 Qt 库和依赖项。



### 步骤 4：测试 AppImage



生成的 AppImage 文件通常会在当前目录中。您可以通过以下命令运行它：



```bash
./your_application-x86_64.AppImage
```



### 步骤 5：创建桌面条目（可选）



如果您希望在应用程序菜单中显示您的应用程序，可以为其创建一个 `.desktop` 文件。以下是一个示例 `.desktop` 文件：



```ini
[Desktop Entry]
Name=YourAppName
Exec=/path/to/your_application-x86_64.AppImage
Icon=/path/to/icon.png
Type=Application
Categories=Utility;
```



将其保存为 `your_application.desktop`，并将其放置在 `~/.local/share/applications/` 目录中。



### 备用方法：使用 `AppImage` 工具



如果您希望手动创建 AppImage，还可以使用 `AppImage` 工具。以下是基本步骤：



1. **创建目录结构**：

   ```bash
   mkdir -p YourApp.AppDir/usr/bin
   mkdir -p YourApp.AppDir/usr/share/applications
   mkdir -p YourApp.AppDir/usr/share/icons/hicolor/256x256/apps
   ```

2. **复制可执行文件和资源**：
    将您的可执行文件、图标和其他资源复制到相应的目录中。

3. **创建 AppImage**：
    使用 `appimagetool` 工具创建 AppImage。您可以从 [AppImage GitHub 页面](https://github.com/AppImage/AppImageKit/releases) 下载 `appimagetool`。

   ```bash
   ./appimagetool YourApp.AppDir
   ```



## Linux移植ARM

这部分放在前面介绍了，根据具体的板子做不同的移植



- windows打包windeployqt
- linux 打包linuxdeployqt
- 打包移植到arm















