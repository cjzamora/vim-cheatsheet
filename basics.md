# Vim Basics

Below are the basic things to learn when playing around with vim.

## Starting Vim

- `$ vim <file>` - Open the given file via vim.
- `$ vim, :e <file>` - Open vim, then execute the edit command.

## Basic Modes

- __Insert Mode__
	- `i` - Enter insert mode at cursor.
	- `I` - Enter insert mode at first non-blank character.
	- `a` - Enter insert mode _after_ cursor.
	- `A` - Enter insert mode at the end of the line.
	- `o` - Enter insert mode on the next line.
	- `o` - Enter insert mode on the above line.
- __Normal Mode__
	- `ESC` - Switch to Normal Mode.
	- `Ctrl+[` - Switch to Normal Mode.
- __Visual Mode__
	- `v` - Switch to visual mode
	- `v<w,e,b...>` - To select a word in visual mode and combine it with any commands.

> __TIP__! Everything you do in vim (for the most part) follows this pattern: `[(n)um]<verb><n(o)un>` where most of the commands can accept number arguments to execute a command _nth_ times, for example: `3i<word>ESC` will insert the `word` 3 times on the current line.

## Movements

- __Line or Character__
	- `h` - Move left per character of the current line.
	- `l` - Move right per character of the current line.
	- `k` - Move up above the current line.
	- `j` - Move down below the current line.
- __Word__
	- `w` - Forward to the beginning of the next __word__.
	- `W` - Forward to the beginning of the next __WORD__.
	- `b` - Backward to the beginning of the next __word__.
	- `B` - Backward to the beginning of the next __WORD__.
	- `e` - Forward to the next end of __word__.
	- `E` - Forward to the next end of __WORD__.
- __Others__
	- `0` - Move to the beginning of the line.
	- `$` - Move to the end of the line.
	- `^` - First non-blank character of the line.
	- `{` - Beginning of the previous paragraph.
	- `}` - Beginning of the next paragraph.
	- `%` - Match the next brace, bracket, comment, #define
	- `gg` - Move to the top of the file.
	- `GG` - Move to the bottom of the file.

> __word__ - is separated by anything that is not a character, the cursor will move to the word that is separated by a non-character e.g a comma.
>
> __WORD__ - is separated by white space, the cursor will move to the beginning of the word that is separated by a white space. 

## Searching

- __Character__
	- `f<char>` - Forward to the next `<char>` __(Inclusive)__.
	- `F<char>` - Backward to the previous `<char>` __(Inclusive)__.
	- `t<char>` - Forward to the next `<char>` __(Exclusive)__.
	- `T<char>` - Backward to the previous `<char>` __(Exclusive)__.
- __Word__
	- `/<word|regexp>` - Forward.
	- `?<word|regexp>` - Backward.
	- `*` - Word under cursor - forward __(bounded)__.
	- `g*` - Word under cursor - forward __(unbounded)__.
	- `#` - Word under cursor - backward __(bound)__.
	- `g#` - Word under cursor - backward __(unbounded)__.
	- `n` - Next result, forward.
	- `N` - Next result, backward. 

> __Inclusive__ - the cursor will go exactly to the `<char>`.
> 
> __Exclusive__ - the cursor will go before the `<char>`.
> 
> __Bounded__ - Exact word match.
> 
> __Unbounded__ - A word is a part of another word, for example "forensic" or "forever" both contains "for", so both will be a result.

## Copy & Paste

- `y` - Yank. Example: `yw` (yank word).
- `yy` - Yank the current line.
- `p` - Paste after cursor.
- `P` - Paste before cursor.

## Undo & Redo

- `u` - Undo stuff.
- `Ctrl+R` - Redo stuff.

## Replacing

- `r` - Replace character under cursor.
- `R` - Replace characters starting at the cursor.

## Deleting

- `d` - Delete. Example: `yw` (delete word).
- `dd` - Delete the current line.
- `x` - Remove a character, forward.
- `X` - Remove a character, backward.
- `s` - Delete character under cursor and enter insert mode.
- `S` - Delete line and begin insert at the beginning of same line.
- `C` - Delete from cursor to end of line and begin insert.
- `J` - Join the current line with the next line (with space).
- `gJ` - Join the current line with the next line (without space).

## Repeating

- `.` - Repeat last changes.