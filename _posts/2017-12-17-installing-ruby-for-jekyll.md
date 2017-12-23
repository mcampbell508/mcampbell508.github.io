---
layout: post
title:  "Installing Ruby for Jekyll (Ubuntu 16.04)"
date:   2017-12-17 14:20:59 +0000
tags: jekyll ruby ubuntu
---

I had to remove the current installed version as I ran into something similar to the following:

```
You don't have write permissions for the /var/lib/gems/2.3.
```

## Remove currently installed

```
sudo apt-get remove ruby
```

## Install new version via `rbenv`


```
cd $HOME
sudo apt-get update
sudo apt-get install autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm3 libgdbm-dev

sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

rbenv install 2.4.3
rbenv global 2.4.3
ruby -v


# Then bundler

gem install bundler
rbenv rehash
```

[This link](https://stackoverflow.com/a/37956249/3032618) was helpful in fixing this.

I then had to do:

```
sudo chown -R $(whoami):$(whoami) ~/.bundle
```


## Updating `ruby-build` (in future)

```
cd "$(rbenv root)"/plugins/ruby-build && git pull
```

## Troubleshooting

- https://github.com/rbenv/ruby-build/wiki#updating-ruby-build