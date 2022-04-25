# CSE 15L Lab Report 2
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
- The extra close parenthesis in the link2 of test-file-1.md will cause the code to enter an infinite loop, which leads to the result shown above with OutofMemoryError. A break statement is required to end the while loop.  
## Code Change #2
![image](https://user-images.githubusercontent.com/103228511/165004179-20544427-af8b-42b6-8d23-3f7b9f3678cb.png)
- [test-file-2.md](https://github.com/JasmineYang1120/markdown-parser/commit/a3785abc8c4bf47a308938c8389dad51806de661)
- ```
   Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOf(Arrays.java:3721)
        at java.base/java.util.Arrays.copyOf(Arrays.java:3690)
        at java.base/java.util.ArrayList.grow(ArrayList.java:235)
        at java.base/java.util.ArrayList.grow(ArrayList.java:242)
        at java.base/java.util.ArrayList.add(ArrayList.java:452)
        at java.base/java.util.ArrayList.add(ArrayList.java:465)
        at MarkdownParse.getLinks(MarkdownParse.java:19)
        at MarkdownParse.main(MarkdownParse.java:40)
        ```
- The extra open and close parenthesis after the link in test-file2.md will cause the code to enter infinite loop because it does not expected the parenthesises to appear again. This leads to the result shown above with OutofMemoryError.
## Code Change #3
![image](https://user-images.githubusercontent.com/103228511/165006853-dcbf40ee-690c-46ee-9bde-104a4f5cbdb9.png)
- [test-file-3.md](https://github.com/JasmineYang1120/markdown-parser/commit/8502bf8e48f419b52a53eb6a8db645e64ec6495c)
- ```
   Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOf(Arrays.java:3721)
        at java.base/java.util.Arrays.copyOf(Arrays.java:3690)
        at java.base/java.util.ArrayList.grow(ArrayList.java:235)
        at java.base/java.util.ArrayList.grow(ArrayList.java:242)
        at java.base/java.util.ArrayList.add(ArrayList.java:452)
        at java.base/java.util.ArrayList.add(ArrayList.java:465)
        at MarkdownParse.getLinks(MarkdownParse.java:19)
        at MarkdownParse.main(MarkdownParse.java:43)
        ```
- The extra line after the link will cause the code to enter infinite loop because it does not know where to end the loop. A break statemnt is required to stop the loop to prevent it leads to the OutofMemoryError as shown above. 
