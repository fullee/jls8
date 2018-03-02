### 3.1 Unicode

Programs are written using the Unicode character set. Information about this character set and its associated character encodings may be found at`http://www.unicode.org/`.

Java代码使用Unicode字符集编写. 关于Unicode查看[http://www.unicode.org/](http://www.unicode.org/).

The Java SE platform tracks the Unicode Standard as it evolves. The precise version of Unicode used by a given release is specified in the documentation of the class`Character`.

Java平台与Uncode标准最大可能的保持同步. the class Character的文档中给出了精确的Unicode版本.

> Versions of the Java programming language prior to JDK 1.1 used Unicode 1.1.5. Upgrades to newer versions of the Unicode Standard occurred in JDK 1.1 \(to Unicode 2.0\), JDK 1.1.7 \(to Unicode 2.1\), Java SE 1.4 \(to Unicode 3.0\), Java SE 5.0 \(to Unicode 4.0\), Java SE 7 \(to Unicode 6.0\), and Java SE 8 \(to Unicode 6.2\).
>
> JDK1.1 一开始使用Unicode1.1.5. 后续的更新对应的版本JDK 1.1 \(to Unicode 2.0\), JDK 1.1.7 \(to Unicode 2.1\), Java SE 1.4 \(to Unicode 3.0\), Java SE 5.0 \(to Unicode 4.0\), Java SE 7 \(to Unicode 6.0\), and Java SE 8 \(to Unicode 6.2\)

The Unicode standard was originally designed as a fixed-width 16-bit character encoding. It has since been changed to allow for characters whose representation requires more than 16 bits. The range of legal code points is now U+0000 to U+10FFFF, using the hexadecimal_U+n notation_. Characters whose code points are greater than U+FFFF are called supplementary characters. To represent the complete range of characters using only 16-bit units, the Unicode standard defines an encoding called UTF-16. In this encoding, supplementary characters are represented as pairs of 16-bit code units, the first from the high-surrogates range, \(U+D800 to U+DBFF\), the second from the low-surrogates range \(U+DC00 to U+DFFF\). For characters in the range U+0000 to U+FFFF, the values of code points and UTF-16 code units are the same.

Unicode标准最初的设计是一个字符固定为16bit\(2byte\).后来修改为允许超过16bit.十六进制表示范围`\u0000`到`\uFFFF`

超过`\uFFFF`被称为补充字符.用16bit标识完成的字符范围,这个Unicode被称为UTF-16......

The Java programming language represents text in sequences of 16-bit code units, using the UTF-16 encoding.

Java代码表示为16bit的字符文本.使用UTF-16编码.

Some APIs of the Java SE platform, primarily in the`Character`class, use 32-bit integers to represent code points as individual entities. The Java SE platform provides methods to convert between 16-bit and 32-bit representations.

Java平台的一些API,主要在Character类,使用32bit表示码点作为单独的实体.Java SE平台提供了在16位和32位表示之间进行转换的方法。

This specification uses the terms _code point _and _UTF-16 code unit _where the representation is relevant, and the generic term _character _where the representation is irrelevant to the discussion.



Except for comments \([§3.7](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.7)\), identifiers, and the contents of character and string literals \([§3.10.4](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.10.4),[§3.10.5](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.10.5)\), all input elements \([§3.5](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.5)\) in a program are formed only from ASCII characters \(or Unicode escapes \([§3.3](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.3)\) which result in ASCII characters\).



> ASCII \(ANSI X3.4\) is the American Standard Code for Information Interchange. The first 128 characters of the Unicode UTF-16 encoding are the ASCII characters.
>
> Unicode UTF-16编码的前128个字符是ASCII字符。



