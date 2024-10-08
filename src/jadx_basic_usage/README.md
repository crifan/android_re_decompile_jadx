# jadx基本用法

## 命令行：`jadx`

* 命令行：`jadx`
  * 处理`apk`
    * 基本用法
      * 语法
        ```bash
        jadx -d output_folder your_apk_file.apk
        ```
      * 举例
        ```bash
        jadx/jadx-0.9.0/bin/jadx -d from_jadx_command xiaohuasheng-v1.5.apk
        jadx/jadx-0.9.0/bin/jadx -d exported_java_src mafengwo_ziyouxing.apk
        ```
    * 典型用法
      * 语法
        ```bash
        jadx --show-bad-code --comments-level debug -d outputFolder yourAndroidApp.apk
        ```
        * 说明
          * `--show-bad-code`：显示更多（即使只是部分成功反编译）的代码
            * 否则，会看到提示：
              ```java
              /*
                  Code decompiled incorrectly, please refer to instructions dump.
                  To view partially-correct add '--show-bad-code' argument
              */
              ```
              * 目的：这样可以输出更多反编译代码，即使只是部分反编译成功，但是也值得参考和研究，比（遇到部分代码反编译错误，就整段代码）完全不输出要好
          * `--comments-level debug`：
            * 否则会看到提示
              ```java
              /*
                  Method dump skipped, instructions count: 330
                  To view this dump add '--comments-level debug' option
              */
              ```
  * 处理`dex`
    * 语法
        ```bash
        jadx -d output_folder your_dex_file.dex
        ```
    * 举例
      ```bash
      jadx-0.9.0/bin/jadx some_dex_file.dex -d .
      jadx-1.0.0/bin/jadx com.ishowedu.child.peiyin8392664.dex -d com.ishowedu.child.peiyin8392664_java
      ```

## GUI：`jadx-gui`

使用方式：双击`bin/jadx-gui`，即可打开界面

### 用`jadx-gui`导出全部代码

`文件 -> 全部保存`

![jadx_gui_file_save_all](../assets/img/jadx_gui_file_save_all.png)

即可下载到：

* 各种资源：`resources`
* 源码：`sources`
  * 其中的`sources`，和`文件 -> 另存为Gradle项目`所导出的代码是一样的

![jadx_exported_resources_sources](../assets/img/jadx_exported_resources_sources.png)

其中就有我们希望的app的业务逻辑的代码：

![jadx_sources_app_logic_code](../assets/img/jadx_sources_app_logic_code.png)
