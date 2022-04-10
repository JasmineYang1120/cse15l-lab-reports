# CSE 15L Lab Report 1
## Logging into a Course-Specific Account on ieng6
### Step 1 - Installing Visual Studio Code

- Go to [Visual Studio Code's website](https://code.visualstudio.com/).
- Choose and install the version (OSX (for Macs) and Windows (for PCs)) for your computer.
- After the installation, you should open a window like this:

 ![image](https://user-images.githubusercontent.com/103228511/162597661-8caf1f49-58de-4ad2-9326-116cdbd6ccc0.png)

### Step 2 - Remotely Connecting
- Go to [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) to look up your course-specific username for CSE15L.
- Open a terminal and type ```$ ssh cs15lsp22zz@ieng6.ucsd.edu ``` 
 on your command but with your username replacing the **zz**.
- After doing so you will see a message "**Are you sure you want to continue connecting (yes/no/[fingerprint])?**", type yes, press enter, and enter your password.
- You should see this after finsih doing this step:

 ![image](https://user-images.githubusercontent.com/103228511/162597774-730f62b4-e4d3-4b5a-bd35-7380c3772c4f.png)

### Step 3 - Trying Some Commands
- Try running some of the commands below on your computer. 
  1. cd ~
  2. cd
  3. ls
  4. ls -lat
  5. ls -a
  6. pwd
- Here's an image of running ```ls-a``` , which will list all the files including the hidden ones.
  ![image](https://user-images.githubusercontent.com/103228511/162597808-b6198151-2da4-44a5-96c2-e001de5510a5.png)

### Step 4 - Moving Files with scp
- Create a file on your computer called WhereAmI.java.
- Enter the following code into the file.
  ```
    class WhereAmI {
      public static void main(String[] args) {
        System.out.println(System.getProperty("os.name"));
        System.out.println(System.getProperty("user.name"));
        System.out.println(System.getProperty("user.home"));
        System.out.println(System.getProperty("user.dir"));
      }
    }
- Run the file using javac and java.
- You should see:

  ![image](https://user-images.githubusercontent.com/103228511/162597863-b82d4d9f-b500-4adf-9247-1d5485128388.png)

- In the terminal, run ```scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/``` . Again, replace **zz** with your username. 
- Enter your password again and log into ieng6 with ssh again. 
- Try use ```ls``` to see if it is in your home directory and run your file on the ieng6 computer with javac and java.
- You should see this after finsih doing this step:
- 
  ![image](https://user-images.githubusercontent.com/103228511/162597871-dec3e723-16c3-4291-816b-88c84c3f1487.png)

### Step 5 - Setting an SSH Key
- To set up the SSH keys on your comupter, enter ```$ ssh-keygen``` on your computer. 
- Enter the file to save the key (it should look like /Users/<user-name>/.ssh/id_rsa).
- Next, enter passphrase twice, you should enter empty for no passphrase. 
- After successfully doing the following steps, you will see a randomart image of your key.
- Then, copy the public key to the .ssh directory by log into the account with ssh and enter ```$ mkdir .ssh``` . 
- Last, log out and enter the following in the terminal:
  
  ```$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys```
- You are now able to ssh or scp to the server without entering your password like the image below.
 
  ![image](https://user-images.githubusercontent.com/103228511/162597881-4b635310-7773-4181-9671-bdd39add15a6.png)

### Step 6 - Optimizing Remote Running
- To make a remote running more convenient, you can write a command in quotation after the ssh command. 
- Also, you may use semicolons to run multiple commands on the same line.
- For example, you can enter ```$ ssh cs15lsp22zz@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI"``` . 
- You should see:
 
  ![image](https://user-images.githubusercontent.com/103228511/162597899-1b97159e-e8c4-4b7a-89f0-e1f045c8b187.png)

  


