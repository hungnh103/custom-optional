```
et nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()

Plugin 'VundleVim/Vundle.vim'
Plugin 'scrooloose/nerdtree'
Plugin 'kien/ctrlp.vim'
Plugin 'mattn/emmet-vim'
Plugin 'scrooloose/syntastic'
Plugin 'airblade/vim-gitgutter'
Plugin 'valloric/youcompleteme'
Plugin 'morhetz/gruvbox' 
Plugin 'vim-airline/vim-airline'
Plugin 'tpope/vim-commentary'
Plugin 'rking/ag.vim'
call vundle#end()            " required                                         

filetype plugin indent on    " required
autocmd StdinReadPre * let s:std_in=1


autocmd VimEnter * if argc() == 1 && isdirectory(argv()[0]) && !exists("s:std_in") | exe 'NERDTree' argv()[0] | wincmd p | ene | endif

" toggle NERDTree
map <C-t> :NERDTreeToggle<CR>


" set theme color
set background=dark                                                       
colorscheme gruvbox

" thiet lap tab 2
set tabstop=2
set shiftwidth=2
set softtabstop=2
set expandtab
set encoding=utf-8
set autoindent
set noswapfile
set backupdir=~/tmp,/tmp
set backupcopy=yes
set backupskip=/tmp/*,$TMPDIR/*,$TMP/*,$TEMP/*
set directory=/tmp
set autowrite
set number
set cursorline
set colorcolumn=80

" setting tab
set hidden
nnoremap <C-Right> :bnext<CR>
nnoremap <C-Left> :bprev<CR>
nnoremap <C-X> :bp<CR>:bd #<CR>
inoremap <C-Down> <Esc>:m +1<CR>==gi
inoremap <C-Up> <Esc>:m -2<CR>==gi
let g:airline#extensions#tabline#enabled = 1
let g:airline#extensions#tabline#buffer_nr_show = 1
let g:ag_working_path_mode="r"
set runtimepath^=~/.vim/bundle/ag
```
