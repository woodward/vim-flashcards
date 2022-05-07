:r file           ⮂  Read in the contents of file after the cursor
:r !command       ⮂  Read in the output from command after the current line
:numr !command    ⮂  Like previous, but place after line num (use zero for the top of the file) 
:! command        ⮂  Run command, then return
!motion command   ⮂  Send the text covered by motion to command; replace with output 
:n,m !command     ⮂  Send lines n–m to command; replace with output
num !! command    ⮂  Send num lines to command; replace with output
:!!               ⮂  Repeat the last system command
:sh               ⮂  Create a subshell; return to editor with EOF
CTRL-Z            ⮂  Suspend the editor, resume with fg. This iconifies gvim
:so file          ⮂  Read and execute ex commands from file
