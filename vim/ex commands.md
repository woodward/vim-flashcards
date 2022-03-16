:6 <enter>   ⮂  Go to line 6
:1,3         ⮂  Print lines 1 - 3
:1s/screen/line/ ⮂  Substitute "line" for "screen" on line 1
d                ⮂  Delete lines
m                ⮂  Move lines
co               ⮂  Copy lines
t                ⮂  Copy lines (a synonym for co) 
:3,18d           ⮂  Delete lines 3 through 18 (inclusive)
:16,224m23       ⮂  Move lines 160 through 224 to follow line 23 (like delete and put in vi)
:23,29co100      ⮂  Copy lines 23 through 29 and put them after line 100 (like yank and put in vi)
:set number      ⮂  Display all line numbers
:set nu          ⮂  Display all line numbers (an abbreviation for :set number)
:set nonumber    ⮂  Turn off line numbers
:set nu!         ⮂  Toggle the line number setting
:=               ⮂  Print the total number of lines
:.=              ⮂  Print the line number of the current line
:/pattern/=      ⮂  Print the line number of the next line that matches pattern
.                ⮂  Stands for the current line
$                ⮂  Stands for the last line in the file
%                ⮂  Stands for the every line in the file (same as 1,$)
:.,$d            ⮂  Delete from the current line to the end of the file
:20,.m$          ⮂  Move from line 20 through the current line (inclusive) to the end of the file
:%d              ⮂  Delete all of the lines in the file
:%t$             ⮂  Copy all the lines and place them at the end of the file (making a consecutive duplicate)
:.,.+20d         ⮂  Delete from the current line through the next 20 lines
:226,$m.-2       ⮂  Move lines 226 through the end of the file to two lines above the current line
:.,+20#          ⮂  Display line numbers from the current line to 20 lines further on in the file
:-,+t0           ⮂  Copy three lines (the line above the cursor through the line below the cursor) and put them at the top of the file 
:/pattern/d      ⮂  Delete the next line containing pattern
:/pattern/+d     ⮂  Delete the line below the next line containing pattern. (You could also use +1 instead of + alone.)
::/pattern1/,/pattern2/d     ⮂  Delete from the first line containing pattern1 through the first line containing pattern2.
:.,/pattern/m23  ⮂  Take the text from the current line (.) through the first line containing pattern and put it after line 23

Use ? as the delimiter instead of / if you want to search backward in the file
The ex command deletes the entire range of addressed lines—in this case, both the current line and the line containing 
the pattern. All lines are deleted in their entirety.

:100;+5 p        ⮂  Prints from the current line to 5 lines past 100 lines from here
:/pattern/;+10 p ⮂  Print the next line containing pattern, plus the 10 lines that follow it
:g/pattern       ⮂  Find (move to) the last occurrence of pattern in the file

:g/pattern/p       ⮂  Find and display all lines in the file containing pattern. Vim displays the line and then prompts you, “Press ENTER or type command to continue.”
:g!/pattern/nu     ⮂  Find and display all lines in the file that don’t contain pattern; also display the line number for each line found
:60,124g/pattern/p ⮂  Find and display any lines between lines 60 and 124 containing pattern
|                  ⮂  A command separator, allowing you to combine multiple commands from the same ex prompt (in much the same way that a semicolon separates multiple commands at the shell prompt)

:1,3d | s/thier/their/  ⮂  Delete lines 1 through 3 (leaving you now on the top line of the file), and then make a substitution on the current line (which was line 4 before you invoked the ex prompt).
:1,5 m 10 | g/pattern/nu ⮂  Move lines 1 through 5 after line 10, and then display all lines (with numbers) containing pattern

:write (abbveviation :w)  ⮂  Write (save) the buffer to the file but do not exit
:quit (abbreviation :q)   ⮂  Quit the editor (and return to the shell prompt)
:wq                       ⮂  Write the file and then quit the editor. The write happens unconditionally, even if the file was not changed. This updates the modification time of the file
:wn                       ⮂  Write the file and then edit the next one
:xit (abbreviation :x)    ⮂  Write the file and then quit (exit) the editor. The file is written only if it has been modified.

