https://www.youtube.com/watch?v=IoyW8XYGqjM&ab_channel=ThePrimeagen
This guy mapped it to ctrl-q (to open and close)
ctrl-j and ctrl-k to move around in global list
ctrl for global
leader for local
He has in .vimrc:
  autocmd! BufWrite,BufEnter,InsertLeave * : call LspLocationList()
to populate the location list for a file
(see: https://www.youtube.com/watch?v=IoyW8XYGqjM&t=399)
and then 
  fun! LspLocationList() 
    lua vim.lsp.diagnostic.set_loclist({open_loclist = false })
  endfun

:ldo g/$function/norm! Ilocal
norm! enters normal mode 
This puts "local" at the beginning of the line

:cnext (or :cn)       ⮂  Next global location
:cprev (or :cp)       ⮂  Previous global location
:copen                ⮂  Open the global quickfix table
:cdo                  ⮂  Do an action over every entry in the global list
:cwin (or :cwindow)   ⮂  See the last quickfix list
:cclose               ⮂  Close the quickfix window

:colder [n]  ⮂  Load the older list of errors (optional n to load the nth older list of errors)
:cnewer [n]   ⮂  Load the newer list of errors (optional n to load the nth older list of errors)

:lnext       ⮂  Next location
:lprev       ⮂  Previous location
:lopen       ⮂  Open the quickfix table for locations
:ldo         ⮂  Do an action over every entry in the local list

