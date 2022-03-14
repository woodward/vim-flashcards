LSP Installer:
https://github.com/williamboman/nvim-lsp-installer

Keybindings:
https://rishabhrd.github.io/jekyll/update/2020/09/19/nvim_lsp_config.html

:LspInstallInfo   ⮂  Show the installed and available language servers
go to item in lsp server list, and press "i"  ⮂  Installs the language server
?                                             ⮂  Bring up the LSP Install help menu
u                                             ⮂  Uninstall a server
:LspInfo                                      ⮂  Shows the active language server
K                                             ⮂  Brings up documentation for a function or module
,lf                                           ⮂  Format code

gd                                            ⮂  Go to definition
K                                             ⮂  Bring up hover dialogue (a 2nd K lets you navigate within that window, and :q closes it)
gD                                            ⮂  Go to declaration

,lj                                           ⮂  Next diagnostic
,lk                                           ⮂  Previous diagnostic
,ls                                           ⮂  Document symbols  


	map('n','gD','<cmd>lua vim.lsp.buf.declaration()<CR>')
	map(G'n','gd','<cmd>lua vim.lsp.buf.definition()<CR>')
	map('n','K','<cmd>lua vim.lsp.buf.hover()<CR>')
	map('n','gr','<cmd>lua vim.lsp.buf.references()<CR>')
	map('n','gs','<cmd>lua vim.lsp.buf.signature_help()<CR>')
	map('n','gi','<cmd>lua vim.lsp.buf.implementation()<CR>')
	map('n','gt','<cmd>lua vim.lsp.buf.type_definition()<CR>')
	map('n','<leader>gw','<cmd>lua vim.lsp.buf.document_symbol()<CR>')
	map('n','<leader>gW','<cmd>lua vim.lsp.buf.workspace_symbol()<CR>')
	map('n','<leader>ah','<cmd>lua vim.lsp.buf.hover()<CR>')
	map('n','<leader>af','<cmd>lua vim.lsp.buf.code_action()<CR>')
	map('n','<leader>ee','<cmd>lua vim.lsp.util.show_line_diagnostics()<CR>')
	map('n','<leader>ar','<cmd>lua vim.lsp.buf.rename()<CR>')
	map('n','<leader>=', '<cmd>lua vim.lsp.buf.formatting()<CR>')
	map('n','<leader>ai','<cmd>lua vim.lsp.buf.incoming_calls()<CR>')
	map('n','<leader>ao','<cmd>lua vim.lsp.buf.outgoing_calls()<CR>')
