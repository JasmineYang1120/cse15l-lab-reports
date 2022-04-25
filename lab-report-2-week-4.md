# CSE 15L Lab Report 1
## Code Change #1
![image](https://user-images.githubusercontent.com/103228511/164950521-7cdaa0ec-ba89-4ea3-967a-d171131251f7.png)
- [test-file-1.md](https://github.com/JasmineYang1120/markdown-parser/commit/0446132155dbab7ae859644cac3225c533f0f799)
-  ```
   Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOfRange(Arrays.java:4031)
        at java.base/java.lang.StringLatin1.newString(StringLatin1.java:767)
        at java.base/java.lang.String.substring(String.java:1914)
        at MarkdownParse.getLinks(MarkdownParse.java:19)
        at MarkdownParse.main(MarkdownParse.java:35)
      ```
- The extra parenthesis in the link2 of test-file-1.md will cause the code to enter an infinite loop, which leads to the result shown above with OutofMemoryError. A break statement is required to end the while loop.  
## Code Change #2

- [test-file-2.md]()
- ```
   Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOf(Arrays.java:3721)
        at java.base/java.util.Arrays.copyOf(Arrays.java:3690)
        at java.base/java.util.ArrayList.grow(ArrayList.java:235)
        at java.base/java.util.ArrayList.grow(ArrayList.java:242)
        at java.base/java.util.ArrayList.add(ArrayList.java:452)
        at java.base/java.util.ArrayList.add(ArrayList.java:465)
        at MarkdownParse.getLinks(MarkdownParse.java:19)
        at MarkdownParse.main(MarkdownParse.java:35)
        ```
## Code Change #3
