## 第三章 词法结构

origin: [https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html\#jls-3.1](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.1)

THIS chapter specifies the lexical structure of the Java programming language.

本章介绍Java的词法结构.

Programs are written in Unicode \(§3.1\), but lexical translations are provided \(§3.2\) so that Unicode escapes \(§3.3\) can be used to include any Unicode character using only ASCII characters. Line terminators are defined \(§3.4\) to support the different conventions of existing host systems while maintaining consistent line numbers.

代码用Unicode编写,但是提供了转义功能,所以任何Unicode,ASCII字符都可以被使用. 行结束符适配不同的操作系统,保证了行号的一致.

The Unicode characters resulting from the lexical translations are reduced to a sequence of input elements \(§3.5\), which are  white space \(§3.6\), comments \(§3.7\),and tokens. The tokens are the identifiers \(§3.8\), keywords \(§3.9\), literals \(§3.10\),separators \(§3.11\), and operators \(§3.12\) of the syntactic grammar.

