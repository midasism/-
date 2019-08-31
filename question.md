### 编程问题

1. IDEA注释中文字体错误
解决方法：打开IDEA安装目录/jre32/lib，找到 fontconfig.properties.src，
把开头为allfonts.chinese的语句值全部修改成需要的字体，例如 Microsoft YaHei
allfonts.chinese-ms936=Microsoft YaHei ...

