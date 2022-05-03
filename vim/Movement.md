'x  ⮂  Move the cursor to the first character of the line marked by x
`x  ⮂  Move the cursor to the character marked by x
``  ⮂  Return to the exact position of the previous mark or context after a move
''  ⮂  Return to the beginning of the line of the previous mark or context

%  ⮂  Jump to the closing parentheses (or [ or {) and back again

w   ⮂   Go to the start of the following word
b   ⮂   Go to the start of the previous word
e   ⮂   Go to the end of this word

W   ⮂   Go to the start of the following WORD
B   ⮂   Go to the start of the previous WORD
E   ⮂   Go to the end of this WORD.
ge  ⮂   End of previous word
gE  ⮂   End of previous Word
)   ⮂   Beginning of next sentence
(   ⮂   Beginning of previous sentence
}   ⮂   Beginning of next paragraph
{   ⮂   Beginning of previous paragraph
]]  ⮂   Beginning of next section
[[  ⮂   Beginning of previous section
][  ⮂   End of next section
[]  ⮂   End of previous section


See here:
https://github.com/unblevable/quick-scope#moving-across-a-line

f<char>   ⮂  Moves your cursor to the first occurrence of <char> to the right
F<char>   ⮂  Moves your cursor to the first occurrence of <char> to the left
t<char>   ⮂  Moves your cursor right before the first occurrence of <char> to the right
T<char>   ⮂  Moves your cursor right before the first occurrence of <char> to the left

The character motions can take a preceding count, but in practice, Vim users tend to use the ; and , to repeat a character motion any number of times.

;         ⮂  Repeat the last character motion in the original direction
,         ⮂  Repeat the last character motion in the opposite direction

gg   ⮂  Shortcut for 1G - go to the beginning of the file

nG        ⮂  Go to line number n
G         ⮂  Go to the last line in the file
:n        ⮂  Go to line number n

0    ⮂  Go to column 0
^    ⮂  Go to first character on the line
$    ⮂  Go to the last column
g_   ⮂  Go to the last character on the line
fa   ⮂  Go to next occurrence of the letter a on the line. , (resp. ;) will find the next (resp. previous) occurrence
t,   ⮂  Go to just before the character ,
3fx  ⮂  Find the 3rd occurrence of x on this line
F and T ⮂ like f and t but backward
dt"  ⮂ remove everything until the "
+    ⮂ Go to first non-blank character of previous line
-    ⮂ Go to first non-blank character of next line


<enter>    ⮂  Go to first non-blank character of next line
g0         ⮂  Go to first position of the screen line
g$         ⮂  Go to last position of the screen line
gm         ⮂  Go to the middle of the screen
gk         ⮂  Move up one screen line
gj         ⮂  Move down one screen line
H          ⮂  Go to the top of the screen
M          ⮂  Go to the middle of the screen
L          ⮂  Go to the bottom of the screen
nH         ⮂  Move to the first character n lines below the top line
nL         ⮂  Move to the first character n lines above the bottom line

ctrl-f   ⮂  Scroll forward one screen
ctrl-b   ⮂  Scroll backward one screen
ctrl-d   ⮂  Scroll down half a screen
ctrl-u   ⮂  Scroll up half a screen
ctrl-e   ⮂  Scroll the screen down, keeping the line at the same position
ctrl-y   ⮂  Scroll the screen up, keeping the line at the same position
