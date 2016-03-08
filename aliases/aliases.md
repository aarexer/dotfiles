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
