vim
===

.vimrc
------

.. code-block:: vim
	set number
	set breakindent
	syntax on
	highlight ExtraWhitespace ctermbg=red guibg=red
	match ExtraWhitespace /\s\+$/
	autocmd FileType tex setlocal tabstop=2
	autocmd FileType html setlocal tabstop=2