---
title:  "VIM Settings"
layout: archive
---
After trying a lot of IDEs and editors, I still feel that VIM/Neovim is what I 
want. In order to use the same editor 
at every machine, I decided not to use any plugin.
Here I would like to share my .vimrc.

```
set nocompatible              
filetype off                 

set nocompatible
set timeoutlen=1000 ttimeoutlen=0
set number
set guioptions-=r
set guioptions-=L
set guioptions-=b
set showtabline=1
syntax on
let g:solarized_termcolors=256  
set background=dark 
colorscheme darkblue
set textwidth=1000
set fileformat=unix
set cindent     
set tabstop=4   
set shiftwidth=4    
set showmatch   
set scrolloff=5 
set laststatus=2    
set fenc=utf-8      
set backspace=2
set selection=exclusive
set selectmode=mouse,key
set matchtime=5
set ignorecase      
set incsearch
set hlsearch        
set noexpandtab     
set whichwrap+=<,>,h,l
set autoread
set cursorline      
set splitright
set splitbelow

let g:netrw_banner=0 " Hide the directory banner
let g:netrw_liststyle=3		" 0=thin; 1=long; 2=wide; 3=tree
let g:netrw_browse_split=4
let g:netrw_preview = 1
let g:netrw_altv = 1
let g:netrw_winsize = 15

"Now define some map"
nnoremap <C-e> :Vex<CR>
nnoremap <C-n> :bn<CR>
nnoremap <C-p> :bp<CR>
nnoremap <C-u> :buffers<CR>

" Following is for column visual
nnoremap <C-L> <C-V>


" Indent
au BufNewFile,BufRead *.py,*.php,*.rb,*.html,*.js,*.ts,*.md
    \ set tabstop=4 |
    \ set softtabstop=4 |
    \ set shiftwidth=4 |
    \ set textwidth=200 |
    \ set expandtab |
    \ set autoindent |
    \ set fileformat=unix

" utf-8
set encoding=utf-8

" highlight
" let python_highlight_all=1
"color setting"
hi String ctermfg = green
hi Number ctermfg = red
```

If you are also a VIMer by chance, cheers!
