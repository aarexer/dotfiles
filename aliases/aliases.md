## Aliases in my system
#### To use bash completion
* Copy this [bash-completion](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)
* Add source bash-completion to your bash_profile

#### /etc/profile
```sh
alias ls='ls --color=auto
```

#### ~/.bash_profile
```sh
source /etc/bash_completion.d/git-completion.bash
alias ll='ls -l'
```

#### ~/.gitconfig
```sh

[user]
        name = Aleksandr Kuchuk
        email = myEmail

[alias]
      l = log
      a = add
      cm = commit -m
      co = checkout
      f = fetch
      m = merge
```
#### On Mac
1. Install homebrew

2. Install Git and bash-completion: brew install git && brew install bash-completion (Note: If this install fails with a 404 error, and you already have git installed, just remove the git part of this brew install)

3. Add bash-completion to your .bash_profile:
```sh
  if [ -f $(brew --prefix)/etc/bash_completion ]; then
    . $(brew --prefix)/etc/bash_completion
  fi
```
