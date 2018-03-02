### 3.1 Unicode

Programs are written using the Unicode character set. Information about this character set and its associated character encodings may be found at [http://www.unicode.org/](http://www.unicode.org/).

程序的编写使用了Unicode字符集. 关于Unicode查看[http://www.unicode.org/](http://www.unicode.org/).

The Java SE platform tracks the Unicode Standard as it evolves. The precise version of Unicode used by a given release is specified in the documentation of the class Character.

Java平台与Uncode标准最大可能的保持同步. the class Character的文档中给出了精确的Unicode版本.

> Versions of the Java programming language prior to JDK 1.1 used Unicode 1.1.5. Upgrades to newer versions of the Unicode Standard occurred in JDK 1.1 \(to Unicode 2.0\), JDK 1.1.7 \(to Unicode 2.1\), Java SE 1.4 \(to Unicode 3.0\), Java SE 5.0 \(to Unicode 4.0\), Java SE 7 \(to Unicode 6.0\), and Java SE 8 \(to Unicode 6.2\).
>
> JDK1.1 一开始使用Unicode1.1.5. 后续的更新对应的版本JDK 1.1 \(to Unicode 2.0\), JDK 1.1.7 \(to Unicode 2.1\), Java SE 1.4 \(to Unicode 3.0\), Java SE 5.0 \(to Unicode 4.0\), Java SE 7 \(to Unicode 6.0\), and Java SE 8 \(to Unicode 6.2\)

The Unicode standard was originally designed as a fixed-width 16-bit character encoding. It has since been changed to allow for characters whose representation requires more than 16 bits. The range of legal code points is now U+0000 to U+10FFFF, using the hexadecimal U+n notation. Characters whose code points are greater than U+FFFF are called supplementary characters. To represent the complete range of characters using only 16-bit units, the Unicode standard defines an encoding called UTF-16. In this encoding, supplementary characters are represented as pairs of 16-bit code units, the first from the high-surrogates range,\(U+D800 to U+DBFF\), the second from the low-surrogates range \(U+DC00 to U+DFFF\). For characters in the range U+0000 to U+FFFF, the values of code pointsand UTF-16 code units are the same.

![](/assets/import1.png)

Unicode标准最初的设计是一个字符固定为16bit\(2byte\).后来修改为允许超过16bit.十六进制表示范围`\u0000` 到`\uFFFF`

超过`\uFFFF` 被称为补充字符.用16bit标识完成的字符范围,这个Unicode被称为UTF-16.

