### 4.1 The Kinds of Types and Values

```
Type:
PrimitiveType
ReferenceType
```

这两种类型是原始类型和引用类型,两种类型的值都存储在变量中,通过入参,方法的返回值来操作这两种类型.

还有一个特殊的null,它没有名字.正因如此,不可以声明一个null类型的变量,也不能把其它类型cast to the null type.

错误示范:

> null abc = null;
>
> Integer a = 1;
>
> null na = \(null\)a;

空引用是null类型表达式的唯一可能值。

> Integer a = null;

空引用可以赋值或转化为任意引用类型。

> Integer a = null;
>
> Integer b = a;
>
> Object c = \(Objcet\)b;



> In practice, the programmer can ignore the null type and just pretend that null is merely a special literal that can be of any reference type.
>
> 程序员可以忽略null,或者当做任意引用类型的字符串



