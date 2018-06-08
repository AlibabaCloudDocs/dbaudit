# 部署Agent程序 {#concept_jf4_nz2_xdb .concept}

将数据库添加至数据库审计系统后，您需要将Agent程序部署到相应的数据库或应用服务器上。Agent程序会获取访问数据库的流量，帮助数据库审计系统通过获取的流量实现数据库的分析审计。

## Agent程序部署位置 {#section_frq_y2k_xdb .section}

根据所添加的数据库在云环境中的实际部署方式，您需要将Agent程序部署在以下位置：

-   ECS云服务器自建数据库：Agent程序需要部署在数据库所在的ECS云服务器上。
-   RDS云数据库实例：Agent程序需要部署在对应的应用服务器上。

## 自动部署Agent程序 {#section_xgl_bfk_xdb .section}

**Note:** Agent程序自动部署仅支持Linux系统。即对于ECS云服务器自建数据库的情况，数据库所在的ECS云服务器必须使用Linux系统；对于RDS云数据库实例，对应的应用服务器必须使用Linux系统。如果您需要审计的数据库所对应的服务器不是Linux系统，请查看[手动部署Agent程序](#section_gwt_pfk_xdb)。

参照以下步骤，自动部署Agent程序：

1.  [登录云盾数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)。
2.  在维护页面，选择**Agent管理**，单击**Agent自动部署**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3662_zh-CN.png)

3.  在Agent自动部署对话框中，按照格式填写需要部署Agent程序的服务器IP地址、ROOT用户密码和SSH端口号，然后单击**部署**，即可将Agent程序自动部署到相应的服务器中。参数说明如下：
    -   **审计服务器IP**：填写数据库审计系统的IP地址，您可以在[登录数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)时查看系统的内网和外网IP。如果数据库审计系统与Agent程序所在的服务器处于同一内网环境中，添加数据库审计系统的内网IP即可；如果两者不在同一内网中，则添加数据库审计系统的外网IP。
    -   **目标服务器**：指需要自动部署Agent程序的服务器相关信息，格式为`目标IP,root密码,ssh端口`。

        **Note:** Agent程序的自动部署需要服务器开通SSH端口，并且自动部署过程中需要使用ROOT用户密码。

    -   如果应用服务与数据库部署在同一台服务器中，在自动部署Agent程序时，需要勾选**本地回环**。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3663_zh-CN.png)

4.  Agent程序自动部署完成后，返回Agent管理页面，单击**Agent部署配置**。
5.  在Agent部署配置对话框中，输入需要部署Agent程序的服务器IP地址，然后单击**添加**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3664_zh-CN.png)

    **Note:** 

    -   如果需要部署Agent程序的服务器与数据库审计系统处于同一个内网，则直接添加内网地址即可；如果与数据库审计系统不在同一个内网需要通过外网进行通信的，则需添加该服务器的外网地址。
    -   如果不添加部署Agent程序的服务器IP地址，审计系统将无法抓取该服务器的数据进行审计。

## 手动部署Agent程序 {#section_gwt_pfk_xdb .section}

**Windows系统服务器部署Agent程序**

对于Windows系统服务器，您需要根据云环境中数据库的实际部署情况选择相应的方式手动部署Agent程序。

-   **应用系统与数据库部署在不同的服务器**
    1.  [登录云盾数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)。
    2.  在维护页面，选择**Agent管理**，单击**下载Agent**。系统自动弹出Agent部署配置提示，且浏览器自动开始将Agent程序（即rmagent.tar.gz文件）下载至本地。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3665_zh-CN.png)

    3.  在Agent部署配置对话框中，输入需要部署Agent程序的服务器IP地址，然后单击**添加**。

        **Note:** 

        -   如果需要部署Agent程序的服务器与数据库审计系统处于同一个内网，则直接添加内网地址即可；如果与数据库审计系统不在同一个内网需要通过外网进行通信的，则需添加该服务器的外网地址。
        -   如果不添加部署Agent程序的服务器IP地址，审计系统将无法抓取该服务器的数据进行审计。
    4.  将Agent程序（即rmagent.tar.gz）文件上传到需要部署Agent程序的服务器，并将其解压缩。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3666_zh-CN.png)

    5.  打开解压后的Agent程序文件夹，双击运行Rmagent\_Setup.exe程序文件。
    6.  在Installer Language对话框中，单击**OK**。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3667_zh-CN.png)

    7.  在rmagent1.0安装对话框中，单击**下一步**，直到Agent程序开始安装。

        **Note:** 选择组件时，必须勾选**VS 2015 Redistributable**和**WinPcap**组件，在Agent程序安装过程中将自动运行相关组件的安装程序。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3668_zh-CN.png)

    8.  所有组件及Agent程序安装完成后，重新启动服务器，即完成Agent程序的部署。
