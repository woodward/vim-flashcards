:ab in out  ⮂  Use in as an abbreviation for out in insert mode
:unab in    ⮂  Remove the abbreviation for in


:ab                     ⮂  List abbreviations
:map string sequence    ⮂  Map characters string as sequence of commands. Use #1, #2, etc for the function keys
:unmap string           ⮂  Remove the map for characters string
:map                    ⮂  List character strings that are mapped
:map! string sequence   ⮂  Map characters string to input mode sequence
:unmap! string          ⮂  Remove input mode map for characters string (you may need to quote the characters with CTRL-V )
:map!                   ⮂  List character strings that are mapped for input mode
qx                      ⮂  Record typed characters into the register specified by letter x. If the letter is uppercase, append to the register
q                       ⮂  Stop recording 
@x                      ⮂  Execute the register specified by the letter x 
@@                      ⮂  Execute the last register command

