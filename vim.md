# vim

## select number of lines

`V<N>j` will select N lines down

## terminal from vim

`:terminal`

## integrate git into vim

[vim-gitgutter](https://github.com/airblade/vim-gitgutter)

## search and replace
`:%s/foo/bar/gc` \
Change each 'foo' to 'bar', but ask for confirmation first. \
[source](https://vim.fandom.com/wiki/Search_and_replace)

## duplicate symbol under the cursor
`ylp` \
`yl` to put in buffer, press `p` each type you want to insert

## working with tabs in ranger
Option-N where N is number of tab \
(Terminal -> Preferences -> Keyboard -> check Use Option as Meta key)

## working with tabs
`:tabnew` — opens new tab \
`:tabedit {file}` — edit specified file in its tab \
`gt` — go to next tab \
`gT` — go to previous tab \
`{i}gt` — go to tab in position i \
[source](https://vim.fandom.com/wiki/Using_tab_pages)

### change color of tabs line
`:hi TabLineFill ctermfg=Gray` \
[source](https://stackoverflow.com/a/7238163/355491)

## working with file tree
`:Explore` \
[source](https://shapeshed.com/vim-netrw/)

### create new file
`%` \
[source](https://til.hashrocket.com/posts/2034bed53c-create-new-file-in-vims-file-explorer)

### create new folder/director
`d` \
[source](https://til.hashrocket.com/posts/ceeb5862b8-create-a-new-directory-in-netrw)

## jump to line/column
`:<num>` — line # num \
`<num>G` — line # num \
`<num>|` — column # num

## sort lines
`Shift+v` — select lines \
type `:sort`

## indent
`>i{` — increase inner block indent \
`<i{` — decrease inner block indent \
[source](https://vim.fandom.com/wiki/Indent_a_code_block) \
`>>` — indent current line \
`<<` — unindent current line \
[source](https://vim.fandom.com/wiki/Shifting_blocks_visually)

## delete word
`diw` — delete word (cursor inside) \
`daw` — delete word with space (cursor inside) \
`de` — delete between cursor and end of word \
`dw` — delete between cursor and whitespace (including) \
`df<char>` — delete next symbols till <char> (including) \
`d<num>f<char>` — delete next symbols till <char> # <num> (including) \
change `d` (delete) with `c` (change) to enable insert mode

## column mode edit
`Ctrl+v` — go to column mode \
`Shift+i` — enter changes (shown on first line) \
`Esc,Esc` — applies changes to all lines \
[source](https://coderwall.com/p/ouzshq/column-edit-mode-in-vi)

### ack plugin

```bash
mkdir -p ~/.vim/pack/ack/start
cd ~/.vim/pack/ack/start
git clone https://github.com/mileszs/ack.vim.git
vim ~
:Ack -i --scala "query" .
:cope # focuses on quickfix window
:ccl # closes quickfix window
```

## switch case
`~` — toggle case of single character \
[source](https://vim.fandom.com/wiki/Switching_case_of_characters)

## directory browser in vim
`gh` — toggle hidden files \
[tutorial](https://shapeshed.com/vim-netrw/) [documentation](http://vimdoc.sourceforge.net/htmldoc/pi_netrw.html)

## open files from vim
`:find <path>` — open file \
`:vs <path>` — open file in vertical split \
`:sp <path>` — open file in horizontal split \
[source](https://shapeshed.com/vim-netrw/#you-may-not-need-netrw)

## delete from cursor to the end of line
`d$` or `D` \
[source](https://unix.stackexchange.com/questions/4415/delete-from-cursor-to-end-of-line-on-vi/4416#4416)

## reload file in vim
`:e` \
[source](https://vi.stackexchange.com/questions/444/how-do-i-reload-the-current-file/445#445)

## increment/decrement number
`C-a` — increment \
`C-x` — decrement \
[source](https://vim.fandom.com/wiki/Increasing_or_decreasing_numbers)

## save all tabs
`:wa` \
[source](https://stackoverflow.com/questions/4246268/how-to-save-all-files-in-tabs-on-vim/4246310#4246310)

## working with [book]marks
`m[a-z]` — set local [a-z] mark \
`m[A-Z]` — set global [A-Z] mark \
`'[a-zA-Z]` — jump to [a-zA-Z] line \
\`[a-zA-Z] — jump to [a-zA-Z] line and column \
\`. — jump to the last change \
[source](https://vim.fandom.com/wiki/Using_marks)

## search whole word
`/\<word\>` or `/\v<word>` \
`:g/\<bar\>` or `:g/\v<word>` \
[source](https://stackoverflow.com/questions/15288155/how-to-do-whole-word-search-similar-to-grep-w-in-vim)

## What is vim recording and how can it be disabled?
https://stackoverflow.com/questions/1527784/what-is-vim-recording-and-how-can-it-be-disabled

## select range of lines
`10GV12G` — select lines 10–12 \
`10GV2j` — select line 10 and 2 bellow \
[source](https://unix.stackexchange.com/questions/43381/select-lines-using-ranges-in-vim)
