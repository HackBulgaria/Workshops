# Vim

## Make sure you have vim

With your proper package manager, install vim.

For example:

```
$ sudo apt-get install vim
```

## Starting out with vim

Now, open vim:

```
$ vim
```

Welcome! You are in vim world. But the screen is not very useful.

Now, in order to edit a file (lets say we want to edit a `README.md` file), type:

* `:e README.md` and hit enter - this will edit a new file. the `:e file` command means - open that file for editing. If there is no such file, create it.
* Press `i` and enter some markdown.
* Ready? Ok. Lets quit vim. Press `<Esc>`, then type `:wq` - write and quit.

That's it. Your first vim experience!

## vimrc

Like our `.bashrc` and `.zshrc`, there is `.vimrc` too.

Open with vim `~/.vimrc` and paste the following contents: <http://vim.wikia.com/wiki/Example_vimrc>

After this, reload vim.

Now, we are going to look at our vimrc file - to understand what we have done ;)

## No More Arrows

It is time to forget about our arrows.

We will navigate using `h`, `j`, `k` and `l` and other motions.

In order to achieve that, paste the following code in your `.vimrc`:

```
noremap <Up> <NOP>
noremap <Down> <NOP>
noremap <Left> <NOP>
noremap <Right> <NOP>
```

`<NOP>` means no operation.

That's it. Welcome to vim.

## Modes & Motions

Vim is not like other editors. It is modal. Depending on the mode you are in, you can do different things:

* If you want to type, you need to go into **insert mode**.
* If you want to navigate the code, you are more powerful in **normal mode**.
* If you want to copy / paste things, you need to be into **visual mode**.

The mode that we are going to stay in the most is **normal mode**. In that mode, we can navigate and give commands.

The important thing in **normal mode** is that we have motions. We can move differently, based on what we want to achieve:

* `w` - moves one word ahead
* `b` - moves one word back
* `h`, `j`, `k`, `l` are your `<`, `v`, `^`, `>` movements
* `gg` - moves at the start of the file
* `G` - moves at the end of the file
* `$` - moves at the end of the line
* `0` - moves at the beginning of the line

The beauty here is that we can combine motions with other commands:

* If we want to delete a char, we can type the `x` command with the cursor over the char.
* If we want to delete 2 characters, we can type `xx` or we can say `2x` - do x 2 times.
* If we want to delete an entire line, we can type `dd`
* If we want to delete the next two wotds, we can type `d2w` - delete the next 2 words. Here we are combining editing commands with motions

**Now, move to the first exercise**

### Go into insert mode and start editing

There are motions that puts us into insert mode, ready to start typing. This is very handy!

* `i` - insert mode directly under the cursor
* `<S-I>` - Shift + I - moves to the beginning of the line and puts us in insert mode.
* `a` - puts us in insert mode one character after the cursor
* `A` - moves to the end of the line and puts us into insert mode
* `o` - makes new line **under** the cursor + insert mode
* `O` - makes new line **above** the cursor + insert mode
* `s` - remove the character under the cursor and puts us into insert mode

**Now, move to the second excercise**

### Searching in vim

* `/` - makes a forward search. To jump to the next match, type `n`. To jump to the prev match, type `N`.
* `f{char}` - jumps to the next {char}. Very useful! You can combine that with delete: `df)` - delete until the next `)` char.
* `;` - repeat last search - to repeat the `f{char}`, you can type `;` - this will jump to the next match
