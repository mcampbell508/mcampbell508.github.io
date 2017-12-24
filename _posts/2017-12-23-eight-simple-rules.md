---
layout: post
title:  "8 Simple Rules for a provocative developer environment"
date:   2017-12-23 15:20:59 +0000
---

> The following "rules" are my opinions of what a developer environent should be like. This article assumes nothing!

## 1. Ditch Windows for Linux.

I have not used Windows for 4 years now, and I have not really looked back since - if you have not made the jump yet maybe you should do so.

## 2. Customise your Bash shell
You *could be* more productive and enjoy your console more if you use use a custom Bash theme like the following. [Agnoster Bash Theme](https://github.com/speedenator/agnoster-bash)

![Agnoster](https://github.com/speedenator/agnoster-bash/blob/master/agnoster-bash-sshot.png?raw=true)

The place where something like this really shines is when you are working with Git repositories, as it can show you lots of relevant info like:

- current branch
- whether you have any changed files (stage or unstaged)
- current directory

Shells like [Oh-My-Zsh](https://github.com/robbyrussell/oh-my-zsh) and [Oh-my-fish](https://github.com/oh-my-fish/oh-my-fish) are avaiable if you are really hardcore.

## 3. Centralise **All the Things &trade;**
The following should be version controlled if possible - so that you are ready to go on multiple systems:

- Dot files (`.~.bashrc` etc)
    - Git Aliases
        - `~/.gitconfig`
        - `~/.gitignore_global`
        - `~/.git_commit_template`
    - Bash Aliases
        - `~/.bashrc`
        - `~/.bash_aliases`
    - Vim Defaults
- IDE Setting configuration (PhpStorm synced settings for instance)

There is even a GitHub community effort where inviduals share their dot files, [here](https://dotfiles.github.io/).

You can checkout my Dotfiles [here on GitHub](https://github.com/mcampbell508/dotfiles), if you are interested.

## 4. Automate **All the Things &trade;**

So maybe now you are happy with your developer envioronment, but what happens if you suffer a hardware failure and need to install everything again..?
You might want to use something like Ansible to provision your local developer environment. The cool thing if you do it properly is that it will only
install what doesnt already exist in a given state, if you create the playbooks correctly.

## 5. **"Git"** your groove on...

> So you've got some decent Git knowledge are you ready to step up to the next level..?

You have already seen in step 2, above, that you can improve the layout of your shell to help with Git. There are a couple of other things that I have done myself:

- Use a git commit template to improve commit messages:
    - `vim ~/.git_commit_message_template` and paste something to the following:

```
# 50 character mark------------------------------|  72 character mark: |
#<prefix>: <title>


# Explain why this change is being made


# Provide links to any relevant tickets, articles or other resources

```

Then make this change available by running `git config --global commit.template ~/.git_commit_message_template`.

- You can also modify your `~/.vimrc` profile to help with following the recommended 72 character limit for commit messages and adds a spell check.

    - `vim ~/.vimrc`:

```
autocmd Filetype gitcommit setlocal spell textwidth=72
```

Here are some external links for improving Git commit messages:

- [A useful template for commit messages](http://codeinthehole.com/writing/a-useful-template-for-commit-messages/)
- [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
- [How to Write a Git Commit Message - Chris Beams](https://chris.beams.io/posts/git-commit/)

## 6. More Git...

How about using Git Hooks to prompt you about your rubbish code style and commit messaging..?

Maybe you could use something similar to the following to guide you to better code or commit messaging:

![Static Review](https://camo.githubusercontent.com/5d44fe2dc2b7b8ba1e41d22723a2dfc80c81a239/687474703a2f2f692e696d6775722e636f6d2f384733754f52702e676966)

Some options for this could be (For PHP):

- [Static Review](https://github.com/sjparkinson/static-review)
- [GrumpPHP](https://github.com/phpro/grumphp)

## 7. Consider tweaking your code editor to suit your style
If you are a developer this will probably be the thing you interact with for most of the day. I use "Material Theme UI" in PhpStorm, as its quite slick - to me.

## 8. Customise Desktop and launching of apps

- You don't necessarily have to use the stock UI that comes with your OS, other options are available.
- Pin / Lock to Launcher your most used apps, to your taskbar & remove any unused apps.
- Consider starting your most used apps on system login, which can be done on Ubuntu via ["Startup applications"](https://help.ubuntu.com/stable/ubuntu-help/startup-applications.html)
- Most importantly, find your own flow.

## Extra

- Prefer using Git in the terminal rather than via a UI
- Ditch nano for vim
- Ditch Sublime for PhpStorm
- Ditch PhpStorm for VSCode, once it has decent PHP support :-)

---

![](https://media.giphy.com/media/8vsr2w5t91Nte/giphy.gif)