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

- always toggle

    let g:rbpt_loadcmd_toggle = 0

### Commands:

    :RainbowParenthesesToggle       " Toggle it on/off
    :RainbowParenthesesLoadRound    " (), the default when toggling
    :RainbowParenthesesLoadSquare   " []
    :RainbowParenthesesLoadBraces   " {}
    :RainbowParenthesesLoadChevrons " <>


### Always On:

    au VimEnter * RainbowParenthesesToggle
    au Syntax * RainbowParenthesesLoadRound
    au Syntax * RainbowParenthesesLoadSquare
    au Syntax * RainbowParenthesesLoadBraces

