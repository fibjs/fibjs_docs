# 对象 File
文件操作对象，用于二进制文件读写

文件操作对象用于对二进制文件进行操作，可使用 [fs](../../module/ifs/fs.md) 模块打开和创建文件：
```JavaScript
var f = fs.open('test.txt');
```
## 函数
        
### chmod
查询当前文件的访问权限，Windows 不支持此方法
```JavaScript
File.chmod(Integer mode) async;
```

调用参数:
* mode - 指定设定的访问权限

--------------------------
### seek
移动文件当前操作位置
```JavaScript
File.seek(Long offset,
                Integer whence);
```

调用参数:
* offset - 指定新的位置
* whence - 指定位置基准，允许的值为：SEEK_SET, SEEK_CUR, SEEK_END

--------------------------
### tell
查询流当前位置
```JavaScript
Long File.tell();
```

返回结果:
* 返回流当前位置

--------------------------
### rewind
移动当前位置到流开头
```JavaScript
File.rewind();
```

--------------------------
### size
查询流尺寸
```JavaScript
Long File.size();
```

返回结果:
* 返回流尺寸

--------------------------
### readAll
从流内读取剩余的全部数据
```JavaScript
Buffer File.readAll() async;
```

返回结果:
* 返回从流内读取的数据，若无数据可读，或者连接中断，则返回 null

--------------------------
### truncate
修改文件尺寸，如果新尺寸小于原尺寸，则文件被截断
```JavaScript
File.truncate(Long bytes) async;
```

调用参数:
* bytes - 新的文件尺寸

--------------------------
### eof
查询文件是否到结尾
```JavaScript
Boolean File.eof();
```

返回结果:
* 返回 True 表示结尾

--------------------------
### flush
将文件缓冲区内容写入物理设备
```JavaScript
File.flush() async;
```

--------------------------
### stat
查询当前文件的基础信息
```JavaScript
Stat File.stat() async;
```

返回结果:
* 返回 Stat 对象描述文件信息

--------------------------
### read
从流内读取指定大小的数据
```JavaScript
Buffer File.read(Integer bytes = -1) async;
```

调用参数:
* bytes - 指定要读取的数据量，缺省为读取随机大小的数据块，读出的数据尺寸取决于设备

返回结果:
* 返回从流内读取的数据，若无数据可读，或者连接中断，则返回 null

--------------------------
### write
将给定的数据写入流
```JavaScript
File.write(Buffer data) async;
```

调用参数:
* data - 给定要写入的数据

--------------------------
### close
关闭当前流对象
```JavaScript
File.close() async;
```

--------------------------
### copyTo
复制流数据到目标流中
```JavaScript
Long File.copyTo(Stream stm,
                Long bytes = -1) async;
```

调用参数:
* stm - 目标流对象
* bytes - 复制的字节数

返回结果:
* 返回复制的字节数

--------------------------
### dispose
强制回收对象，调用此方法后，对象资源将立即释放
```JavaScript
File.dispose();
```

--------------------------
### equals
比较当前对象与给定的对象是否相等
```JavaScript
Boolean File.equals(object expected);
```

调用参数:
* expected - 制定比较的目标对象

返回结果:
* 返回对象比较的结果

--------------------------
### toString
返回对象的字符串表示，一般返回 "[Native Object]"，对象可以根据自己的特性重新实现
```JavaScript
String File.toString();
```

返回结果:
* 返回对象的字符串表示

--------------------------
### toJSON
返回对象的 JSON 格式表示，一般返回对象定义的可读属性集合
```JavaScript
Value File.toJSON(String key = "");
```

调用参数:
* key - 未使用

返回结果:
* 返回包含可 JSON 序列化的值

--------------------------
### valueOf
返回对象本身的数值
```JavaScript
Value File.valueOf();
```

返回结果:
* 返回对象本身的数值

## 属性
        
### name
查询当前文件名
```JavaScript
readonly String File.name;
```
