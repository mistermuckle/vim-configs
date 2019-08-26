if strlen(finddir('~/.vim/bundle/Vundle.vim')) > 0
    set nocompatible              " be iMproved, required
    filetype off                  " required

    " set the runtime path to include Vundle and initialize
    set rtp+=~/.vim/bundle/Vundle.vim
    call vundle#begin()
    " alternatively, pass a path where Vundle should install plugins
    "call vundle#begin('~/some/path/here')

    " let Vundle manage Vundle, required
    Plugin 'VundleVim/Vundle.vim'
    Plugin 'rizzatti/dash.vim'
    Plugin 'pangloss/vim-javascript'
    Plugin 'mxw/vim-jsx'

    " All of your Plugins must be added before the following line
    call vundle#end()            " required
    filetype plugin indent on    " required
    " To ignore plugin indent changes, instead use:
    "filetype plugin on
    "
    " Brief help
    " :PluginList       - lists configured plugins
    " :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
    " :PluginSearch foo - searches for foo; append `!` to refresh local cache
    " :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
    "
    " see :h vundle for more details or wiki for FAQ
    " Put your non-Plugin stuff after this line
endif

syntax on
set number
set ai
set shiftwidth=2
set expandtab
set nohlsearch
set shell=bash\ --login
set foldmethod=syntax
set foldlevelstart=99
colorscheme pablo

au BufNewFile *.test.jsx au! BufNewFile *.jsx
au BufNewFile *.test.jsx silent 0read ~/.vim/skeleton.test.jsx
au BufNewFile *.test.jsx normal Gdd
au BufNewFile *.test.jsx execute '%s/XXX/' . substitute(bufname('%'), '^\(.*\/\)*\(.*\)\.test\.jsx$', '\2', '') . '/g'
au BufNewFile *.test.jsx normal gg

au BufNewFile *.jsx silent 0read ~/.vim/skeleton.jsx
au BufNewFile *.jsx normal Gdd
au BufNewFile *.jsx execute '%s/XXX/' . substitute(bufname('%'), '^\(.*\/\)*\(.*\)\.jsx$', '\2', '') . '/g'
au BufNewFile *.jsx normal gg

" Append the JIRA ticket # to the end of the line
imap jjira <ESC>:read !jiranum<ESC>^i(<ESC>$a)<ESC>kJ
