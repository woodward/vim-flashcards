<ctrl>-^  ⮂  Switch back to the previous file (same as :e #) 

global command (abbreviation g)  ⮂  Globally (on all lines) execute command  
global! pattern command (abbreviation g! pattern command - same as v)  ⮂  On all lines not matching pattern execute command  

POSIX character classes

[:alnum:]  ⮂  Alphanumeric characters                                             
[:alpha:]  ⮂  Alphabetic characters                                               
[:blank:]  ⮂  Space and tab characters only                                       
[:cntrl:]  ⮂  Control characters                                                  
[:digit:]  ⮂  Numeric characters                                                  
[:graph:]  ⮂  Printable and visible (nonspace) characters                         
[:lower:]  ⮂  Lowercase characters                                                
[:print:]  ⮂  Printable characters (includes whitespace)                          
[:punct:]  ⮂  Punctuation characters                                              
[:space:]  ⮂  All whitespace characters (space, tab, newline, vertical tab, etc.) 
[:upper:]  ⮂  Uppercase characters                                                
[:xdigit:] ⮂  Hexadecimal digits                                                  

:g/^/m0/  ⮂  Reverse the order of all the lines in the file

* (resp. #) ⮂  Go to next (resp. previous) occurrence of the word under the cursor

<tab> <tab> <tab> ⮂  Cycle between options, such as :Packer <tab> <tab> <tab>  Use shift-<tab> to cycle backwards

Packer puts its plugins in: 
Loaded on startup:  ~/.local/share/nvim/site/pack/packer/start
Lazy loaded:        ~/.local/share/nvim/site/pack/packer/opt

For a plugin on GitHub, they will have a `doc` directory with a text file in there; that's the help file in nvim

~/.local/share/nvim  ⮂  Where Neovim stores plugins, LSP servers, etc.
~/.config/nvim       ⮂  Where Neovim stores config info
~/.cache/nvim        ⮂  Where Neovim stores cache stuff

gc (while in visual mode)                      ⮂  Comment line using the Comment plugin
<shift>j or <shift>-k (while in visual mode)   ⮂  Move lines up or down  
:lua vim.lsp.buf.formatting_sync()             ⮂  Format the file (from the Null LS plugin)
:NullLsInfo                                    ⮂  Show what Null LS source(s) are being used

Site with plugins:
https://vimawesome.com/

,b   ⮂  Bring up a list of currently open buffers
,ls  ⮂  See a list of symbols and functions in a file
gc (while in visual mode)  ⮂  Comment out a bunch of lines
gcc (while in normal mode) ⮂  Toggle the comment status of a line

v       ⮂  Character visual mode
V       ⮂  Line visual mode
ctrl-v  ⮂  Block visual mode

>       ⮂  Indent (while in visual mode, after highlighting a bunch of lines)
<       ⮂  Outdent (while in visual mode, after highlighting a bunch of lines)

:{range}sort       ⮂  Sort using the built-in vim sort
:{range}sort!      ⮂  Sort in reverse using the built-in sort
:{range}!sort      ⮂  Sort using the Unix sort
:{range}!sort -r   ⮂  Sort in reverse using the Unix sort

:wa  ⮂ Write all changed files (save all changes), and keep working

ctrl-v and then shift-i  ⮂  Go into insert mode in column mode. Kind of bogus; doesn't show you the changes while they are happening

ctrl-\  ⮂  Bring up toggleterm

,sk  ⮂   Brings up the current keymap

:s/foo/bar/g   ⮂  Change foo to bar in the current line
:%s/foo/bar/g  ⮂  Change foo to bar in the entire file

ctrl-o   ⮂  Go to last location
ctrl-i   ⮂  Go forward in locations

di{      ⮂  Delete everything inside of curly braces
da{      ⮂  Delete everything inside of curly braces, including the curly braces
ci{      ⮂  Change inside of curly braces
ca{      ⮂  Change everything inside of curly braces, including the curly braces
Also works with quotes, parens, etc.

i        ⮂  Inside
a        ⮂  Around

8j       ⮂  Jump down 8 lines 
f"       ⮂  Go ahead in the line to the double quote 
"        ⮂  Bring up the list of buffers 

z <enter> ⮂  Move the cursor to the top of the screen
z.        ⮂  Move the cursor to the middle of the screen
z-        ⮂  Move the cursor to the bottom of the screen

:set paste  ⮂  Turn off auto indentation when pasting code (:set nopaste to turn auto-indentation back on)  

ctrl-x ctrl-l  ⮂  Show line completions; in insert mode, type a few characters, and then ctrl-x ctrl-l (ctrl-n or ctrl-p to move through this list; ctrl-e halts the match without substituting)
ctrl-x ctrl-t  ⮂  Show thesauraus completions; in insert mode, type a few characters, and then ctrl-x ctrl-t
ctrl-x ctrl-k  ⮂  Show dictionary completions; in insert mode, type a few characters, and then ctrl-x ctrl-k

insert in visual column mode  ⮂  Highlight area with ctrl-v, shift-i, add text, ESC twice

:lua print(vim.fn.stdpath("data"))  ⮂  Print something (in this case the standard path "data" which is ~/.local/share/nvim)

:lua vim.lsp.set_log_level("debug")  and then  :lua vim.cmd('e'..vim.lsp.get_log_path())   ⮂  To see log output

:mksession mysession.vim  ⮂  Makes a session and stores it in "mysession.vim"
:source mysession.vim     ⮂  Re-establish or load this session
:set nowrap               ⮂  Don't wrap the lines of text (it scrolls off to the right of the screen)
:set wrap                 ⮂  Wrap the lines of text

xp                        ⮂  Swap two characters
ddp                       ⮂  Swap two lines
ctrl-f                    ⮂  Bring up list of recent commands

g-  ⮂  Maps to :earlier
g+  ⮂  Maps to :later
From Jeff Schomay - figure out the difference between undo and earlier!
https://coderwall.com/p/twr_bw/time-traveling-in-vim

:vg                  ⮂  Invert a global search; find lines which do NOT match this pattern
:vg/.*TEST..*PROD/d  ⮂  Find lines which do NOT have TEST.*PROD in them, and delete them

<spacebar>     ⮂  Right
<backspace>    ⮂  Left
<ctrl>-h       ⮂  Left
<ctrl>-n       ⮂  Down
<ctrl>-p       ⮂  Up

<ctrl-g        ⮂  Show the current line number