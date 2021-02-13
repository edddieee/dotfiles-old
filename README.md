# dotfiles

## Zsh
```
$ sudo pacman -S zsh
$ zsh --version
$ chsh -s $(which zsh)
$ ln -s -f ~/.dotfiles/zsh/zshrc ~/.zshrc.local

# In your ~/.zshrc file add the following code:
[[ -f ~/.zshrc.local ]] && source ~/.zshrc.local
```

## Oh My Zsh
```
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Alacritty
```
$ sudo pacman -S alacritty
```

To set alacritty as the default terminal, modify this line in `~/.config/i3/config`:

```
bindsym $mod+Return exec alacritty
```

## Tmux
```
$ sudo pacman -S tmux
$ ln -s ~/.dotfiles/tmux/tmux.conf ~/.tmux.conf
```

## Neovim
```
$ sudo pacman -Sy neovim
$ mkdir -p ~/.config/nvim
$ touch ~/.config/nvim/init.vim
$ ln -s -f ~/.dotfiles/vim/init.vim ~/.config/nvim/init.vim
```

**vim-plug**
```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

**ripgrep (rg)**
```
$ sudo pacman -S ripgrep
```

**editorconfig**
```
$ sudo pacman -S editorconfig-core-c
```

**PlugInstall**
Open the `~/.dotfiles/vim/Plugfile.vim` and then run `:PlugInstall`