-   应用服务与数据库部署在同一台服务器的情况
    1.  [登录云盾数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)。
    2.  在维护页面，选择**Agent管理**，单击**下载Agent**。系统自动弹出Agent部署配置提示，且浏览器自动开始将Agent程序（即rmagent.tar.gz文件）下载至本地。
    3.  在Agent部署配置对话框中，输入需要部署Agent程序的服务器IP地址，然后单击**添加**。

        **Note:** 

        -   如果需要部署Agent程序的服务器与数据库审计系统处于同一个内网，则直接添加内网地址即可；如果与数据库审计系统不在同一个内网需要通过外网进行通信的，则需添加该服务器的外网地址。
        -   如果不添加部署Agent程序的服务器IP地址，审计系统将无法抓取该服务器的数据进行审计。
    4.  将Agent程序（即rmagent.tar.gz文件）文件上传到需要部署Agent程序的服务器，并将其解压缩。
    5.  打开解压后的Agent程序文件夹，双击运行Rmagent\_Setup.exe程序文件。
    6.  在Installer Language对话框中，单击**OK**。
    7.  在rmagent1.0安装对话框中，单击**下一步**，直到Agent程序开始安装。

        **Note:** 选择组件时，必须勾选**VS 2015 Redistributable**和**npcap**组件，在Agent程序安装过程中将自动运行相关组件的安装程序。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3669_zh-CN.png)

        **Note:** 安装Npcap组件时，请务必勾选**Install Npcap in WinPcap API-compatible Mode**选项。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3670_zh-CN.png)

    8.  所有组件及Agent程序安装完成后，修改C:\\Users\\<用户名\>\\AppData\\Roaming\\rmagent\\rmagent.ini文件，将其中`#loopback=1`一行中的`#`删除以解除注释，保存文件。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3671_zh-CN.png)

    9.  重新启动服务器，完成Agent程序的部署。

**Linux系统服务器部署Agent程序**

对于Linux系统服务器，您也可以根据云环境中数据库的实际部署情况选择相应的方式手动部署Agent程序。

-   应用服务与数据库部署在不同的服务器的情况
    1.  [登录云盾数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)。
    2.  在维护页面，选择**Agent管理**，单击**下载Agent**。系统自动弹出Agent部署配置提示，且浏览器自动开始将Agent程序（即rmagent.tar.gz文件）下载至本地。
    3.  在Agent部署配置对话框中，输入需要部署Agent程序的服务器IP地址，然后单击**添加**。

        **Note:** 

        -   如果需要部署Agent程序的服务器与数据库审计系统处于同一个内网，则直接添加内网地址即可；如果与数据库审计系统不在同一个内网需要通过外网进行通信的，则需添加该服务器的外网地址。
        -   如果不添加部署Agent程序的服务器IP地址，审计系统将无法抓取该服务器的数据进行审计。
    4.  以root用户登录需要安装Agent程序的服务器，将rmagent.tar.gz文件上传到服务器，并将其解压缩。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3672_zh-CN.png)

    5.  执行`chmod 755 install.sh`命令，给install.sh文件增加权限。
    6.  安装Agent程序。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3673_zh-CN.png)

    7.  安装完成后，启动Agent程序（rmagent）完成Agent程序的部署。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3674_zh-CN.png)

