# centos install vim from source:
```
yum groupinstall 'Development tools'
yum install ncurses ncurses-devel
git clone https://github.com/vim/vim
./configure --prefix=/usr --with-features=huge --enable-rubyinterp --enable-pythoninterp --enable-luainterp
make && make install
vim --version
```

# ubuntu install vim from source:
```
sudo apt-get install build-essential bison mercurial libreadline-dev libncurses-dev libgtk-3-dev libgtk2.0-dev libxt-dev libx11-dev
mkdir ~/local
mkdir ~/local/vim
echo 'PATH=$HOME/local/vim/bin:$PATH' >> ~/.profile
mkdir ~/src
$ cd ~/src
git clone https://github.com/vim/vim
$ cd ~/src
$ touch build_vim.sh
$ chmod +x build_vim.sh
cd ~/src/vim
rm src/auto/config.cache
./configure --prefix=$HOME/local/vim --enable-gui=gtk2 --enable-rubyinterp=yes --with-features=huge
make clean
make
make install
make clean
$ cd ~/src
$ ./build_vim.sh
$ vim --version
```

# compile computeme:
```
cd ~/.vim/bundle/YouCompleteMe/
git submodule update --init --recursive


cd ~/.vim/bundle/YouCompleteMe
./install.py
#./install.py --clang-completer 
```