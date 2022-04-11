<h1 align = "center">
   <span style ="color:red">Week 2 Lab Report</span>
</h1>

<h2 align = "center">
    <span style = "font-size: 30px">Introduction</span>
</h2>

<span style = "font-size: 20px; font-family:Arial"> Hello everyone, This is a tutorial of how to log into a course-specific account on <span style = "color:green">ieng6</span>.</span>

<h3 align = "center">
    <span style = "font-size:30px"> Installing Visual studio code</span>
    </h3>

<span style = "font-size: 18px; font-family:Arial">
    Vs code is a useful tool for CSE 15L, and here is how you get it.
</span>

* <span style = "font-size: 18px"> Click on [this Link](https://code.visualstudio.com/download) to download vs code. The link should bring you to this page.
![Image](vscode.png) Download the package corresponds to your computer system and install it.
</span>

<h4 align = "center">
    <span style = "font-size:30px">Remotely Connecting</span>
</h4>

* <span style = "font-size: 18px"> After you have successfully install vs code, open it, hover to extensions ![Image](extensions.png), search and install remote-ssh ![Image](remotessh.png)

* <span style = "font-size: 18px"> Then, hover to "Terminal" -> new terminal.

* <span style = "font-size: 18px"> In terminal type <span style = "color:red">ssh cs15lsp22+(course quarter)+3 unique letters @ieng6.ucsd.edu </span> in your terminal.</span>
    
    * <span style = "font-size: 18px"> Ps: your cs15l(course quarter) username will have 3 unique letters after 22, make sure you know yours.</span>

* <span style = "font-size: 18px"> After you entered your email, it will ask you to enter your password.</span>

    * <span style = "font-size: 18px"> Ps: for security reason, it would not show anything when you are typing your password, so just type it and press enter.</span>

* <span style = "font-size: 18px"> After you have done all steps above, you should see ![Image](login.png) This mean you are successfully remote connected to the your lab computer.

* <span style = "font-size: 18px"> Now you have connected to the lab computer, lets try some commands
    * <span style = "font-size: 18px"> ls (show normal files in blue)
    
    ![Image](ls.png)

    * <span style = "font-size: 18px"> mkdir (create a directory or file)

    ![Image](mkdir.png)

    <span style = "font-size: 18px"> After you done that do ls again to check if you have created successfully or not.

    *<span style = "font-size: 18px"> cd filename (change directory)

    ![Image](cd.png)

    *<span style = "font-size: 18px"> pwd (check which directory you are currently at)

    ![Image](pwd.png)


<h5 align = "center">
   <span style = "font-size: 30px"> Setting an <span style = "color: blue">SSH </span> Key and Moving files with <span style = "color: blue">SCP</span></span>
       
</h5>

* <span style = "font-size: 18px">If you are those type of person that doesn't like entering password every single time, then this is designed for you.

* <span style = "font-size: 18px">First, do ctrl + d for disconnect from the remote computer.

* <span style = "font-size: 18px">Then, enter <span style = "color:green"> ssh-keygen</span> in your terminal. It should show something like the picture.

  ![Image](keygen1.png)

* <span style = "font-size:18px">Leave it empty, press enter to continue. Then, it ask you for the passphrase, also leave it empty and press continue.

* <span style = "font-size:18px"> After you done that it will shows this ![Image](keygen.png) that mean you have successfully created an empty file that stored your password.

* <span style = "font-size:18px"> Now, you need to login to the remote computer first to create a <span style = "color:purple">.ssh</span> file to store your password.

    * <span style = "font-size:18px"> After login, type <span style = "color:green"> mkdir .ssh</span> to create your ssh filder. (user <span style = "color:green">ls -a </span> to make sure you have created the file)

    * <span style = "font-size:18px"> disconnect

* <span style = "font-size:18px"> In your main computer, type <span style = "color:green"> scp /Users/(your username for your computer)/.ssh/id_rsa.pub (your @ieng.ucsd.edu email):~/.ssh/authorized_keys</span> in your terminal to upload your public keygen file from your computer to the remote computer.

    * <span style = "font-size:18px"> In general, if you are trying upload file from your current file, simply just do <span style = "color:green">scp (name of the file) (ieng6 email):~/</span> this will upload your file to the main folder, but if you want to upload file to a specific folder, type the exist folder in your remote computer after <span style = "color:green"> ~/</span>.

    * <span style = "font-size:18px"> For exmaple, if I want to upload this file to the "hello" folder, I need to type <span style = "color:green">scp lab-report-1-week-2.md cs15lsp22@ieng6.ucsd.edu:~/hello

       <center>
<span style = "font-size:30px"> Tips</center>

* <span style = "font-size:18px"> When typing command lines in terminal, you can always use tab to autofill codes or file's name.

* <span style = "font-size:18px"> Using the up or down arrow key may help you save some times when your previous command has some errors in it.

    



