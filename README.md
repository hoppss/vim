vim
==

# Introduction
A good vim configuration.

# Install

## Install configuration file:
1. `git clone https://github.com/feixia586/vim.git <dir>`
2. `ln <dir>/.vimrc ~/.vimrc`

## Install plugin:
1. `git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle`
2. start vim
3. run command ":BundleInstall" in vim

## Post-proprocessing:
For plugin YouCompleteMe (step 3~4 are for supporting C-family language):

1. `cd ~/.vim/bundle/YouCompleteMe`
2. `./install.sh --clang-completer` # This is for supporting C-family language
3. `cp ~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp/ycm/.ycm_extra_conf.py ~/`
4. modify .ycm_extra_conf.py if you have special need 

# Trouble shooting

When run command ":BundleInstall", there might be some prolbems:
- Some plugin can not be successfully installed. ==> **Solution:** search the plugin in website, then put the plugin folder in ~/.vim/bundle/

When doing ./install.sh --clang-completer, there might be some problems:
- CMake is required to build YouCompleteMe. ==> **Solution:** sudo apt-get install CMake
- Could NOT find PythonLibs (missing: PYTHON_LIBRARIES PYTHON_INCLUDE_DIRS). ==> **Solution:** sudo apt-get install python-dev

