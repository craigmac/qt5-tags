# Qt 5.12.3 Exuberant CTags tag files

This repo contains 'tags' files for use with Vim editor >7.0 (will not work with
Emacs and probably others).

It contains 5 of the most common headers used in Qt 5 development. In .pro
files these headers are represented by having the line:

`QT += core gui multimedia network widgets`

To include specific tag file in your Vim session, copy this repo locally and
from inside vim, add to the 'tags' option the paths to the additional tag files
you'd like to use. For example let's say I download the repo to
~/Downloads/qt-tags and in project I'd like to use the qtcore tags file--inside
Vim I could do:

`:set tags+=~/Downloads/qtcore`

or use all of them:

`:set tags+=foo/qtcore,foo/qtgui,foo/qtmultimedia,foo/qtwidgets`

## Local .vimrc project settings to help simplify

If you turn on per-directory .vimrc files in Vim with `:set exrc` then you
could put the project settings in a .vimrc file inside the project and source
that file to setup your project settings and tags files, e.g., `:source
~/project/myqt-project/.vimrc`

## Example .vimrc

Don't use this .vimrc, this is here as an example of one I use on my personal
project: Qt 5.12.3 on Windows 7 with GVim 8.1 (64-bit build).

```
" local vimrc, requires 'set exrc' in Vim

cd $HOME/projects/myqt-project

set path+=**
set path+=C:/Qt/5.12.3/mingw73_32/include
set path+=C:/Qt/5.12.3/mingw73_32/include/QtWidgets
set path+=C:/Qt/5.12.3/mingw73_32/include/QtMultimedia
set path+=C:/Qt/5.12.3/mingw73_32/include/QtGui
set path+=C:/Qt/5.12.3/mingw73_32/include/QtANGLE
set path+=C:/Qt/5.12.3/mingw73_32/include/QtNetwork
set path+=C:/Qt/5.12.3/mingw73_32/include/QtCore
set path+=C:/Qt/Tools/mingw730_32/lib/gcc/i686-w64-mingw32/7.3.0/include/c++
set path+=C:/Qt/Tools/mingw730_32/lib/gcc/i686-w64-mingw32/7.3.0/include/c++/i686-w64-mingw32
set path+=C:/Qt/Tools/mingw730_32/lib/gcc/i686-w64-mingw32/7.3.0/include/c++/backward
set path+=C:/Qt/Tools/mingw730_32/lib/gcc/i686-w64-mingw32/7.3.0/include
set path+=C:/Qt/Tools/mingw730_32/lib/gcc/i686-w64-mingw32/7.3.0/include-fixed
set path+=C:/Qt/Tools/mingw730_32/i686-w64-mingw32/include

set tags=./tags;,./lib-tags/qtcore,./lib-tags/qtgui,./lib-tags/qtmultimedia,./lib-tags/qtwidgets
```


