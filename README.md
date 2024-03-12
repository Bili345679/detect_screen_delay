# 对比屏幕间延迟
使用说明 | [HOW TO USE](https://github.com/Bili345679/Compare_screen_delay/blob/main/README_EN.md)

这个程序会在每个屏幕上生成一个最大化窗口，显示从 `time.perf_counter()` 获取的时间，以及基于该时间的时间进度条。在进度条中，`#` 代表该秒已经过的毫秒数，而 `.` 代表该秒未经过的毫秒数。

## 测试方法

为了对比屏幕间延迟，您需要使用快门时间小于 1/1000 的相机同时拍摄所有屏幕。部分手机可以通过以下步骤来调整快门时间并拍摄照片：

1. 打开相机应用。
2. 进入专业模式。
3. 调整快门时间为 1/1000。
4. 拍摄照片。

## 进度条设置

由于进度条可能会影响显示时间，造成屏幕间延迟不准，您可以通过设置来禁用进度条。同样，您可以调整时间尺寸和进度条尺寸，以适应您的窗口大小。

## 设置方法

请在程序的同一目录下创建一个 `config.json` 文件，并按照以下内容进行配置：

```json
{
  "show_ms_array": true,
  "time_size": 250,
  "ms_array_size": 20,
  "refresh_interval": 1
}
```
show_ms_array：是否显示进度条，默认为 true。如果您不想显示进度条，请将其改为 false。<br>
time_size：时间字符尺寸，默认为 250。<br>
ms_array_size：毫秒阵列字符尺寸，默认为 20。<br>
refresh_interval：时间字符与毫秒阵列字符刷新时间间隔，单位为毫秒(ms)，默认值为 1。<br>
