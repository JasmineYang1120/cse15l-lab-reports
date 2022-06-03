# CSE 15L Lab Report 5

## Test 1
- [link for test1](https://github.com/JasmineYang1120/markdown-parser/blob/main/test-diff-1.md)
- My implementation:

  ![image](https://user-images.githubusercontent.com/103228511/171760583-b8b59312-56d4-4a76-a54d-81f5ab02f142.png)

- Lab 9 implementation:

  ![image](https://user-images.githubusercontent.com/103228511/171762087-59083736-61b9-4f48-9b72-b42297d6e4e9.png)

- For test1, my implementation provided the correct output while Lab 9 implementation did not. 
- According to the CommonMark demo site, the expected output should be:
```
[/uri "title"]
```
![image](https://user-images.githubusercontent.com/103228511/171761525-b68e62bd-7160-4d50-a75b-3a06de77362e.png)

- The bug in the implementation of lab 9 is that as shown below with the screenshot, the && should changed to || or else this condition will never be fufilled. 
  Therefore, the potentialLink could not be added to toReturn, and as the condition of the while loop is fulfill with currentInde greater than the length of the markdown, toReturn is return with an empty Arraylist. 
  
  ![image](https://user-images.githubusercontent.com/103228511/171767479-0ed389a8-974e-40f0-95ff-e5e3102bc057.png)




## Test 2
- [link for test2](https://github.com/JasmineYang1120/markdown-parser/blob/main/test-diff-2.md)

- My implementation:

![image](https://user-images.githubusercontent.com/103228511/171761164-0fd7eb22-bb8a-4458-8f39-7167dc3d5f94.png)

- Lab 9 implementationL:

![image](https://user-images.githubusercontent.com/103228511/171767993-92d384de-6e08-4740-9bc9-89abc566bdc8.png)

- For test2, lab 9 implementation provided the correct output while my implementation did not. 
- According to the CommonMark demo site, the expected output should be:
```
[]
```
  ![image](https://user-images.githubusercontent.com/103228511/171768136-67106e14-aeeb-469e-8f00-7bb0565b7d6b.png)

- The bug of my implementation is that my code can not analyze if the string in the file is a link or a picture since the format of the picture also has [] and (). 
  To solve this error, an if statement could be added before the highlighted if statement with the condition that if the string contains all ![]() and in order, then return an empty arraylist. 
  ![image](https://user-images.githubusercontent.com/103228511/171769037-5d3ce629-dda0-4118-b8a1-50854435670e.png)

## Finding different test results
- My partner used vimdiff on the results of running a bash for loop to find tests with different results in lab, however, I could not successfully performed that with my laptop.
  Therefore, for the lab report, I search through manually, which is time consuming.

