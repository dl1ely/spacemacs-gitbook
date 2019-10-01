# Learning Evil by Speaking Vim (Vi)

Vim can be easier to learn if you learn to speak commands as sentences.

First learn some verbs:

`c` (change), `d` (delete), `g` go, `v` visual (select), `y` yank (copy)

Then use those verbs with some modifiers

`'` mark, `{ }` begining/end of paragraph, `a` around, `f` find (includes character), `i` inside, `s` surround, `t` till (just before a character)

Then learn the text objects you can apply verbs and modifiers too

`b` block/parentheses, `p` paragraph, `s` sentence  `t` tag - html/xml, `w` word


## Examples of speaking Evil (Vi)

Practice speaking vim with these examples

| Keybinding  | Description                                                           |
|-------------|-----------------------------------------------------------------------|
| `c i s`     | change inside sentence                                                |
| `c i "`     | change inside double quotes                                           |
| `c i s`     | change inside current sentence (change the whole sentence)            |
| `c f )`     | change from cursor to next `)` character                              |
| `c s ' "`   | change by the surrounding single quotes with double quotes            |
| `c t X`     | change till the character `X` (not including `X`)                     |
| `c /foo`    | change until the first search result of ‘foo’                         |
| `d d`       | delete current line                                                   |
| `d i w`     | delete inside the current word (delete word)                          |
| `v t SPC`   | visual select till the next `Space` character                         |
| `v s ]`     | visually select and surround with `[]` without spaces                 |
| `g v`       | go to last visual selection                                           |
| `v a p`     | visually select around current paragraph                              |
| `SPC v s "` | visually select current work and surround with `""`                   |
| `v i w s "` | visually select, insert around current word, and surround with quotes |
| `y y`       | yank (copy) current line                                              |
| `y w`       | yank (copy) current word                                              |
| `y ' a`     | yank (copy) to mark `a` (`m a` creates a mark called `a`)                 |
|             |                                                                       |


### Using marks

The name of the mark is a character, so you can have 26 of them.  In general practice no more than 4 marks are ever used.  A recommended use of marks is:

| Keybinding | Description |
|------------|-------------|
| `a`        | First mark  |
| `b`        | Next mark   |
| `c`        | Another mark |
| `z`        | Last mark   |


> #### Hint:: Vim Reference and Tips
> [Vim quick reference guide](vim-quick-reference.html)
> [Vim tips for developers](vim-tips-for-developers.html)
> [Speaking Vim](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118)
