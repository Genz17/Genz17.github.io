---
title:  "VIM Settings"
layout: archive
---
After trying a lot of IDEs and editors, I still feel that VIM/Neovim is what I 
want. Here I would like to share my .vimrc.

```
set nocompatible              
filetype off                 

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'git@github.com:gmarik/Vundle.vim.git'

" Add all your plugins here (note older versions of Vundle used Bundle instead of Plugin

Plugin 'git@github.com:jistr/vim-nerdtree-tabs.git'
Plugin 'git@github.com:vim-airline/vim-airline.git'
Plugin 'git@github.com:vim-airline/vim-airline-themes.git'
Plugin 'git@github.com:iamcco/markdown-preview.nvim.git'
Plugin 'git@github.com:preservim/nerdtree.git'
Plugin 'git@github.com:jiangmiao/auto-pairs.git'
Plugin 'git@github.com:preservim/vim-markdown.git'
Plugin 'git@github.com:iamcco/mathjax-support-for-mkdp.git'
Plugin 'git@github.com:morhetz/gruvbox.git'

" All of your Plugins must be added before the following line

" Some more settings to the Plugins

" airline
let g:airline_theme="powerlineish" 
" let g:airline_powerline_fonts = 1   
let g:airline#extensions#clock#auto = 1

 let g:airline#extensions#tabline#enabled = 3 
 let g:airline#extensions#tabline#buffer_nr_show = 1

 nnoremap <C-N> :bn<CR>
 nnoremap <C-P> :bp<CR> 
 let g:airline#extensions#whitespace#enabled = 0
 let g:airline#extensions#whitespace#symbol = '!'


" python highlight
let g:python_highlight_all = 1


" markdown
let g:vim_markdown_folding_disabled = 1
let g:mkdp_echo_preview_url = 1
let g:vim_markdown_math = 1
"function OpenMarkdownPreview (url)
"execute "ter xdg-open " . a:url
"execute "q"
"endfunction
"let g:mkdp_browserfunc = 'OpenMarkdownPreview'

call vundle#end()            " required
filetype plugin indent on    " required



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
colorscheme gruvbox
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
"Now define some map"
nnoremap <C-Left> <C-W>h
nnoremap <C-Right> <C-W>l
nnoremap <C-Up> <C-W>k
nnoremap <C-Down> <C-W>j
nnoremap <A-Left> <C-w>H
nnoremap <A-Right> <C-w>L
nnoremap <A-Up> <C-w>K
nnoremap <A-Down> <C-w>J

nnoremap <C-T> :NERDTree<cr>
" Following is for column visual
nnoremap <C-L> <C-V>

let g:asyncrun_open=10
let g:asyncrun_save=1


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
let python_highlight_all=1

"color setting"
hi String ctermfg = green
hi Number ctermfg = red
```

If you are also a VIMer by chance, cheers!
