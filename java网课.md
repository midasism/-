####  常用类库
1. Date 日期类
	
* 
	
2. Calendar 日历类（抽象类）
	* 使用子类 GregorianCalendar 创建对象（默认使用当前系统时间）
	* setTime（Date date）：设置时间
	* set（年月日对应静态常量，value）：单独设置年月日
	* getTime（）：获取当前时间
	* get（年月日对应静态常量）：单独获取年月日的值
	* getTime（）同 Date类

3. DateFormat
	* 常用的是 SimpleDateFormat 类
	* 格式化时间：SimpleDateFormat xx = new SimpleDateFormat（String pattern）;
	例：pattern = "yyyy-MM-dd  HH-mm-ss"
	* String format（Date date）：提供时间，返回格式化后的字符串
	* Date  parse（String time）：将字符串解析为 Date 对象

4. NumberFormat 数字格式化抽象类
	* 通常使用子类 DecimalFormat 格式化或者解析数字
	* 例： 处理金额：DecimalFormat xx = new DecimalFormat（"#,###,###.00"）；
	* String format（）：数字格式化为字符串
	* Number parse（）：将字符串解析为数字