## 1.2 例子

本书中给出的示例程序都通过了编译,并且能够运行,如下:

```java
class Test { 
    public static void main(String[] args) { 
        for (int i = 0; i < args.length; i++) 
            System.out.print(i == 0 ? args[i] : " " + args[i]); 
        System.out.println(); 
    } 
}
```

这个类存储在Test.java中,在安装有JDK的电脑上可以使用下面命令执行:

```shell
javac Test.java
java Test Hello,world.
```

输出:

```shell
Hello,world.
```



