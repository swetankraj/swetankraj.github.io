---
layout: post
title: Styling Ubuntu Terminal with Powerline-Go and Fonts
tags: [ubuntu]
comments: true
---

![Crepe](/assets/img/posts/utp/terminal-style-powerlinego.png){: .mx-auto.d-block :}

## 1. Install Go and Powerline-Go

Install Go, then [Powerline-Go](https://github.com/justjanne/powerline-go), below commands should do the work.

```shell
sudo apt install golang-go
```

```go
go get -u github.com/justjanne/powerline-go
```

## 2. Update .bashrc file

Add the below shell script to your `~/.bashrc` file. This will enable powerline-go on your bash shell.

```shell
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
PROMPT_COMMAND="\_update_ps1; \$PROMPT_COMMAND"
fi
```

## 3. Install Powerline Fonts

Powerline need special fonts to show certain symbols, we will get it and a configuration file.

```bash
wget https://github.com/powerline/powerline/raw/develop/font/PowerlineSymbols.otf
wget https://github.com/powerline/powerline/raw/develop/font/10-powerline-symbols.conf
```

We will move `PowerlineSymbols.otf` to fonts directory `/usr/share/fonts/`.

```shell
sudo mv PowerlineSymbols.otf /usr/share/fonts/
```

Next, well update system's font cache.

```shell
sudo fc-cache -vf /usr/share/fonts/
```

Now, we'll install the `10-powerline-symbols.conf` file.

```shell
sudo mv 10-powerline-symbols.conf /etc/fonts/conf.d/
```

That's it! Now, open a new terminal and you shall see those styles.
