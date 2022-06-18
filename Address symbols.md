These are the address symbols in :ex commmands (not vi)

1,$                           ⮂  All the lines in the file
%                             ⮂  All lines; same as 1,$
x,y                           ⮂  Lines x through y
x;y                           ⮂  Lines x through y, with the current line reset to x before computing y 
0                             ⮂  The top of the file
.                             ⮂  The current line
num                           ⮂  Absolute line number num
$                             ⮂  The last line
x-n                           ⮂  n lines before x
x+n                           ⮂  n lines after x
-[num]                        ⮂  One or num lines previous
+[num]                        ⮂  One or num lines ahead
'x (Apostrophe.)              ⮂  The line marked with x
'' (Apostrophe apostrophe.)   ⮂  The previous mark
/pattern/                     ⮂  Forward to the line matching pattern
?pattern?                     ⮂  Backward to the line matching pattern