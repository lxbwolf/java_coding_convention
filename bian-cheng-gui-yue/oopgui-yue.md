1. 避免通过一个类的对象引用访问此类的静态变量或静态方法, 无谓增加编译器解析成本.
2. 所有的覆写方法, 必须加@Override注解
3. Object的equals方法容易抛空指针异常, 应使用常量或确定有值的对象来调用equals
	```
	正例:
		"test".equals(object);
	反例:
		object.equals("test");
	```
4. 所有相同类型的包装类对象之间值得比较, 全部使用equals方法比较
5. 构造方法中禁止加入任何业务逻辑, 如果有初始化逻辑, 放在init方法中
6. 当一个类有多个构造方法或多个同名方法, 这些方法应按顺序放置在一起, 此条规则优先于第7条
7. 类内方法定义顺序:
	公有方法/保护方法 > 私有方法 > getter/setter方法
8. setter方法中, 参数名称与类成员变量名称一致, this.成员名 = 参数名. 在getter/setter方法中, 不要增加业务逻辑
	```language
	反例:
		public Integer getData() {
			if (true) {
				return this.data + 100;
			} else {
				return this.data - 100;
			}
		}
	```
9. 循环体内, 字符串的连接方式, 使用StringBuilder的append方法进行扩展.(反编译的字节码显示每次循环都会new出一个StringBuilder对象, 然后进行append操作, 最后通过toString方法返回String对象, 造成内存资源浪费)
	```language
	反例:
		String str = "start";
		for (int i = 0; i < 100; ++i) {
			str = str + "hello";
		}
	```
10. final可以声明类/成员变量/方法/本地变量, 下列情况使用final关键字:
	* 不允许被继承的类, 如String类
	* 不允许修改引用的域对象
	* 不允许被重写的方法
	* 不允许运行过程中重新赋值的局部变量
	* 避免上下文重复使用一个变量, 使用final描述可以强制重新定义一个变量, 方便更好地进行重构
11. 类成员与方法访问控制从严
12. 使用前缀自增/自减