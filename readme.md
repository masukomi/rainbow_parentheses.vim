# Rainbow Parentheses

### Commands:

```vim
:RainbowParenthesesToggle       " toggle it on/off
:RainbowParenthesesLoadRound    " (), toggle default
:RainbowParenthesesLoadSquare   " []
:RainbowParenthesesLoadBraces   " {}
:RainbowParenthesesLoadChevrons " <>
```

### Always On:

```vim
augroup RainbowParentheses
    au!
    au VimEnter * RainbowParenthesesToggle
    au Syntax * RainbowParenthesesLoadRound
    au Syntax * RainbowParenthesesLoadSquare
    au Syntax * RainbowParenthesesLoadBraces
augroup END
```

### Options:

set color ordering

- left column = vim
- right column = gvim
- order is from inner to outer

If less than 16 entries, then existing list of colors repeat until 16.

```vim
let g:rbpt_colorpairs = [
    \ ['3',         '808000'],
    \ ['6',         '008080'],
    \ ['202',       'ff5f00'],
    \ ['11',        'ffff00'],
    \ ['13',        'ff00ff'],
    \ ['10',        '00ff00'],
    \ ['45',        '00dfff'],
    \ ['9',         'ff0000'],
    \ ]
```

max parentheses to match

```vim
let g:rbpt_max = 16
```

bold parentheses

```vim
let g:rbpt_bold = 0
```

unknown

```vim
let g:rbpt_loadcmd_toggle = 0
```
