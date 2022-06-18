yH        ⮂  Copy from cursor to top of screen
yL        ⮂  Copy from cursor to bottom of screen
y+        ⮂  Copy from cursor to next line
y5|       ⮂  Copy from cursor to column 5 of current line
2y)       ⮂  Copy from cursor to second sentence following
y{        ⮂  Copy from cursor to previous paragraph
y/pattern ⮂  Copy from cursor to pattern
yn        ⮂  Copy from cursor to next pattern
yG        ⮂  Copy from cursor to end of file
y9G       ⮂  Copy from cursor to line number 13
Y         ⮂  Copy the current line (same as yy)
yy        ⮂  Copy the current line (same as Y)
ye        ⮂  Copy to the end of the word
yw        ⮂  Copy to the end of the word (and include whitespace)
y$        ⮂  Copy the rest of the line
y]]       ⮂  Copy up to the next section heading
J         ⮂  Join the current line to the next line
gJ        ⮂  Join the current line to the next line (but don't leave a space)
:j        ⮂  Join the current line to the next line (same as J)
:j!       ⮂  Join the current line to the next line (but don't leave a space) - same as gJ


"2p       ⮂  The deletion in register 2 is placed after the cursor
"1pu.u.u  ⮂  Cycle through the registers (undoing as you go) until you get the deleted text you want
"dyy      ⮂  Yank the current line into register d
"a7yy     ⮂  Yank the next seven lines into register a
"dP       ⮂  Put the contents of register d before the cursor 
"ap       ⮂  Put the contents of register a after the cursor
"Zy)      ⮂  Add the next sentence to register z
"bcommand ⮂  Do command with register b
"f4yy     ⮂  Yank four lines into register f
"fp       ⮂  Place yanked text below the cursor

Jeff Schomay has this:  keymap("v", "p", '"_dP', opts) which keeps the last item in the paste buffer so you can paste multiple times (?)
