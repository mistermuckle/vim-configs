# VIM Configuration

## Install

```bash
if [[ -a ~/.vim ]]; then
  mv ~/.vim ~/.vim.bak
fi
if [[ -a ~/.vimrc ]]; then
  mv ~/.vimrc ~/.vimrc.bak
fi
ln -s $PWD/dot-vim ~/.vim
ln -s $PWD/dot-vimrc ~/.vimrc
if [[ ! ( -d dot-vim/bundle || -d dot-vim/bundle/Vundle.vim ) ]]; then
  git clone https://github.com/VundleVim/Vundle.vim.git dot-vim/bundle/Vundle.vim
fi
```
