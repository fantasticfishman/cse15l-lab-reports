# Lab Report 3

## Streaming SSH Configuration
- This lab report documents how I streamlined my SSH process. 

## Config
- I edited the config file in my local .ssh folder, using VS Code, to create a new alias (ieng6), so I didn't have to type in the full address each time I wanted to access the remote server.
![Image](/week6/1.png)

- Please note that when I was connecting the VSCode SSH extension so I could view/edit files on the remote server through VS Code, it made its own alias in the config(the first one). The one I made was the second one, with ieng6 as the alias. Deleting/editing the first one causes issues with the extension, so I just made two.

## SSH

- As you can see, I was able to ssh into the remote server just by typing "ieng6" instead of the full long address (cs15lwi22whatever@ieng6.ucsd.edu). This helps streamline the process a lot. If I wanted to quickly check the remote server this makes things a lot easier.
![Image](/week6/2.png)

## SCP
- In addition to shorting my SSH commands, I can also use "ieng6" in my scp commands, to shorten them, so I don't have to type out the full address, as displayed below.
![Image](/week6/3.png)

- This makes copying over single files when I need to very quick and easy. Here I scp over amogus.txt using the alias, saving a lot of typing.


