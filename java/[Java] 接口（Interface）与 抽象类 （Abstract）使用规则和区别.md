# 接口（Interface）

> 是**抽象方法的集合**，接口通常以interface来声明。
> 
> 一个类通过继承接口的方式，从而来继承接口的抽象方法。
**接口并不是类**，编写接口的方式和类很相似，但是它们属于不同的概念。　　

>**类描述对象的属性和方法。接口则包含类要实现的方法**。
除非实现接口的类是抽象类，否则该类要定义接口中的所有方法。　

>**接口无法被实例化，但是可以被实现**。一个实现接口的类，必须实现接口内所描述的所有方法（**所有方法都是抽象的方法**），否则就必须声明为抽象类。　

>接口**没有构造方法，支持多重继承**，不能包含成员变量，除了static和final变量。


接口的申明方法

	

```
[可见度] interface 接口名称 [extends 其他的类名] {
         //任何类型 final, static 字段
        
        public [返回类型] [函数名] ();
        // 抽象方法（所有都是 public）
}
```

　　接口是**隐式抽象**的，当声明一个接口和接口中方法的时候，不必使用abstract关键字。接口中的方法都是公有的。


 　　类使用implements关键字实现接口。在类声明中，Implements关键字放在class声明后面。
 　　

```
... implements 接口名称[, 其他接口, 其他接口..., ...] ...
```

重写接口中的方法时，需注意：

　　类在实现接口的方法时，**不能抛出强制性异常**，只能在接口中，或者继承接口的抽象类　中抛出该强制性异常。
　　
　　类在重写方法时要**保持一致的方法名**，并且应该保持相同或者相兼容的返回值类型。

　　一个类只能继承一个类，但是**能实现多个接口**，同时一个接口能继承另一个接口。

　　**一个接口能继承另一个接口**，和类之间的继承方式比较相似。接口的继承使用　extends　关键字，**子接口继承父接口的方法**。
　　

# 抽象类 （Abstract）

> 　在面向对象的概念中，所有的对象都是通过类来描绘的，但是反过来，**并不是所有的类都是用来描绘对象的**，如果一个类中**没有包含足够的信息**来描绘一个具体的对象，这样的类就是抽象类。

>　　抽象类除了**不能实例化对象**之外，类的其它功能依然存在，成员变量、成员方法和构造方法的访问方式和普通类一样。抽象类必须被继承，才能被使用。（它没有足够信息描绘一个对象，只有等子类来继承完善后才能使用）



在Java语言中使用abstract class来定义抽象类。

```
public abstract class Employee
{　　　
		／／成员变量
		／／成员方法，可以是抽象的或实现的（可以没有抽象方法）
		
		［访问权限修饰符］ abstract ［返回类型］　［函数名］();
｝

```


声明抽象方法会造成以下两个结果：

　　如果一个类包含抽象方法，那么该类必须是抽象类。但是一个抽象类可以没有抽象方法，只是把类申明为抽象的。
　　
　　任何子类**必须重写父类的抽象方法**（一句话抽象方法都要重写，只不过接口的方法全部都是抽象的而已），或者声明自身为抽象类。


# 区别

　　接口不是类，抽象类是一个功能不齐全的类，都不能实例化对象。

　　一个类可以实现（implements）多个接口。一个类只能继承（extends）一个抽象类。

	

　　 接口没有构造函数，所有方法都是 public abstract的，一般不定义成员变量。（所有的成员变量都是 static final ，而且必须显示初始化）。
　　抽象类除了不能实例化对象之外，类的其它功能依然存在，成员变量、成员方法和构造方法的访问方式和普通类一样。

　　一个实现接口的类，必须实现接口内所描述的所有方法（**所有方法都是抽象的方法**），否则就必须声明为抽象类。　
　　如果一个类包含抽象方法，那么该类必须是抽象类。任何子类必须重写父类的抽象方法，或者声明自身为抽象类。
	

