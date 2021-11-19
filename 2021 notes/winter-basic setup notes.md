# Machine Setup
1. Edit bash profile and bash rc. Aliases should be in bashrc, not bash_profile
```
nano ~/.bashrc
nano ~/.bash_profile
source ~/.bashrc
source ~/.bash_profile
```

<details>
  <summary>click here for full text of bash profile or bash rc</summary>
  
  ```
  # Setting PATH for Python 3.7
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.7/bin:${PATH}"
export PATH

export PATH="/Users/stepha/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"

# see git branch in terminal
export PS1="\\w:\$(git branch 2>/dev/null | grep '^*' | colrm 1 2)\$ "

# weather and the moon
alias weather='curl -4 http://wttr.in/Houston'
alias moon='curl -4 http://wttr.in/Moon'

# cheat sheet
function cheat() {
  curl cht.sh/$1
}

# code shortcut
alias code="cd ~/Code"

# git shortcuts
alias gitst="git status"
alias gitcheckout="git checkout"
alias gitco="git checkout"
alias gita="git add"
alias gitadd="git add"
alias gitcommit="git commit -m"
alias gitcmt="git commit -m"

# nvm
export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
  ```
</details>

2. Install homebrew, nvm, npm, node 
```
nvm install stable
node --version
npm --version
````

# Repo Setup
1. Create repo in github
2. Set up SSH key auth for git on this machine: [Github Doc Link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
