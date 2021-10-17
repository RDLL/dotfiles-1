"Identación y visualización de texto
syntax on	" Activa el resaltado de sintaxis
filetype plugin indent on	" Activa la identación basado en el tipo de archivo
" Install vim-plug if it's not already installed.
if empty(glob('~/.vim/autoload/plug.vim'))
silent !curl -fLo ~/.vim/autoload/plug.vim --create-dirs
\ https://raw.github.com/junegunn/vim-plug/master/plug.vim
autocmd VimEnter * PlugInstall --sync | source $MYVIMRC
endif

set encoding=utf-8
set number
set autoindent	" Respeta la identación al iniciar una nueva linea
set expandtab	" Expande los tabs a espacios. Esencial para python
set tabstop=4	" Tamaño del espacio de tabulador
set shiftwidth=4	"Numero de espacios para el autoidentado
set foldmethod=indent
set laststatus=2

"Ayudas o mejoras
set wildmenu    " Activa la mejora con tab autocompletado
set wildmode=list:longest,full " Completa hasta la cadena mas larga
" Entonces abre el wildmenu
set hlsearch    "Resalta las coincidencias de búsqueda
set incsearch   "Te mueve al primer resultado de búsqueda

set backspace=2	" Arregla el espacio del retroceso de muchas terminales

colorscheme murphy  " Cambia el color del resaltado de sintaxis

set directory=$HOME/.vim/swap//

inoremap ' ''<esc>i
inoremap " ""<esc>i
inoremap ( ()<esc>i
inoremap { {}<esc>i
inoremap [ []<esc>i
inoremap < <><esc>i
"Plugins
silent! helptags ALL    " Carga los archivos de ayuda para todos los plugins
"Manejo de plugins con vim-plug
call plug#begin()

Plug 'preservim/nerdtree'
Plug 'tpope/vim-vinegar'
Plug 'ctrlpvim/ctrlp.vim'
Plug 'mileszs/ack.vim'
Plug 'easymotion/vim-easymotion'
Plug 'junegunn/goyo.vim', { 'for': 'markdown' }
Plug 'tpope/vim-fugitive'
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'bfrg/vim-cpp-modern'
Plug 'ryanoasis/vim-devicons'
Plug 'vim-scripts/ScrollColors'
Plug 'flazz/vim-colorschemes'
Plug 'JuliaEditorSupport/julia-vim'
Plug 'frazrepo/vim-rainbow'

call plug#end()

if exists('+termguicolors')
  let &t_8f="\<Esc>[38;2;%lu;%lu;%lum"
  let &t_8b="\<Esc>[48;2;%lu;%lu;%lum"
  set termguicolors
endif

colorscheme luna

" Load powerline.
python3 from powerline.vim import setup as powerline_setup
python3 powerline_setup()
python3 del powerline_setup

let NERDTreeShowBookmarks = 1  " Display bookmarks on startup.
let g:rainbow_active = 1

" Key bindings personalizados
let mapleader = "\<space>"
noremap <leader>w :w<cr>
noremap <leader>n :NERDTreeToggle<cr>
noremap <leader>q :wqa<cr>
noremap <leader>c :bd<cr>
noremap <leader><up> <c-w><c-k>
noremap <leader><down> <c-w><c-j>
noremap <leader><right> <c-w><c-l>
noremap <leader><left> <c-w><c-h>
noremap <leader>t :tabnew<cr> 
