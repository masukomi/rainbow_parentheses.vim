# Better Rainbow Parentheses

### Options:

- set color ordering

    let g:rbpt_colorpairs = [
        \ ['brown',       'RoyalBlue3'],
        \ ['Darkblue',    'SeaGreen3'],
        \ ['darkgray',    'DarkOrchid3'],
        \ ['darkgreen',   'firebrick3'],
        \ ['darkcyan',    'RoyalBlue3'],
        \ ['darkred',     'SeaGreen3'],
        \ ['darkmagenta', 'DarkOrchid3'],
        \ ['brown',       'firebrick3'],
        \ ['gray',        'RoyalBlue3'],
        \ ['black',       'SeaGreen3'],
        \ ['darkmagenta', 'DarkOrchid3'],
        \ ['Darkblue',    'firebrick3'],
        \ ['darkgreen',   'RoyalBlue3'],
        \ ['darkcyan',    'SeaGreen3'],
        \ ['darkred',     'DarkOrchid3'],
        \ ['red',         'firebrick3'],
        \ ]

- set max number to match

    let g:rbpt_max = 16

    let g:rbpt_loadcmd_toggle = 0

```vim
let g:rbpt_bold = 0
```

`g:rbpt_bold` highlights colored parentheses in bold to make them easier to see.
`1` to enable. Default is `0`.

### Commands:

    :RainbowParenthesesToggle       " Toggle it on/off
    :RainbowParenthesesLoadRound    " (), the default when toggling
    :RainbowParenthesesLoadSquare   " []
    :RainbowParenthesesLoadBraces   " {}
    :RainbowParenthesesLoadChevrons " <>

### Always On:

    augroup RainbowParentheses
        au!
        au VimEnter * RainbowParenthesesToggle
        au Syntax * RainbowParenthesesLoadRound
        au Syntax * RainbowParenthesesLoadSquare
        au Syntax * RainbowParenthesesLoadBraces
    augroup END
