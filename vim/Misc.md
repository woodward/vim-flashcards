mx  ⮂  Mark the current position with x (x can be any letter, upper or lowercase)
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

xp  ⮂  Swap two characters
ddp  ⮂  Swap two lines
:g/^/m0/  ⮂  Reverse the order of all the lines in the file

gg   ⮂  Shortcut for 1G - go to the beginning of the file

%  ⮂  Jump to the closing parentheses (or [ or {) and back again

w   ⮂   Go to the start of the following word,
e   ⮂   Go to the end of this word

W   ⮂   Go to the start of the following WORD,
E   ⮂   Go to the end of this WORD.

* (resp. #) ⮂  Go to next (resp. previous) occurrence of the word under the cursor

0    ⮂  Go to column 0
^    ⮂  Go to first character on the line
$    ⮂  Go to the last column
g_   ⮂  Go to the last character on the line
fa   ⮂  Go to next occurrence of the letter a on the line. , (resp. ;) will find the next (resp. previous) occurrence
t,   ⮂  Go to just before the character ,
3fx  ⮂  Find the 3rd occurrence of x on this line
F and T ⮂ like f and t but backward
dt"  ⮂ remove everything until the "

<ctrl>-w h  ⮂  Go to window on the left
<ctrl>-w l  ⮂  Go to window on the right
<ctrl>-w j  ⮂  Go to window on the top
<ctrl>-w k  ⮂  Go to window on the bottom

<tab> <tab> <tab> ⮂  Cycle between options, such as :Packer <tab> <tab> <tab>  Use shift-<tab> to cycle backwards

Packer puts its plugins in: 
Loaded on startup:  ~/.local/share/nvim/site/pack/packer/start
Lazy loaded:        ~/.local/share/nvim/site/pack/packer/opt

For a plugin on GitHub, they will have a `doc` directory with a text file in there; that's the help file in nvim

~/.local/share/nvim  ⮂  Where Neovim stores plugins, LSP servers, etc.
~/.config/nvim       ⮂  Where Neovim stores config info

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
z        ⮂  Move the cursor to the top of the screen

:set paste  ⮂  Turn off auto indentation when pasting code (:set nopaste to turn auto-indentation back on)  

ctrl-x ctrl-l  ⮂  Show line completions; in insert mode, type a few characters, and then ctrl-x ctrl-l (ctrl-n or ctrl-p to move through this list; ctrl-e halts the match without substituting)
