# ZSH and Oh My Zsh

## Install ZSH and Oh My Zsh
```
$ sudo apt-get install zsh
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Agnoster theme (Terminator and VSCode)

### Install powerline fonts
```
$ git clone https://github.com/powerline/fonts.git
$ cd fonts
fonts$ sudo ./install.sh
```

### Configure Terminator

Open Terminator and go under the Preference menu (right-click -> Preferences) 

Select as font: Meslo LG for Powerline Regular

### Download useful plugins

```
$ cd ~/.oh-my-zsh/plugins
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting
$ git clone https://github.com/zsh-users/zsh-autosuggestions
$ git clone https://github.com/zsh-users/zsh-completions
$ git clone https://github.com/zsh-users/zsh-history-substring-search
$ git clone https://github.com/chrissicool/zsh-256color
```

In ~/.zshrc:

```
ZSH_THEME="agnoster"

plugins=(
        git
        docker
        zsh-autosuggestions
        zsh-syntax-highlighting
        zsh-completions
        zsh-history-substring-search
		zsh-256color
		autojump
        )

# To allow exiting with jobs in background:
setopt NO_HUP
setopt NO_CHECK_JOBS
```

Autosuggestions completes with CRL+f

Autojump jumps with j


### Configure VScode

In preferences:

```
{
"terminal.integrated.fontFamily": "'Meslo LG M DZ for Powerline', 'fontawesome'",
"terminal.integrated.fontSize": 15
}
```


## Upgrade oh_my_zsh
```
$ upgrade_oh_my_zsh
```
