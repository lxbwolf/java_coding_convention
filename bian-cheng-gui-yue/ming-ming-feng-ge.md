1. 代码中的命名均不能以下划线或者美元符号开始/结束
	```
	反例:
		_name
		__name
		$Object
		name_
		name$
		Object$
	```
2. 禁止使用拼音
3. 类名使用UpperCamelCase风格
	```language
	正例:
		MarcoPolo
		UserDO
		XmlService
		TcpUdpDeal
		TaPromotion
	反例:
		marcoPolo
		UserDo
		XMLService
		TCPUDPDeal
		TAPromotion
	```
4. 方法名, 参数名, 成员变量, 局部变量 使用lowerCamelCase风格
	```language
	正例:
		localValue
		getHttpMessage()
		inputUserId
	```
5. 常量名全部大写, 单词间用下划线连接
	```language
	正例: MAX_STOCK_COUNT
	```
6. 中括号是数组类型的一部分, 数组定义如下:
	`String[] args`
	不使用`String args[]` 方式定义
7. POJO类中布尔类型的变量不加is
8. 包名使用小写, 点分隔符之间有且仅有一个自然语义的英文单词. 包名使用单数形式.
9. 禁止完全不规范的缩写. 任何自定义编程元素在命名时, 使用尽量完整的单词组合来表达其意.
	```language
	正例:
		AbstractClass
		condition
	反例:
		AbsClass
		condi
	```
10. 接口类中的方法和属性不加包括public在内的任何修饰符号, 并加上有效的Javadoc注释, 保持代码的简洁性. 尽量不在接口里定义变量.
	```language
	正例:
		void f();
		String COMPANY = "something";
	反例:
		public abstract void f();
	```
11. 实现类用Impl后缀. 形容能力的接口, 取对应的形容词作接口名
	```language
	正例:
		CacheServiceImpl // 实现CacheService接口
		AbstractTranslator // 实现Translatable
	```
12. 枚举类 成员名称全部大写, 单词间用下划线连接
13. 方法命名规约:
	```language
	获取单个对象用get前缀
	获取多个对象用list前缀
	获取统计值用count前缀
	插入用save/insert前缀
	删除用remove/delete前缀
	修改用update前缀
	```












