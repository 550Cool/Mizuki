---
title: 高通设备树提取工具
published: 2025-09-14
pinned: true
description: 一个用于提取高通设备树的小工具
tags: [Qualcomm, Device-tree]
category: Tools
licenseName: "CC BY 4.0"
author: 2days
sourceLink: "https://github.com/550Cool/Qualcomm-Device-Tree-Extraction-Tool"
draft: false
date: 2025-09-14
pubDate: 2025-09-14
---

# 高通设备树提取工具

用于从安卓启动镜像boot.img中提取设备树文件
仓库地址：https://github.com/550Cool/Qualcomm-Device-Tree-Extraction-Tool
## 使用方法

### 1\. 准备工作

将以下文件放置在脚本同一目录下：

* **必需文件**: `boot.img`
* **可选文件（位于设备的/proc/device-tree文件夹下）**:

  * `qcom,msm-id`
  * `qcom,board-id`
  * `model`

### 2\. 运行脚本

```bash
# 下载脚本
git clone <repository-url>
cd <repository-directory>

# 添加执行权限
chmod +x extract\\\_dt.sh

# 运行脚本
./extract\\\_dt.sh

PS:其实原本打算增加设备树定位功能，用于快速确定bootloader加载的设备树文件，不过感觉太麻烦就去掉了。理论上也可用于其他处理器的安卓设备（实测MT6735可用），不过设计初衷是用于高通设备