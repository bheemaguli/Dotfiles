# Dotfiles

### 1. To get started, install zsh in your linux system

```bash
sudo apt update && sudo apt upgrade
sudo apt install -y zsh
```

### 2. For zsh and its plugins, run

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" &
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting &
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions &
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use

```

### 3. My prefered oh-my-zsh theme is *eastwood*. Install this theme by

```bash
sudo vim .zshrc
```
and changing theme as 

```python
ZSH_THEME="eastwood"
```

### 4. Update plugins by 
```bash
sudo vim .zshrc
```

and update plugins to 

```python
plugins=(
	git 
	zsh-syntax-highlighting
	zsh-autosuggestions
	you-should-use $plugins
)
```

