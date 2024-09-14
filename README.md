# DPETER DOTFILES

## Setting up on a new machine

Add the following to your `.bashrc` or `.zshrc` file:

```bashrc
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

Also make sure that your source repository ignores the folder where you'll clone it, so that you don't create weird recursion problems:

```bash
echo ".cfg" >> .gitignore
```

Now clone the dotfiles into a bare repository into a "dot" folder of your `$HOME`:

```bash
git clone --bare https://github.com/diegopluna/dotfiles.git $HOME/.cfg
```
