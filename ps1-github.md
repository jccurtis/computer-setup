# Colored Username/Host with GIT Details

## Get script
```bash
wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh -O ~/.git-prompt.sh
chmod a+x ~/.git-prompt.sh
```

## Add to .bashrc
```bash
#bash prompt coloring from http://osxdaily.com/2013/02/05/improve-terminal-appearance-mac-os-x/
#http://martinvalasek.com/blog/current-git-branch-name-in-command-prompt
#export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$ "
RED="\[\033[0;31m\]"
YELLOW="\[\033[1;33m\]"
GREEN="\[\033[0;32m\]"
PINK="\[\033[1;35m\]"
NO_COLOR="\[\033[0m\]"
# wget https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh ~/.git-prompt.sh
source ~/.git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
# Git branch in prompt (no hostname - \h)
# http://stackoverflow.com/questions/5379986/why-doesnt-my-bash-prompt-update
PS1="$GREEN\u:$PINK\w$YELLOW\$(__git_ps1 '(%s)')$NO_COLOR\$ "
```
