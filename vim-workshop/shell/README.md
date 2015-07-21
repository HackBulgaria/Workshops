# Introduction to Shell

## Commands - Piping, Redirecting

Command piping is something very useful:

```
$ ls /usr/bin | grep python
```

This can be read as:

1. Take the output from `ls /usr/bin`
2. Give that output to `grep python`
3. Print the output of `grep python the previous output`

Now if we want to redirect the output of the previous commands, we can do the following:

```
$ ls /usr/bin | grep python >> python_executables
```

The `>>` means append the output to the file `python_executables`

If we want to take the output from a file, rather than another command, we can use that `<` symbol:

```
$ grep var < fix_me.js
var factorial = function(n) {
var n = 10
```

[For more information about pipes & redirects, you can read here](http://www.westwind.com/reference/os-x/commandline/pipes.html)

## more / less

Now, man pages are something very usefull. To learn more about `more` and `less`:

```
$ man more
$ man less
```

Quite the word play. Now, we are going to use less to read large files!

```
$ less README.md
```

`less` supports vim-like motions.

**If you want to quit from the `less` view, hit `q`**

## bashrc

* [rc files](http://unix.stackexchange.com/questions/3467/what-does-rc-in-bashrc-stand-for) - bashrc / zshrc

This is your bash configuration. You can put useful things here.

Aliases are a good start.

If you want to have `py` running your python3.4 REPL, open `~/.bashrc` in vim and append:

```
alias py='python3.4'
```

Now restart your shell and you will have the `py` program!

[You can generate your own .bashrc file!](http://bashrcgenerator.com/)

## Shells & zsh

* <http://www.tutorialspoint.com/unix/unix-shell.htm>
* [Slides talking about Zsh awesomeness](http://www.slideshare.net/jaguardesignstudio/why-zsh-is-cooler-than-your-shell-16194692)
* [Oh-My-Zsh](https://github.com/robbyrussell/oh-my-zsh)
* [Install Oh-My-Zsh](https://github.com/RadoRado/Untouched-Ubuntu/blob/master/zsh.sh)

## z command

Pretty useful command to jump into directories. Remembers your choices and makes you look smart!

* [Install z](https://github.com/rupa/z)


## Materials

* http://vimcasts.org/blog/2013/02/habit-breaking-habit-making/
* http://bullium.com/support/vim.html
* http://vim.wikia.com/wiki/Tutorial
* http://stackoverflow.com/questions/3776117/what-is-the-difference-between-the-remap-noremap-nnoremap-and-vnoremap-mapping
