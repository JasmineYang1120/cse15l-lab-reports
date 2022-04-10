# CSE 15L Lab Report 1
## Logging into a Course-Specific Account on ieng6
### Step 1 - Installing Visual Studio Code

- Go to [Visual Studio Code's website](https://code.visualstudio.com/).
- Choose and install the version (OSX (for Macs) and Windows (for PCs)) for your computer.
- After the installation, you should open a window like this:
- 

### Step 2 - Remotely Connecting
- Go to [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) and look up your course-specific account for CSE15L.
- Open a terminal in VSCode and type ```$ ssh cs15lsp22zz@ieng6.ucsd.edu ``` 
 on your command but with your username replacing the **zz**.
- After doing so you will see a message "**Are you sure you want to continue connecting (yes/no/[fingerprint])?**", type yes, press enter, and enter your password.
- You should see this after finsih doing this step:
- 
### Step 3 - Trying Some Commands
- Try running some of the comands on your computer. 
- Dicuss and record what you see. 
- Useful commands to try on include:
  1. cd ~
  2. cd
  3. ls
  4. ls -lat
  5. ls -a
  6. pwd
- Here's an image of running ```ls-a``` , which will list all the files including the hidden ones.
- 

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
- Run the file using javac and java on your computer.
- In the terminal, run ```scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/``` . Again, replace **zz** with your username. 
- Enter your password again and log into ieng6 with ssh again. 
- Try use ```ls``` to see if it is in your home directory and run your file on the ieng6 computer with javac and java.
- You should see this after finsih doing this step:
- 

### Step 5 - Setting an SSH Key
- To set up the SSH keys on your comupter, enter ```$ ssh-keygen``` on your computer. 
- Enter the file to save the key (it should look like /Users/<user-name>/.ssh/id_rsa).
- Next, enter passphrase twice, you should enter empty for no passphrase. 
- After successfully doing the following steps, you will see a randomart image of your key.
- Then, copy the public key to the .ssh directory by log into the account with ssh and enter ```$ mkdir .ssh``` . 
- Last, log out and enter the following in the terminal:
  
  ```$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys```
- You are now able to ssh or scp to the server without entering your password like the image below.
- 
  
### Step 6 - Optimizing Remote Running
- To make a local edit to WhereAmI.java, you can write a command in quotation after the ssh command. 
- Also, you may use semicolons to run multiple commands on the same line.
- For example, you can enter ```$ ssh cs15lsp22zz@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI"``` in this case. 
- You should see:
- 
  


