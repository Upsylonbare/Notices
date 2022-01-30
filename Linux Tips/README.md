# Linux Tips



## .basrc

------

.bashrc is the file you can modify to "create" commands. It is located in the home directory of the user and is executed each time you connect to "setup" your shell.

To modify it :

```bash
nano ~/.basrc 
```

To update your modifications :

```
source ~/.bashrc
```

For example, I have added the alias `up` :

```bash
alias up="sudo apt-get update -y && sudo apt-get upgrade -y"
```

When I want to update all my packages I just type "up"



## Exa

------

It is a package that add colour and a better presentation of the `ls` command in Linux

To download and install it : https://the.exa.website/

<img src="Ressources\exa.png" style="zoom: 67%;" />

Add exa alias in .bashrc :

```bash
# some more ls aliases
#alias ll='ls -alF'
#alias la='ls -A'
#alias l='ls -CF'

alias ll='exa -laF --group-directories-first --header --git --long'
alias la='exa -a --group-directories-first'
alias l='exa -lF --group-directories-first --header --git --long'
```



## Useful commands

------

See processes behind ports :

```bash
sudo netstat -tulpn
```

