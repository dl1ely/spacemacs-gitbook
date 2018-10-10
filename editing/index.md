# Editing with Vim and iedit

 Using [iedit](https://github.com/victorhge/iedit) you can edit multiple, identical string occurrences at the same time.

![iedit - Edit multiple regions in the same way simultaneously](https://github.com/victorhge/iedit/raw/master/iedit-demo.gif)

Spacemacs uses the powerful [iedit](https://github.com/tsdh/iedit) mode through [[https://github.com/syl20bnr/evil-iedit-state][evil-iedit-state]] to quickly edit multiple occurrences of a symbol or selection.

iedit also integrates with [[https://github.com/magnars/expand-region.el][expand-region]] for quick editing of the currently selected text by pressing `e`.

**** iedit states key bindings

| Key Binding | From             | To     |
|-------------|------------------|--------|
| `SPC s e`   | normal or visual | iedit  |
| `e`         | expand-region    | iedit  |
| `ESC`       | iedit            | normal |
| `C-g`       | iedit            | normal |
| `fd`        | iedit            | normal |
| `ESC`       | iedit-insert     | iedit  |
| `C-g`       | iedit-insert     | normal |
| `fd`        | iedit-insert     | normal |


*Note*: evil commands which switch to =insert state= will switch in =iedit-insert state=.

***** In iedit state
=iedit state= inherits from =normal state=, the following key bindings are specific to =iedit state=.

| Key Binding | Description                                                                             |
|-------------|-----------------------------------------------------------------------------------------|
| `ESC`       | go back to =normal state=                                                               |
| `TAB`       | toggle current occurrence                                                               |
| `0`         | go to the beginning of the current occurrence                                           |
| `$`         | go to the end of the current occurrence                                                 |
| `#`         | prefix all occurrences with an increasing number (SPC u to choose the starting number). |
| `A`         | go to the end of the current occurrence and switch to =iedit-insert state=              |
| `D`         | delete the occurrences                                                                  |
| `F`         | restrict the scope to the function                                                      |
| `gg`        | go to first occurrence                                                                  |
| `G`         | go to last occurrence                                                                   |
| `I`         | go to the beginning of the current occurrence and switch to =iedit-insert state=        |
| `J`         | increase the editing scope by one line below                                            |
| `K`         | increase the editing scope by one line above                                            |
| `L`         | restrict the scope to the current line                                                  |
| `n`         | go to next occurrence                                                                   |
| `N`         | go to previous occurrence                                                               |
| `p`         | replace occurrences with last yanked (copied) text                                      |
| `S`         | (substitute) delete the occurrences and switch to =iedit-insert state=                  |
| `V`         | toggle visibility of lines with no occurrence                                           |
| `U`         | Up-case the occurrences                                                                 |
| `C-U`       | down-case the occurrences                                                               |

*Note*: `0`, `$`, `A` and `I` have the default Vim behavior when used outside of an `occurrence`.

***** In iedit-insert state

| Key Binding | Description               |
|-------------|---------------------------|
| `ESC`       | go back to =iedit state=  |
| `C-g`       | go back to =normal state= |


------------------------------------------

> ####Hint::Vim Editing
> [Vim Basics](/spacemacs-basics/vim-basics.html) and [Vim Quick Reference](/spacemacs-basics/vim-quick-reference.html) covers a lot of the power of Vim editing.


`SPC s e` calls evil-iedit-state/iedit-mode, which in turn calls iedit-mode - this is done for integration with evil
