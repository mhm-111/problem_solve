This repo is about the problems which I have solved different times 
 ------------------------------------------------------------------------------------------------

 
 PROBLEM-1 :   ROOT shell problem:
 ___________________________________________
 
If the shell of root change somehow you can't access root .

problem: >Can't access root. sudo su won't work.

![problem_root_shell](https://user-images.githubusercontent.com/89272932/131243546-fcdf9d1b-a615-493c-a84d-d4bfa6ce8962.png)


Solution
------------
1.cat /etc/shells will show all shells available in your system. pick a shell and place it in root shell.

    cat /etc/shells
 
  /bin/sh
  /bin/bash
  /usr/bin/bash
  /bin/rbash
  /usr/bin/rbash
  /bin/dash
  /usr/bin/dash
  /bin/zsh
 
 There may be many more shells.


2. See the  /etc/passwd file.

       cat /etc/passwd
 
       root:x:0:0:root:/root:zsh
  
Here is the problem . your system can't execute zsh shell. It can't recongnize it.


3. Replace the zsh to any other shell (ex: /bin/bash ) .You can use any text editor to edit it.
      
       sudo gedit /cat/passwd
 
       root:x:0:0:root:/root:/bin/bash
  
 :grinning: Problem is SOLVED
 
    _______________________  ______________________________   _______________________________   _______________________
  
  