The difference between :wq and :x is important when editing source code and using make, which performs actions based on file modification times.

:w!              ⮂  Write the file (override the warning)
:q!              ⮂  Quit the editor (override the warning)

:w practice.new  ⮂  Saves the buffer in a new file
:230,$w newfile  ⮂  Save from line 230 to end of file in newfile
:.,600w newfile  ⮂  Save from the current line to line 600 in newfile

:1,10w newfile  (and then) :340,$w >> newfile  ⮂  newfile would contain lines 1–10 and from line 340 to the end of the buffer

:read filename (abbreviation :r filename)  ⮂ Insert the contents of filename starting on the line after the cursor position in the file

:185r filename   ⮂  Read in the contents of filename, and place it after line 185
:$r filename     ⮂  Read in the contents of filename and place it at the end of the file
:0r filename     ⮂  Read in the contents of filename and place it at the beginning of the file

:/pattern/r filename       ⮂ Read in the contents of filename and place it after the line containing pattern
:next (abbreviation :n)    ⮂  Go to the next file named on the command line
:args (abbreviation ar)    ⮂  Display the argument list in the status line, with brackets around the current filename.
:edit (abbreviation e)     ⮂  Switch to editing the last named file
:prev (abbreviation prev)  ⮂  Go back to the previous file
:rewind (abbreviation rew) ⮂  Resets the current file to be the first file named on the command line
:last (abbreviation la)    ⮂  Move to the last file listed on the command line (the argument list)

:w, :e filename  ⮂  Write your current file, and then edit another file
%                ⮂  Current filename
#                ⮂  Alternate or previous filename
:e #             ⮂  Return to the first file
:r #             ⮂  Read the first file into the current file
:e!              ⮂  Discard your edits and return to the last saved version of the current file
:w %.new         ⮂  Save a second version of the current file with the extension ".new"
:ya              ⮂  Yank
:pu              ⮂  Put
:160,224ya       ⮂  Yank (copy) lines 160 through 224 into register a
:pu              ⮂  Put the contents of register a after the current line


Line deletion, moving, and copying:

print (abbreviation p)      ⮂  Print lines
#                           ⮂  Print lines with line numbers
delete (abbreviation d)     ⮂  Delete lines
move (abbreviation m)       ⮂  Move lines
copy (abbreviation co or t) ⮂  Copy lines (t is a short for "to")
yank (abbreviation ya)      ⮂  Yank lines into a named register
put (abbreviation pu)       ⮂  Put lines from a named register


Line addressing symbols:

n         ⮂  Line number n
.         ⮂  Current line
$         ⮂  Last line
%         ⮂  All lines in file
. +n      ⮂ Current line plus n
. -n      ⮂ Current line minus n
/pattern/ ⮂ Search forward for the first line that matches pattern
?pattern? ⮂ Search backward for the first line that matches pattern

Q                         ⮂  Switch to ex (vi command)
visual (abbreviation vi)  ⮂  Switch from ex to vi

:s/old/new/  ⮂  Change the first occurrence of the pattern "old" to "new" on the current line.  
"/" can be any delimiter

:s/old/new/g         ⮂  Change all of the occurrence of the pattern "old" to "new" on the current line.  
:50,100s/old/new/g   ⮂  Change all of the occurrence of the pattern "old" to "new" on lines 50 through 100
:1,$s/old/new/g      ⮂  Change all of the occurrence of the pattern "old" to "new" in the current file
:%s/old/new/g        ⮂  Change all of the occurrence of the pattern "old" to "new" in the current file
:1,30s/old/new/gc    ⮂  Change all of the occurrence of the pattern "old" to "new" on lines 50 through 100 with confirmation

When doing a substitution with confirmation ("c"):

