# CSE 15L Lab Report 3
## Streamlining ssh Configuration
- To save time from typing the long line to log into ieng6, put an entry in the configuration files in ssh. 
- Screenshot of my .ssh/config file:

![image](https://user-images.githubusercontent.com/103228511/167316849-d34eb0a2-5af6-4cb1-aa7a-07cd8738a190.png)

- Screenshot of logging into the course specific account with the ssh command.

![image](https://user-images.githubusercontent.com/103228511/167317056-2d5ecf89-7aab-4650-ac4b-217a55f1aa49.png)

- Screenshot of using scp to copy one of the file:
![image](https://user-images.githubusercontent.com/103228511/167317296-89126910-a273-4113-b342-045e43495f9f.png)

## Setup Github Access from ieng6
- To setup Github access from ieng6, I created a key with the course specific account and added new ssh to Github. 
- Screenshot of my SSH public key stored in Github:

![image](https://user-images.githubusercontent.com/103228511/167319660-c188d376-3cc6-4b84-99e6-7e65d340f418.png)

- Screenshot of my SSH public and private id_rsa key stored in my user account (C:\Users\User\.ssh):

![image](https://user-images.githubusercontent.com/103228511/167319784-3287dd32-718d-43c6-b02e-ebe938dece63.png)

- Screenshot of running git commands to commit and push a change to Github while logged into the ieng6 account.

<img width="568" alt="擷取 lab 3" src="https://user-images.githubusercontent.com/103228511/168523921-29a3eb98-a63a-40d2-9716-841c94788f6d.PNG">

[The link for the resulting commit](https://github.com/JasmineYang1120/cse15l-lab-reports/commit/ba62b9966a1db51d4d6725b402638d7cd80ab6c7)

## Copy whole directories with scp -r
- To copy the whole directory, this is what I typed:
```
$ scp -r . cs15lsp22@ieng6.ucsd.edu:~/markdown-parse
```
- The -r means to work recursively. 
- Screenshot of copying the whole markdown-parse directory to my ieng6 account.

<img width="530" alt="擷取 lab3-1" src="https://user-images.githubusercontent.com/103228511/168523588-07fc0ec2-ffda-4bdc-ad36-633a6914d5a1.PNG">

- Sceenshot of logging into the ieng6 account and complie and run the tests.

<img width="570" alt="擷取 lab3-2" src="https://user-images.githubusercontent.com/103228511/168523554-b3f9250b-bd2e-4a29-b0d8-857972d9d4e7.PNG">

- Screenshot of combining scp, ;, and ssh to copy the whole directory and run the tests in one line.

<img width="487" alt="擷取 lab3-3" src="https://user-images.githubusercontent.com/103228511/168523810-1e5f41f8-4e79-4d51-9387-77abb7157cc8.PNG">


