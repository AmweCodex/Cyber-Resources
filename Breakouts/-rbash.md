# -rbash

**`Initial Enumeration`**

***Check -1 : [[ Environment Variables Check ]]***

```bash
export -p # It spits out all the variables set
env # It gives the $SHELL and $PATH variable
echo $0 # It gives the $SHELL name
echo $PATH # It gives the path variable
```

***Check -2: [[ The `$PATH` Variable ]]***

```bash
ls /home/tom/usr/bin  #This will list all the files/commands inside that dir
/home/tom/usr/bin and hit tab twice #Sometimes the ls command itself won't be available, so we can use this method to still list the commands
echo /home/tom/usr/bin/* #If double tapping the tab is also disabled, you can echo the directory and get the list
```

**`Exploitation to Breakout of the rbash`**

***Method -1 : [[ Edit $PATH Variable ]]***

```bash
export PATH=$PATH:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

***Method -2 : [[ GTFObins ]]***

4 commands from the previous screenshot, `less` `ls` `scp` `vi` . So I’ll show how to use some of them to spawn a normal shell.

**vi :** I searched gtfobins with less and found a section on spawning a shell

![https://miro.medium.com/v2/resize:fit:875/1*PHWbDJOE7KjKUnt1owvO_Q.png](https://miro.medium.com/v2/resize:fit:875/1*PHWbDJOE7KjKUnt1owvO_Q.png)