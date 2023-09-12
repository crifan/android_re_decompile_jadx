# 相关页面

## 菜单栏

* View
  * ![jadx_gui_view](../assets/img/jadx_gui_view.png)
* Navigation
  * ![jadx_gui_navigation](../assets/img/jadx_gui_navigation.png)
* Tools
  * ![jadx_gui_tools](../assets/img/jadx_gui_tools.png)
* Help
  * ![jadx_gui_help](../assets/img/jadx_gui_help.png)

## View视图

### 显示内存使用

勾选：`View`->`Show memory usage bar`

可以在底部显示JADX的内存使用量：

* ![jadx_gui_view_show_mem](../assets/img/jadx_gui_view_show_mem.png)

-》估计是防止，反编译太大的apk，导致内存占用太多，而导致崩溃时，至少知道是内存方面的问题。

### 调试进程

`Tool`->`Select a process to debug`

![jadx_gui_select_process_debug](../assets/img/jadx_gui_select_process_debug.png)

或点击：

工具栏中bug虫子的图标：

![jadx_gui_icon_bug](../assets/img/jadx_gui_icon_bug.png)

可以打开：

ADB调试窗口：

![jadx_gui_debug_adb_window](../assets/img/jadx_gui_debug_adb_window.png)

此处自动找到了：

* ADB的path
* ADB的Address 和port

以及：

目标安卓设备中，（debuggable）可以调试的进程 = 此处是自己之前AS调试安装过的一个app：KeepAliveAndroid的相关进程

### 日志查看器

* 打开`Log Viewer`=`日志查看器`的方式
  * `Help`->`Log Viewer`
    * ![jadx_gui_help_log_viewer](../assets/img/jadx_gui_help_log_viewer.png)
  * 工具栏中点击：日志图标
    * ![jadx_gui_tool_icon_log](../assets/img/jadx_gui_tool_icon_log.png)

可以打开：日志查看器

![jadx_gui_show_log_info](../assets/img/jadx_gui_show_log_info.png)
