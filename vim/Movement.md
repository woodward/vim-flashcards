'x  ⮂  Move the cursor to the first character of the line marked by x
`x  ⮂  Move the cursor to the character marked by x
``  ⮂  Return to the exact position of the previous mark or context after a move
''  ⮂  Return to the beginning of the line of the previous mark or context


See here:
https://github.com/unblevable/quick-scope#moving-across-a-line

f<char>   ⮂  Moves your cursor to the first occurrence of <char> to the right
F<char>   ⮂  Moves your cursor to the first occurrence of <char> to the left
t<char>   ⮂  Moves your cursor right before the first occurrence of <char> to the right
T<char>   ⮂  Moves your cursor right before the first occurrence of <char> to the left

The character motions can take a preceding count, but in practice, Vim users tend to use the ; and , to repeat a character motion any number of times.

;         ⮂  Repeat the last character motion in the original direction
,         ⮂  Repeat the last character motion in the opposite direction
