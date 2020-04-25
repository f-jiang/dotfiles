1. Set up tmuxinator

```
# if ruby version < 2.4
sudo apt-add-repository ppa:brightbox/ruby-ng
sudo apt install ruby2.6

gem install --user-install tmuxinator
```

2. Symlink dotfiles:

```
ln -s {`pwd`,~}/.bashrc
ln -s {`pwd`,~}/.profile
ln -s {`pwd`,~}/.tmux.conf

mkdir -p ~/.config/tmuxinator
ln -s {`pwd`,~/.config/tmuxinator}/default-project.yml
```

3. [Set up vim](https://github.com/f-jiang/vim-config)

