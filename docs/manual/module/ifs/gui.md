# 模块 gui
输入输出处理模块

使用方法：
```JavaScript
var gui = require('gui');
```
## 函数
        
### setVersion
设置 [WebView](../../object/ifs/WebView.md) 内 ie 模拟版本
```JavaScript
static gui.setVersion(Integer ver);
```

调用参数:

--------------------------
### open
打开一个窗口并访问指定网址
```JavaScript
static WebView gui.open(String url) async;
```

调用参数:
* url - 指定的网址，，可以使用 fs:path 访问本地文件系统

返回结果:
* 返回打开的窗口对象

--------------------------
打开一个窗口并访问指定网址
```JavaScript
static WebView gui.open(String url,
                Map opt) async;
```

调用参数:
* url - 指定的网址，，可以使用 fs:path 访问本地文件系统
* opt - 打开窗口参数

返回结果:
* 返回打开的窗口对象

支持以下参数:
```JavaScript
{
    "left": 100, // 窗口左上角 x，缺省系统自动设定
    "right": 100, // 窗口左上角 y，缺省系统自动设定
    "width": 100, // 窗口宽度，缺省系统自动设定
    "height": 100, // 窗口高度，缺省系统自动设定
    "border": true, // 是否有边框，缺省有边框
    "caption": true, // 是否有标题栏，缺省有标题栏
    "resizable": true, // 是否可改变尺寸，缺省可以改变
    "maximize": false, // 是否最大化显示，缺省不最大化
    "visible": true, // 是否显示，缺省显示
    "debug": false // 是否提示页面错误，缺省不提示
}
```
当设定 width 和 height，而未设定 left 或 right 时，窗口将自动居中

## 常量
        
### IE7
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 ie7
```JavaScript
const gui.IE7 = 7000;
```

--------------------------
### IE8
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 ie8
```JavaScript
const gui.IE8 = 8000;
```

--------------------------
### IE9
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 ie9
```JavaScript
const gui.IE9 = 9000;
```

--------------------------
### IE10
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 ie10
```JavaScript
const gui.IE10 = 10000;
```

--------------------------
### IE11
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 ie11
```JavaScript
const gui.IE11 = 11000;
```

--------------------------
### EDGE
[WebView](../../object/ifs/WebView.md) ie 模拟版本，指定 edge
```JavaScript
const gui.EDGE = 11001;
```