y       ⮂  To substitute this match
n       ⮂  To skip this match
a       ⮂  To substitute this and all remaining matches q to quit substituting
l       ⮂  To substitute this match and then quit (“last”)
CTRL-E  ⮂  To scroll the screen up 
CTRL-Y  ⮂  To scroll the screen down 
ESC     ⮂  To quit substituting

/which        Search for which
cwthat <ESC>  Change to that
n             Repeat search
n             Repeat search, skip a change
.             Repeat change (if appropriate)
(Etc.)

:g/pattern/ command      ⮂  Apply a command across all relevant lines in a file
:g/# FIXME/d             ⮂  Delete all lines with FIXME comments on them
:g/# FIXME/s/FIXME/DONE/ ⮂  Change all instances of FIXME comments to say DONE
:g/# FIXME/s/FIXME/DONE/g ⮂  Change all instances of FIXME comments to say DONE (every instance of FIXME on that line)

The global command (:g) is most often used in tandem with the substitute command (s)

:%s/editer/editor/g       ⮂  Substitute "editor" for every occurrence of "editer" throughout the file
:g/pattern/s/old/new/g    ⮂  The first g tells the command to operate on all lines of the file that match pattern. On those lines containing pattern, ex is to replace (substitute, s) the characters matching old with the characters in new. The last g indicates that the substitution is to occur globally on that line. This means that all matches of old are replaced by new, not just the first match on each relevant line.
:g/string/s//new/g        ⮂  Search for lines containing string and substitutes for that same string; you don't have to repeat "string" if that's what you're going to replace

Note that:
:g/editer/s//editor/g 
has the same effect as:
:%s/editer/editor/g

You can combine the :g command with :d, :m, :co, and other ex commands besides :s

\n  ⮂ Replace the \n with the text matching the nth subpattern previously saved by \( and \), where n is a number from 1 to 9, and previously saved subpatterns (kept in hold buffers) are counted from the left on the line

\u or \l  ⮂  Cause the next character in the replacement string to be changed to uppercase or lowercase, respectively.
\U or \L and \e or \E  ⮂  \U and \L are similar to \u or \l, but all following characters are converted to uppercase or lowercase until the end of the replacement string or until \e or \E is reached. If there is no \e or \E, all characters of the replacement text are affected by the \U or \L.

A simple :s      ⮂   Is the same as :s//~/. In other words, repeat the last substitution. This can save enormous amounts of time and typing when you are working your way through a document making the same change repeatedly but you don’t want to use a global substitution.
&                ⮂   If you think of the & as meaning “the same thing” (as in, what was just matched), this command is relatively mnemonic. E.g., :%&g means repeat the last substitution everywhere
&                ⮂   The & key can be used as a vi-mode command to perform the :& command, i.e., to repeat the last substitution. This can save even more typing than :s <ENTER> —one keystroke versus three.

Besides the / character, you may use any nonalphanumeric, nonspace character as your delimiter, except backslash, 
double quotes, and the vertical bar (\, ", and |). 

:g/.*/mo0  ⮂  Reverse the order of lines in a file
:g!/Paid in full/s/$/ Overdue/  ⮂  On all lines not marked Paid in full, append the phrase Overdue. Instead of :g! you could also use :v

:set option    ⮂  Turn option on
:set nooption  ⮂  To turn a toggle option off

:set ic    ⮂  Specify that pattern searches should ignore case (full name of option is "ignorecase")
:set noic  ⮂  Specify that pattern searches are case sensitive
:set option! ⮂  Toggle the value of the option
:set all     ⮂  Show the values of all options
:set option? ⮂  Find out the current value of the option

Since the .exrc file is actually read by ex before it enters visual mode (vi), commands in .exrc need not have a preceding colon.

:so filename  ⮂  Short for "source" - read in this settings file
:!command     ⮂  Create a shell and execute the following Unix command
:sh           ⮂  Create a shell to execute several Unix commands
:read !date   ⮂  Call to the shell with the "date" command and read the result into your file(shortcut "r")

:96,99!sort  ⮂  Pass lines 96 through 99 through the Unix sort filter, and replace those lines with the output of sort
!)command    ⮂  Pass the next line through the Unix "command"

