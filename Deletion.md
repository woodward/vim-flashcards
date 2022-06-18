dw ⮂ delete word
dW ⮂ delete word, including punctuation
D  ⮂ deletes from the current cursor position to the end of the line. Shortcut for d$

d}  ⮂  Delete next paragraph
d^  ⮂  Delete to the beginning of the line
d/pattern  ⮂  Delete up to the first occurrence of pattern
dn         ⮂  Delete to the next occurrence of pattern
dL         ⮂  Delete up to the last line on the screen
dfx        ⮂  Delete up to and including x on the current line
dtx        ⮂  Delete up to (but not including) x on the current line

de ⮂ delete only to the end of the word (and not the space)

dE ⮂ delete to the end of the word, including punctuation

db ⮂ delete backward

d$   ⮂  Delete to the end of the line
d0   ⮂  Delete to the beginning of the line
dd   ⮂  Delete line.  Same as D
ndd  ⮂  Delete n lines 


x  ⮂ delete a single character
X  ⮂ delete a single character (before the cursor)

dH        ⮂  Delete from cursor to top of screen
dL        ⮂  Delete from cursor to bottom of screen
d+        ⮂  Delete from cursor to next line
d5|       ⮂  Delete from cursor to column 5 of current line
2d)       ⮂  Delete from cursor to second sentence following
d{        ⮂  Delete from cursor to previous paragraph
d/pattern ⮂  Delete from cursor to pattern
dn        ⮂  Delete from cursor to next pattern
dG        ⮂  Delete from cursor to end of file
d9G       ⮂  Delete from cursor to line number 13
"a5dd     ⮂  Delete five lines into register a

:/Part I/,/Part II/-1d  ⮂  Delete to the line above “Part II”
:/main/+d               ⮂  Delete the line below “main”
:.,$d x                 ⮂  Delete from this line to the last line into register x
