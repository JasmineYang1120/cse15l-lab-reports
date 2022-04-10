# CSE 15L Lab Report 1
## Logging into a Course-Specific Account on ieng6
### Step 1 - Installing Visual Studio Code

- Go to [Visual Studio Code's website](https://code.visualstudio.com/).
- Choose and install the version (OSX (for Macs) and Windows (for PCs)) for your computer.
- After the installation, you should open a window like this:
- 

### Step 2 - Remotely Connecting
- Go to [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) and look up your course-specific account for CSE15L.
- Open a terminal in VSCode and type **$ ssh cs15lsp22zz@ieng6.ucsd.edu** on your command but with your username replacing the **zz**.
- After doing so you will see a message "**Are you sure you want to continue connecting (yes/no/[fingerprint])?**", type yes and press enter, then enter your password.
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
- Here's an image of running ls-a, which will list all the files including the hidden ones.
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
- In the terminal, run **scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/**. Again, replace **zz** with your username. 
- Enter your password again and log into ieng6 with ssh again. 
- Try use **ls** to see if it is in your home directory and run your file on the ieng6 computer with javac and java.
- You should see this after finsih doing this step:
- 

### Step 5 - Setting an SSH Key
- 
### Step 6 - Optimizing Remote Running

