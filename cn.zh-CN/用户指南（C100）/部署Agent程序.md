# 部署Agent程序 {#concept_592911 .task}

数据库审计系统的Agent程序是部署在用户终端或目标数据库服务器上的功能插件，用来转发数据库访问流量到审计系统。您需要根据数据库服务器的操作系统类型，选择部署Linux或者Windows版本的Agent，才能使数据库审计服务收集目标数据库的访问流量信息。

## Agent程序的部署位置 {#section_d6n_7i7_ir2 .section}

根据所添加的数据库类型，您需要将Agent程序部署在以下位置：

-   RDS数据库：Agent程序需要部署在与该数据库相连的应用服务器上。

    **说明：** RDS数据库内暂时无法安装配置Agent。

-   ECS自建数据库：Agent程序可以部署在数据库所在服务器上，也可以部署在与该数据库相连的Web服务器上。

**说明：** 如果您的ECS位于经典网络中，请参照[审计经典网络数据库实例](cn.zh-CN/用户指南（C100）/审计经典网络数据库实例.md#)进行特殊处理。

## Linux系统部署Agent {#section_0wd_pw6_7vw .section}

**背景信息**

云盾数据库审计系统的系统管理导航下提供Agent管理功能页面，您可以在Agent管理页面下载Agent并查看Agent的连接状态。Agent的部署操作在Linux服务器上执行。

针对安装了云助手的Linux系统ECS，您可以通过云助手自动安装Agent，无需登录服务器进行操作。

**操作步骤**

1.  登录数据库审计系统。具体操作请参见[登录系统](cn.zh-CN/用户指南（C100）/登录系统.md#)。
2.  前往**系统管理** \> **Agent管理**页面。
3.  单击安装Agent页签，选择通过云助手自动安装Agent或者下载Agent手动安装。 

    ![Linux安装Agent](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149330_zh-CN.png)

    -   **通过云助手安装**：针对安装了云助手的Linux系统ECS，推荐您使用该方式。该方式操作简便，Agent安装后自动运行。具体操作如下：
        1.  单击**开始安装**。
        2.  在通过云助手安装Agent对话框中，勾选要安装Agent的实例，并单击**安装选中实例**。您也可以单击一个实例操作列下的**安装**，单独为其安装Agent。

            ![云助手安装Agent](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149331_zh-CN.png)

        3.  等待安装完成。

            成功安装后，目标实例的**Agent状态**更新为**运行中，已连接**。

            ![云助手安装成功](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149332_zh-CN.png)

    -   **下载Agent手动安装** 
        1.  在**下载Agent手动安装**区域，单击**Linux**。
        2.  在下载对话框中，等待打包成功，单击**下载**，下载Linux版Agent安装包。

            ![下载安装包](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149333_zh-CN.png)

        3.  登录Linux服务器。
        4.  将下载好的Agent安装包上传到Linux服务器的指定目录，用作解压和运行安装脚本。

            **说明：** 

            -   解压目录中不能出现空格。
            -   每次更换运行或解压目录时，需要重新运行安装脚本。
            ![查看目录](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149334_zh-CN.png)

        5.  运行以下命令，解压Agent安装包。

            ``` {#codeblock_p4y_5x8_vv5}
            tar –xf dbagent_V1.0.tar.gz
            ```

            ![解压安装包](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149335_zh-CN.png)

        6.  运行以下命令，安装并启用Agent。

            ``` {#codeblock_z4n_v66_vnu}
            ./install.sh
            ```

            **说明：** 

            -   禁止直接运行二进制文件。
            -   必须以root账号运行脚本，且指定解释器为bash（或不指定解释器）。
            ![脚本安装Agent](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149336_zh-CN.png)

        7.  Agent安装启用后，回到云盾数据库审计系统，前往**系统管理** \> **Agent管理**页面，在查看Agent状态页签下查看Agent的**连接状态**。

            ![检测安装结果](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149337_zh-CN.png)

            连接状态显示**无异常**，表示成功部署Agent。


**更多操作**

在Linux环境下，您可以根据需要对已部署的Agent程序执行以下操作：

-   卸载：运行安装目录下的uninstall.sh
-   启用：运行安装目录下的dbagent\_start.sh
-   停用：运行安装目录下的dbagent\_stop.sh

![Agent管理脚本](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423249342_zh-CN.png)

## Windows系统部署Agent {#section_4qm_883_o0n .section}

**背景信息**

云盾数据库审计系统的系统管理导航下提供Agent管理功能页面，您可以在Agent管理页面下载Agent并查看Agent的连接状态。Agent的部署操作在Windows服务器上执行。

**操作步骤**

1.  登录数据库审计系统。具体操作请参见[登录系统](cn.zh-CN/用户指南（C100）/登录系统.md#)。
2.  前往**系统管理** \> **Agent管理**页面。
3.  单击安装Agent页签，并在**下载Agent手动安装**区域，单击**Windows**。 

    ![安装Agent页面](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149330_zh-CN.png)

4.  在下载对话框中，等待打包成功，单击**下载**，下载Windows版Agent安装包。 

    ![下载Agent](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149333_zh-CN.png)

5.  登录Windows服务器。
6.  将Agent安装包上传到Windows服务器。 

    ![Agent安装包](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423249338_zh-CN.png)

7.  将压缩包解压到指定的运行目录。 

    **说明：** 

    -   解压目录中不能出现空格等特殊字符，具体包括：`<space>()[]{}^=;!'+,`~(&()`。若一定要在含特殊字符的目录中运行脚本，请选择以管理员权限进入dos命令行运行脚本。
    -   每次更换运行或解压目录时，需要重新运行安装脚本。
8.  进入**dbagent** \> **tool**目录，双击运行install\_npcap.bat，打开Npcap工具安装向导。Npcap是流量代理运行所依赖的工具，需要优先安装。
9.  根据Npcap工具安装向导，使用默认配置完成Npcap安装。 

    **说明：** 您需要管理员权限才能完成Npcap安装。

    ![安装Npcap](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423249339_zh-CN.png)

10. Npcap安装完成后，回到dbagent目录，以管理员身份运行install.bat，安装并启用Agent程序。 

    **说明：** 

    -   禁止直接运行二进制文件。
    -   必须以管理员权限运行脚本。
    -   如需自行更改配置文件，请勿更改文件的编码格式。
    ![Windows安装Agent](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423249340_zh-CN.png)

11. 等待Agent安装完成。Agent安装完成后自动启用。 

    **说明：** 安装过程中遇到问题时，建议您尝试以下方法：等待一段时间重试、卸载Agent并重装、重新启动电脑、直接联系我们。

12. Agent程序安装启用后，回到云盾数据库审计系统，前往**系统管理** \> **Agent管理**页面，在查看Agent状态页签下查看Agent的连接状态信息。 

    ![查看安装结果](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423149337_zh-CN.png)

    连接状态显示**无异常**，表示成功部署Agent。

    **说明：** 若要强制结束dbagent进程，请先结束monitor进程，再结束agent进程。


**更多操作**

在Windows环境下，您可以根据需要对已部署的Agent程序执行以下操作：

-   卸载：运行安装目录下的uninstall.bat
-   启用：运行安装目录下的dbagent\_start.bat
-   停用：运行安装目录下的dbagent\_stop.bat

![Windows的Agent管理脚本](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/475372/156801423249341_zh-CN.png)

## 下一步 {#section_5r7_rii_hcu .section}

部署Agent程序后，您可以前往数据库审计系统的总览页面，查看目标数据库的整体安全状态。具体操作请参见[总览](cn.zh-CN/用户指南（C100）/总览.md#)。

