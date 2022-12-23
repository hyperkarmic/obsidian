# move comand
## Move command

You can move a line, or a block of lines, with the `:m` command. Examples:

`:m 12`

move current line to after line 12

`:m 0`

move current line to before first line

`:m $`

move current line to after last line

`:m 'a`

move current line to after line with mark `a` (see [using marks](https://vim.fandom.com/wiki/Using_marks "Using marks"))

`:m 'a-1`

move current line to before line with mark `a`

`:m '}-1`

move current line to the end of the current paragraph

For clarity, a space is shown after the `:m` commands above, but that space is not required.

To move a block of lines, use the same command but visually select the lines before entering the move command. You can also use arbitrary [ranges](https://vim.fandom.com/wiki/Ranges "Ranges") with the move command. Examples:

`:5,7m 21`

move lines 5, 6 and 7 to after line 21

`:5,7m 0`

move lines 5, 6 and 7 to before first line

`:5,7m $`

move lines 5, 6 and 7 to after last line

`:.,.+4m 21`

move 5 lines starting at current line to after line 21

`:,+4m14`

same (`.` for current line is assumed)