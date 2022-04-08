# How to login to a course-specific account on ieng6

Welcome future students or to my future self!
This short tutorial will show you the basics of ieng6.

### Step 1: Installing VSCode
1. First you want to either look up VSCode installation or go to this link [VSCode Installation](https://code.visualstudio.com/download). It should look like:
2. Then you are going to want to download for your specific device and you should start to download .zip file.
3. Once that file downloads, open it and follow the set up steps that are prompted. Then you have succesfully downloaded VSCode.

### Step 2: Remotely Connecting
1. First you are going to need to download OpenSSH which can be found at [OpenSSH download](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). Follow what it says and you are done with this step.
2. Find your course specific account which can be found after logging into [Account look up](https://docs.google.com/document/d/1AO6RDoJnaWxMui-UFjEa_2bbQ4qcANpbIpPuV-awsOg/edit).
3. Open VSCode and open a new terminal. Then type in `ssh cs15lsp22zz@ieng6.ucsd.edu` with the zz being replaced with your account specific letters.
4. Say yes to the question prompted asking if you want to continue to connect, and then give your password. After this you are done with step 2.

### Step 3: Trying Some Commands
1.  Now that you are remotely connected, try runnig some commands that you can see in this photo:

### Step 4: Moving Files with scp
1. Go to your terminal and run the command: `scp [fileName] cs15lsp22zz@ieng6.ucsd.edu:~/` again replacing `[fileName]` with the full file name (including the .java) and replacing the `zz` with your account numbers.
2. You will be prompted for your password. After putting in your password, you want to log back into your `ssh` account and insert the command `ls`. You should see your file and can run it on the remote account.

### Step 5: Setting an ssh key
1. On your client insert the code:
> `ssh-keygen`

> `Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa`

> `Enter passphrase (empty for no passphrase): ` 

**Make sure to not add a passphrase**

> `Enter same passphrase again:`

> `Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.`

>`Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.`

> `The key fingerprint is:`

> `SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local`

> `The key's randomart image is:`

2. If you are on windows you will need to do bonus steps found at [Windows OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation).

3. Now we have to copy the public key to the `ssh` directory of your remote account. So follow the code below:
> `ssh cs15lsp22zz@ieng6.ucsd.edu` (enter password when prompted)

> `mkdir .ssh`

> `<logout>`

> `scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys`

> *User your username and the path seen in the command above*

4. Now you should be able to use ssh and scp without needing a password!

### Step 6: Optimizing Remote Running
1. At the end of an ssh statement, you can add commands in quotes which will run on the command server!
2. Semicolons can be used to seperate multiple commands on the same line.
3. Also the up arrow can be used to go back to the previous command that was called.