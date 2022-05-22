# CSE 15L Lab Report 3
- [Link to my markdown-parse repository](https://github.com/JasmineYang1120/markdown-parser)
- [Link to the code my group reviewed in week 7:](https://github.com/kcyy127/markdown-parser)

## Snippet 1
```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

- Expected output:
```
[google.com, google.com, ucsd.edu]
```

- Code in MarkdownParseTest.java:
<img width="385" alt="lab4-1" src="https://user-images.githubusercontent.com/103228511/169680967-636e7638-8ffa-42e9-b07f-df7c641f7d95.PNG">

- Output of my implementation:
It did not passed, and here is the error showed in JUnit.
<img width="512" alt="lab4-4" src="https://user-images.githubusercontent.com/103228511/169681140-c0687ef2-0795-410e-a74e-be4e19d97cdb.PNG">

- Output of the implementation you reviewed in Week 7:
- It did not passed either, and here is the error showed in JUnit.
<img width="655" alt="lab4-7" src="https://user-images.githubusercontent.com/103228511/169681480-a88de299-624f-4288-b668-2c641f8b5cfc.PNG">

- I don't think that a small code change will be able to make my program work for snippet 1 and all related cases that use inline code with backticks. My code initially did not involved cases like this so it will be a totally new thing to start with which undoubedly will require many changes and add ons to it. 
## Snippet 2
```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

- Expected output:
```
[a.com, a.com, example.com]
```

- Code in MarkdownParseTest.java:
<img width="371" alt="lab4-2" src="https://user-images.githubusercontent.com/103228511/169681042-446bb18f-52fe-48d2-8a0a-f8bd6942bdb9.PNG">

- Output of my implementation:
It did not passed, and here is the error showed in JUnit.
<img width="464" alt="lab4-5" src="https://user-images.githubusercontent.com/103228511/169681149-405fe43e-3087-4ad9-8eaf-e3932c4afcf7.PNG">

- Output of the implementation you reviewed in Week 7:
- It did not passed either, and here is the error showed in JUnit.
<img width="511" alt="lab4-8" src="https://user-images.githubusercontent.com/103228511/169681490-054f168a-d292-4275-8ce4-b2d84a0fa47b.PNG">

- I do not think that a small code change will be able to make my program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets. Even though my code sucessfully printed out the first link, due to the fact that I wrote a break statement inside the if statements, the code will not goes through the rest of the file, and that definetly needs to be changed. 
## Snippet 3
```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

- Expected output:
```
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
```

- Code in MarkdownParseTest.java:
<img width="533" alt="lab4-3" src="https://user-images.githubusercontent.com/103228511/169680991-d6a06f3c-3b39-4da2-b6f2-6ca505c86fe2.PNG">

- Output of my implementation:
It did not passed, and here is the error showed in JUnit.
<img width="651" alt="lab4-6" src="https://user-images.githubusercontent.com/103228511/169681156-6f9f8282-f7d8-4b5d-bf08-23805e039b76.PNG">

- Output of the implementation you reviewed in Week 7:
- It did not passed either, and here is the error showed in JUnit.
<img width="641" alt="lab4-9" src="https://user-images.githubusercontent.com/103228511/169681497-0f160b74-12eb-4605-804c-5e8e1cb34796.PNG">

- I do no think that a small code change will be able to fix and make my program work for snippet 3 and all related cases that have newlines in brackets and parentheses. My code printed out the first link in the file that was not in the expected output, and agian the break statement stop the code to read the rest of the file so here has the same problem that need to be fixed greatly. 