:ab abbr phrase  ⮂  abbr is an abbreviation for the specified phrase  
:ab imrc International Materials Research Center  ⮂  Abbreviate "imrc" to be "International Materials Research Center" 

Abbreviations expand as soon as you press a nonalphanumeric character (e.g., punc‐ tuation), a space, a carriage return, or ESC (returning to command mode). 

:ab ⮂  List your currently defined abbreviations

:map x sequence  ⮂   Define character x as a sequence of editing commands
:unmap x         ⮂  Disable the sequence defined for x
:map             ⮂  List the characters that are currently mapped
:map <leader>q :q<cr>  ⮂  You can now execute the ex command :quit with the keystrokes \q

By default mapleader has the value \

<ctrl>-v  ⮂  A control character so that you can use <enter>, <esc>, <backspace>, <delete> in a command to be mapped

There are, however, three control characters that must be escaped with a ^V. They are ^T, ^W, and ^X. 

Unfortunately, one character always has special meaning in ex commands, even if you try to quote it with CTRL-V . 
Recall that the vertical bar (|) has special meaning as a separator of multiple ex commands. You cannot use a vertical 
bar in insert mode maps.

:unmap! x  ⮂  Reinstate a character "x" for normal typing (i.e., unmap it)

:map #1 commands  ⮂  Map function key F1 to the series of commands  

gdd  ⮂  Delete the line into register g

:set autoindent  ⮂  Turn on autoindent for source code
<ctrl-t> (typed in insert mode)  ⮂  Indent another level
<ctrl-d> (typed in insert mode)  ⮂  Outdent a level

^ ^D  ⮂  Shift the cursor back to the beginning of the line, but only for the current line
0 ^D  ⮂  Shift the cursor back to the beginning of the line.  The current autoindent level is set to zero; the next line you enter is not autoindented
^U    ⮂  Erase the entire line you've typed so far

:set expandtab  ⮂  Expand tabs into spaces
:set list       ⮂  Show tabs as ^I and end-of-lines as $ (a temporary equivalent is the :l command)
:5,20 l         ⮂  Display lines 5 through 20 showing tab characters and end-of-line characters

:split          ⮂ Split a window horizontally
:vsplit         ⮂ Split a window vertically
:colorscheme <tab>  ⮂  Change colorscheme (tab through to select a different color scheme) 

:messages  ⮂  Go through all messages

:help x    ⮂  Help on a normal mode command
:help v_x  ⮂  Help on a visual mode command
:help i_x  ⮂  Help on an insert mode command
:help :command  ⮂  Help on a command-mode command
:help c_x       ⮂  Help on command-line editing
:help -r        ⮂  Help on a command-line argument
:help '         ⮂  Help on an option, e.g, :help 'textwidth'
:help /         ⮂  Help on a regular expression

:redo     ⮂  Redo a command (undo an undo)
<ctrl-r>  ⮂  Same as redo

:nmap   ⮂  Mapping on normal mode
:cmap   ⮂  Mapping on command mode
:vmap   ⮂  Mapping on visual mode


:jumps  ⮂  Show the jump list (for ctrl-o and ctrl-i navigation)
:checkhealth  ⮂  See if your neovim config is healthy 

:vimgrep def **/*.ex      ⮂  Search in all Elixir files for "def" (includes deps folder)
:vimgrep def lib/**/*.ex  ⮂  Search in all Elixir files for "def"

:resize -4                ⮂  Decreases the current horizontal window size by 4 lines
:resize +4                ⮂  Increases the current horizontal window size by 4 lines
:resize n                 ⮂  Set the horizontal current window size to n lines
:vertical resize n        ⮂  Set the current window width to n