---
layout: post
title:  "Switching from Bash to ZSH (Oh-my-zsh)"
date:   2018-01-07 11:20:59 +0000
tags: dev-env bash oh-my-zsh terminal
---

For years I have used the default terminal shell that comes with Linux, Bash. Having looked at several dotfile projects on [GitHub](https://dotfiles.github.io)
and also watching Wes Bos' [Command Line Power User](http://commandlinepoweruser.com/) free course, I thought it was time to look around at the other options available.

> The Wes Bos course is a great watch if you have not already done so, and his teaching style is awesome. He also has tonnes of other courses.

## Installing ZSH

```
sudo apt-get install zsh -y
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
```

### Changing the shell

```
chsh -s `which zsh`
```

> The above will require a logout or system restart.

### Fixing Jekyll server

I had to do the following to ensure Jekyll was able to serve files locally (found [here](https://stackoverflow.com/a/34362519/3032618)):

```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshenv
echo 'eval "$(rbenv init -)"' >> ~/.zshenv
echo 'source $HOME/.zshenv' >> ~/.zshrc
exec $SHELL
```

#### 1. Set the theme

- Edit the `~/.zshrc` file `vim ~/.zshrc` and set:

```
ZSH_THEME="agnoster"
```

#### 2. Choose the plugins

- `vim ~/.zshrc`

```
plugins=(git command-not-found node sudo vagrant)
```

> Don't forget to then `source ~/.zshrc`

#### 3. Using `z` for jumping to recent folders
1. `cd ~/`
2. Download: `wget https://raw.githubusercontent.com/rupa/z/master/z.sh`
3. Make `z` available with `ZSH`:
```
printf "\n\n#initialize Z (https://github.com/rupa/z) \n. ~/z.sh \n\n" >> .zshrc
```
4. Reload shell: `source ~/.zshrc`

> Helpful link for this can be found [here](https://www.vultr.com/docs/boost-productivity-with-z-and-zsh-on-ubuntu)

### Features

#### Folder search

Example (found on Google):

![](https://camo.githubusercontent.com/28cbb7ca8080a540dca9371e738fb35e1ff1373e/68747470733a2f2f7261772e6769746875622e636f6d2f7368656e67796f752f6265726b7368656c662d7a73682d706c7567696e2f6d61737465722f696d616765732f6265726b7368656c662e676966)

#### Advanced History

If you know the command, i.e `git` but can't remember the parameters you can type `git ` and then cycle through your previous Git commands pressing the up key.