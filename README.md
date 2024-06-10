# Zero's dotfiles

My configs for my development environment on Linux/UNIX systems.

Configs included for:
- [Alacritty](https://github.com/alacritty/alacritty)
- [neovim](https://github.com/neovim/neovim) configured with [vim-plug](https://github.com/junegunn/vim-plug)
- [tmux](https://github.com/tmux/tmux) configured with [Oh my tmux!](https://github.com/gpakosz/.tmux)
- [zsh](https://www.zsh.org/) configured with [Zim](https://github.com/zimfw/zimfw)


### Recommended
- [eza](https://github.com/eza-community/eza)
- Powerlevel10k's recommended [font](https://github.com/romkatv/powerlevel10k#fonts)

### Installation
This repository is intended to be used with [GNU stow](https://www.gnu.org/software/stow/) to symlink the files, as explained [here](https://venthur.de/2021-12-19-managing-dotfiles-with-stow.html).

If you intend to use the included makefile to install all configs, GNU stow is required.

- Clone this repository:
    ```sh
    git clone https://github.com/memoryofzero/.dotfiles.git
    ```
- To install all configs, run `make` inside the cloned repository.

- If you would like to install a specific config instead, run
    ```sh
    stow --verbose --target=$$HOME [foldername]
    ```
    inside the cloned repository, where `[foldername]` is the name of the folder for the config you would like to install

- To use nvim config:
    - Install vim-plug:
        ```sh
        sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
       ```
    - Open nvim and `:PlugInstall` to install plugins

### Uninstalling configs
The included makefile can also be used to delete all configs.

To delete all configs, run `make delete` inside the cloned repository

### TODO
- document installed zsh modules
- document installed nvim plugins
