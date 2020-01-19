# 酱油君的项目

## Pulvis 云盘 概览

Editted at 2020/1/12 by arno at 15:57 am.

### 描述

**Pulvis云盘是一个基于微服务架构的云端文件管理WEB应用，包含服务器端和客户端。该系统基于HTTP协议，使用URL实现各模块间的系统内部交互。**

**Pulvis服务器端支持对文件进行逻辑分区，以及文件的基本操作。服务器端的逻辑层含登陆会话模块，用户模块，系统模块。会话模块用于管理用户会话获取当前用户的Token。用户模块，验证用户的token来获取用户信息以及用户的文件空间。系统模块负责文件的逻辑分区和读写部分，通过upload/download 模式 实现文件的写操作。**

### 功能

**该应用应该包含以下特点：**

- **用户注册和登陆：用户需要无状态登陆，登陆状态不由传统session实现，而是通过token来进行用户验证，Token由非对称加密来计算和验证。**
- **文件的分区： 用户的文件系统是由文件系统虚拟出来的，文件系统内存在从用户文件空间的地址到实际地址的映射，这里应该符合易用性原则，映射对用户是不可见的。**
- **文件的读写： 应该实现文件基本的读操作和写操作，这里使用upload/download 方案来实现远端文件的读写，读操作通过系统生成的临时URL下载内容， 写操作通过唯一的URL+token认证实现上传更新，（这里建议delayed wirte,在本地完成读写后异步上传。。)**
- **会话模块：用于验证当前用户的Token，读取用户信息，通知用户界面的更新。由于是非对称加密，应该包含token数字签名的验证。**
- **用户界面： 初期不需要用户界面的设计，使用Json和控制台进行交互**

## 未整理的需求

**协议和接口： 服务端和客户端的交互由http协议实现，各个模块的耦合通过URL实现**

### 步骤

**-概览：**

 **预计完成时间 6个月，时间区间从2020年3月到2020年9月** 

- **March：**

    主要实现用户模块和会话模块，用户的登陆和验证的库通过Python实现，数据层通过关系型数据库实现，并且可部署到远端，可以实现远端的系统调用。

- **April：**

    待定

- **May:**
- **June**
- **July**
- **August**
- **December**