-   应用服务与数据库部署在同一台服务器的情况
    1.  [登录云盾数据库审计系统](cn.zh-CN/用户指南/登录数据库审计系统.md#)。
    2.  在维护页面，选择**Agent管理**，单击**下载Agent**。系统自动弹出Agent部署配置提示，且浏览器自动开始将Agent程序（即rmagent.tar.gz文件）下载至本地。
    3.  在Agent部署配置对话框中，输入需要部署Agent程序的服务器IP地址，然后单击**添加**。

        **Note:** 

        -   如果需要部署Agent程序的服务器与数据库审计系统处于同一个内网，则直接添加内网地址即可；如果与数据库审计系统不在同一个内网需要通过外网进行通信的，则需添加该服务器的外网地址。
        -   如果不添加部署Agent程序的服务器IP地址，审计系统将无法抓取该服务器的数据进行审计。
    4.  以root用户登录需要安装Agent程序的服务器，将rmagent.tar.gz文件上传到服务器，并将其解压缩。
    5.  执行`chmod 755 install.sh`命令，给install.sh文件增加权限。
    6.  安装Agent程序。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3675_zh-CN.png)

    7.  安装完成后，进入rmagent安装目录，使用VI编辑器修改rmagent.ini配置文件，在文件最后加入一行`loopback=1`，然后保存。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3676_zh-CN.png)

    8.  执行`./stop_rmagent.sh`命令停止rmagent进程后，执行`./rmagent`命令重启Agent程序使配置更改生效，完成Agent程序的部署。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3677_zh-CN.png)


## Agent部署注意事项 {#section_bqt_glk_xdb .section}

Agent程序默认连接数据库审计系统的内网IP，如果部署Agent程序的服务器与云盾数据库审计系统之间通过外网连接则需要修改rmagent.ini配置文件中的IP地址。

**Windows系统服务器修改Agent程序连接地址**

1.  登录数据库所在服务器或RDS数据库实例所对应的应用服务器。
2.  找到并修改C:\\Users\\用户名\\AppData\\Roaming\\rmagent\\rmagent.ini配置文件，将其中`server_host`一行的IP地址修改为云盾数据库审计系统的外网IP地址，保存文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3678_zh-CN.png)

3.  重新启动rmagent服务，使配置变更生效。在服务管理器，选中**Rmagent Service**服务，单击**重启动此服务**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3679_zh-CN.png)


**Linux系统服务器修改Agent程序连接地址**

1.  登录数据库所在服务器或RDS数据库实例所对应的应用服务器。
2.  进入rmagent安装目录，使用VI编辑器修改rmagent.ini配置文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3680_zh-CN.png)

3.  将`server_host`的值修改为云盾数据库审计系统的外网IP地址，然后保存。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12776/3681_zh-CN.png)

4.  执行`./stop_rmagent.sh`命令停止rmagent进程后，执行`./rmagent`命令重启Agent程序，使配置更改生效。

## Agent程序部署测试 {#section_afh_3lk_xdb .section}

在数据库相应的服务器上成功部署Agent程序后，数据库审计系统就可以正常对您已添加的数据库进行审计。

您可以通过使用已安装Agent程序的应用服务器访问被审计的数据库实例并执行SQL语句，然后登录云盾数据库审计系统，查看是否已有审计信息。

-   如果数据库审计系统正常记录了该数据库实例的审计信息，则说明数据库实例部署成功。
-   如果数据库审计系统未能记录到审计信息，在相应的ECS云服务器上查看Agent程序的日志确认连接是否正常。

**查看Agent程序日志**

Agent程序的日志一般存放在以下目录：

-   Windows：C:\\tmp\\rmagent\\rmagent\_info.log
-   Linux：/tmp/rmagent/rmagent\_info.log

如果在Agent程序的日志中出现以下信息，表示Agent程序未能正确连接到数据库审计系统。

```
xml[INFO][tid=31235]20170322114351 rmagent.cpp:912:Rma_ConnectServer connect <审计系统IP地址>:9266 failed, Connection timed out
```

**解决方案**

检查该数据库审计实例所在的安全组是否放开了内网入方向的9266端口。由于Agent程序与数据库审计系统是通过9266端口进行通讯的，请确保在相关的安全组中放行该端口。

