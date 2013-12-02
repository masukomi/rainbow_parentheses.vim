# Rainbow Parentheses

<style type="text/css">
	<!--
	pre { white-space: pre-wrap; font-family: monospace; color: #ffffff; background-color: #303030; }
	#rainbow_example { font-family: monospace; color: #ffffff; background-color: #303030; }
	* { font-size: 1em; }
	.level1c { color: #ffdead; }
	.level2c { color: #2f4f4f; }
	.level3c { color: #696969; }
	.level4c { color: #778899; }
	.level5c { color: #8470ff; }
	.level16c { color: #b22222; }
	.level6c { color: #4682b4; }
	.level7c { color: #20b2aa; }
	.level8c { color: #6b8e23; }
	.level9c { color: #9acd32; }
	.level10c { color: #bdb76b; }
	.level11c { color: #fafad2; }
	.level12c { color: #ffd700; }
	.level13c { color: #b8860b; }
	.level14c { color: #8b4513; }
	.level15c { color: #d2691e; }
	.LineNr { color: #ffff00; }
	.Constant { color: #ffa0a0; }
	-->
</style>

<div id="rainbow_example">
	<pre id='vimCodeElement'>
	<span id="L1" class="LineNr">An example for you: </span>
	<span class="level16c">(</span><span class="level15c">(</span><span class="level14c">(</span><span class="level13c">(</span><span class="level12c">(</span><span class="level11c">(</span><span class="level10c">(</span><span class="level9c">(</span><span class="level8c">(</span><span class="level7c">(</span><span class="level6c">(</span><span class="level5c">(</span><span class="level4c">(</span><span class="level3c">(</span><span class="level2c">(</span><span class="level1c">(</span> <span class="Constant">&quot;hi&quot;</span> <span class="level1c">)</span><span class="level2c">)</span><span class="level3c">)</span><span class="level4c">)</span><span class="level5c">)</span><span class="level6c">)</span><span class="level7c">)</span><span class="level8c">)</span><span class="level9c">)</span><span class="level10c">)</span><span class="level11c">)</span><span class="level12c">)</span><span class="level13c">)</span><span class="level14c">)</span><span class="level15c">)</span><span class="level16c">)</span>
	<span class="level16c">[</span><span class="level15c">[</span><span class="level14c">[</span><span class="level13c">[</span><span class="level12c">[</span><span class="level11c">[</span><span class="level10c">[</span><span class="level9c">[</span><span class="level8c">[</span><span class="level7c">[</span><span class="level6c">[</span><span class="level5c">[</span><span class="level4c">[</span><span class="level3c">[</span><span class="level2c">[</span><span class="level1c">[</span> <span class="Constant">&quot;hi&quot;</span> <span class="level1c">]</span><span class="level2c">]</span><span class="level3c">]</span><span class="level4c">]</span><span class="level5c">]</span><span class="level6c">]</span><span class="level7c">]</span><span class="level8c">]</span><span class="level9c">]</span><span class="level10c">]</span><span class="level11c">]</span><span class="level12c">]</span><span class="level13c">]</span><span class="level14c">]</span><span class="level15c">]</span><span class="level16c">]</span>
	<span class="level16c">{</span><span class="level15c">{</span><span class="level14c">{</span><span class="level13c">{</span><span class="level12c">{</span><span class="level11c">{</span><span class="level10c">{</span><span class="level9c">{</span><span class="level8c">{</span><span class="level7c">{</span><span class="level6c">{</span><span class="level5c">{</span><span class="level4c">{</span><span class="level3c">{</span><span class="level2c">{</span><span class="level1c">{</span> <span class="Constant">&quot;hi&quot;</span> <span class="level1c">}</span><span class="level2c">}</span><span class="level3c">}</span><span class="level4c">}</span><span class="level5c">}</span><span class="level6c">}</span><span class="level7c">}</span><span class="level8c">}</span><span class="level9c">}</span><span class="level10c">}</span><span class="level11c">}</span><span class="level12c">}</span><span class="level13c">}</span><span class="level14c">}</span><span class="level15c">}</span><span class="level16c">}</span>
	</pre>
</div>

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
