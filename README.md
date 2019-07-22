项目为上学时用日历来记录课表

## 环境要求

Python 2.7+

[xlrd](https://pypi.python.org/pypi/xlrd) 


## 执行详解
1、配置 classInfo Excel 表格

在工作目录下创建一个 classInfo Excel 表格，表格表头有如下参数：

className：课程名称

startWeek：起始周

endWeek：结束周

weekday：星期

classTime：第几节。这个参数要配合 conf_classTime.json 文件，下文会讲。

classroom：教室


2、配置 conf_classTime.json

name：每个课程的的节数

startTime：上课时间

endTime：下课时间

```

```
{
  "classTime": [
    {
        "name":"第 1、2 节",
        "startTime":"0800",
        "endTime":"9050"
    },
    {
        "name":"第 3、4 节",
        "startTime":"1010",
        "endTime":"1200"
    },
    {
        "name":"第 7、8 、9节",
        "startTime":"1430",
        "endTime":"1720"
    },
    {
        "name":"第 10 节",
        "startTime":"1730",
        "endTime":"1820"
    },
    {
        "name":"第 11、12、13 节",
        "startTime":"1910",
        "endTime":"2200"
    }
  ]
}
```

```



3、运行 excelReader.py 脚本

终端运行：
cd 切换到文件所在目录
python excelReader.py

完成后生成一个 conf_classInfo.json 配置文件


4、运行 main.py 脚本

终端运行：
cd 切换到文件所在目录
python main.py

完成后在工作目录下会生成一个 class.ics 文件

5、打开 class.ics 文件
