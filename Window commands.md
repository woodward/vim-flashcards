ctrl-w h  ⮂  Go to window on the left
ctrl-w l  ⮂  Go to window on the right
ctrl-w j  ⮂  Go to window on the top
ctrl-w k  ⮂  Go to window on the bottom

ctrl-w s    ⮂  Split a window
:sp[lit]    ⮂  Split a window

:vsp[lit]   ⮂  Vertically split a window
ctrl-w v    ⮂  Vertically split a window

:sn[ext][file] ⮂  Edit the next file in the file list in the new window

:new           ⮂  Same as split, but create a new file
:new filename  ⮂  Open filename in new window
ctrl-w n       ⮂  Same as split, but create a new file
ctrl-w ^       ⮂  Open the new window with the alternate (previously edited) file

:sview      ⮂  Read-only version of split
:sfind      ⮂  Split the window and open file

ctrl-w w         ⮂  Move to the next window below or to the right. Note that this command (unlike ctrl-w j) cycles through all vim windows

ctrl-w downarrow ⮂  Move to the next window down (does not cycle through windows)
ctrl-w j         ⮂  Move to the next window down (does not cycle through windows)
ctrl-w p         ⮂  Move to the previous window

ctrl-w uparrow   ⮂  Move to the next window up (does not cycle through windows)
ctrl-w k         ⮂  Move to the next window up (does not cycle through windows)

ctrl-w leftarrow   ⮂  Move to the next window to the left (does not cycle through windows)
ctrl-w h           ⮂  Move to the next window to the left (does not cycle through windows)

ctrl-w rightarrow  ⮂  Move to the next window to the right (does not cycle through windows)
ctrl-w l           ⮂  Move to the next window to the right (does not cycle through windows)

ctrl-w shift-w     ⮂  Move to the next window above or to the left. This is the upward counterpart to the ctrl-w w command

ctrl-w t           ⮂  Move to the top leftmost window (t is mnemonic for "top")
ctrl-w b           ⮂  Move to the bottom rightmost window (b ios mnemonic for "bottom")

ctrl-p p           ⮂  Move to the previous (last accessed) window

ctrl-w r           ⮂  Rotate windows down or to the right
ctrl-w shift-r     ⮂  Rotate windows up or to the left

ctrl-w x           ⮂  Exchange two windows

ctrl-w shift-k     ⮂  Move the current window to the top of the screen, using the full width of the screen
ctrl-w shift-j     ⮂  Move the current window to the bottom of the screen, using the full width of the screen
ctrl-w shift-h     ⮂  Move the current window to the left of the screen, using the full height of the screen
ctrl-w shift-l     ⮂  Move the current window to the right of the screen, using the full height of the screen
ctrl-w shift-t     ⮂  Move the current window to a new tab

ctrl-w =          ⮂  Try to resize all windows equally
ctrl-w -          ⮂  Decrease the current window height by one line
ctrl-w +          ⮂  Increase the current window height by one line
ctrl-w <          ⮂  Decrease the current window width by one line
ctrl-w >          ⮂  Increase the current window width by one line
ctrl-w |          ⮂  Resize the current window width to the widest size possible
zn <enter>        ⮂  Set the current window height to n

ctrl-w ] or ctrl-w ^  ⮂  Split the window and open a window above the current window
ctrl-w g              ⮂  Splits the window, and creates a new window above the current window. In the new window, vim performs the command :tselect tag
ctrl-w g              ⮂  Splits the window, and creates a new window above the current window. In the new window, vim performs the command :tjump tag
ctrl-w f              ⮂  Splits the window and edit the filename under the cursor
ctrl-w shift-f        ⮂  Splits the window and edits the filename under the cursor
ctrl-w g f            ⮂  Opens the file under the cursor in a new tab (only if the file exists)
ctrl-w g shift-f      ⮂  Opens the file under the cursor in a new tab and positions the cursor on the line specified by the number following the filename in the first window

ctrl-pagedown         ⮂  Move one tab to the right
ctrl-pageup           ⮂  Move one tab to the left

ctrl-w q              ⮂  Quit the current window.  Same as :quit command
ctrl-w c              ⮂  Close the current window.  If the window is on a tab and it's the last window for the tab, the window and the tab are closed. Same as :close
:close[!]             ⮂  Close the current window (the ! makes it close even if there are changes)
ctrl-w o              ⮂  Close all of the windows except the current window.  Same as :only
:only[!]              ⮂  Close all of the windows except the current window (the ! closes them even if there are changes)
:hide[cmd]            ⮂  Close the current window and hide the buffer; execute cmd if it is present  
:res[ize] num         ⮂  Resize the window to num lines