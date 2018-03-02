### 3.2. Lexical Translations

A raw Unicode character stream is translated into a sequence of tokens, using the following three lexical translation steps, which are applied in turn:

1. A translation of Unicode escapes \([§3.3](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.3)\) in the raw stream of Unicode characters to the corresponding Unicode character. A Unicode escape of the form`\uxxxx`, where`xxxx`_\_is a hexadecimal value, represents the UTF-16 code unit whose encoding is_`xxxx`\_. This translation step allows any program to be expressed using only ASCII characters.

2. A translation of the Unicode stream resulting from step 1 into a stream of input characters and line terminators \([§3.4](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.4)\).

3. A translation of the stream of input characters and line terminators resulting from step 2 into a sequence of input elements \([§3.5](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.5)\) which, after white space \([§3.6](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.6)\) and comments \([§3.7](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.7)\) are discarded, comprise the tokens \([§3.5](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.5)\) that are the terminal symbols of the syntactic grammar \([§2.3](https://docs.oracle.com/javase/specs/jls/se8/html/jls-2.html#jls-2.3)\).

The longest possible translation is used at each step, even if the result does not ultimately make a correct program while another lexical translation would. There is one exception: if lexical translation occurs in a type context \([§4.11](https://docs.oracle.com/javase/specs/jls/se8/html/jls-4.html#jls-4.11)\) and the input stream has two or more consecutive`>`characters that are followed by a non-`>`character, then each`>`character must be translated to the token for the numerical comparison operator`>`.

```text
The input characters a--b are tokenized (§3.5) as a, --, b, which is not part of any grammatically correct program, 
even though the tokenization a, -, -, b could be part of a grammatically correct program.

Without the rule for>characters, two consecutive>brackets in a type such as List<List<String>>would be tokenized 
as the signed right shift operator>>, while three consecutive>brackets in a type such as List<List<List<String>>> 
would be tokenized as the unsigned right shift operator>>>. Worse, the tokenization of four or more 
consecutive>brackets in a type such as List<List<List<List<String>>>> would be ambiguous, 
as various combinations of>,>>, and>>>tokens could represent the>>>>characters.
```



