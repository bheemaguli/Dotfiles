# Dotfiles

### 1. To get started, install zsh in your linux system

```bash
sudo apt update && sudo apt upgrade
sudo apt install -y zsh
```

### 2. For zsh and its plugins, run

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" &&
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting &&
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions &&
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use

```

If ``raw.githubusercontent.com`` is blocked, add below to allowed hosts

```bash
sudo echo "185.199.108.133 raw.githubusercontent.com" >> /etc/hosts

```

### 3. My prefered oh-my-zsh theme is *eastwood*. Install this theme by

```bash
sudo vim ~/.zshrc
```
and changing theme as 

```python
ZSH_THEME="eastwood"
```

### 4. Update plugins by 
```bash
sudo vim ~/.zshrc
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

Save and close vim by ESC -> :wq


TODO:
0. Update to omarchy
1. Add background
2. Handle multi-monitor with external as main
```sh
monitor = eDP-1, 1920x1080@60, 1920x0, 1.33
monitor = HDMI-A-1, 1920x1080@60, 0x0, 1
```
3. Update workspace switching
```sh
# Tiling workspaces
workspace= 1, monitor:HDMI-A-1, default:true
workspace= 2, monitor:eDP-1, default:true
workspace= 3, monitor:HDMI-A-1, default:true
workspace= 4, monitor:eDP-1, default:true
workspace= 5, monitor:HDMI-A-1, default:true
workspace= 6, monitor:eDP-1, default:true
workspace= 7, monitor:HDMI-A-1, default:true
workspace= 8, monitor:eDP-1, default:true
workspace= 9, monitor:HDMI-A-1, default:true
workspace= 10, monitor:eDP-1, default:true
workspace= 11, monitor:HDMI-A-1, default:true

bindd = SUPER, code:10, Switch to workspace 1, workspace, 1
bindd = SUPER, code:11, Switch to workspace 2, workspace, 2
bindd = SUPER, code:12, Switch to workspace 3, workspace, 3
bindd = SUPER, code:13, Switch to workspace 4, workspace, 4
bindd = SUPER, code:14, Switch to workspace 5, workspace, 5
bindd = SUPER, code:15, Switch to workspace 6, workspace, 6
bindd = SUPER, code:16, Switch to workspace 7, workspace, 7
bindd = SUPER, code:17, Switch to workspace 8, workspace, 8
bindd = SUPER, code:18, Switch to workspace 9, workspace, 9
bindd = SUPER, code:19, Switch to workspace 10, workspace, 10
bindd = SUPER, code:20, Switch to workspace 11, workspace, 11
```
4. Waybar
```
    "persistent-workspaces": {
      "1": [],
      "2": [],
      "3": [],
      "4": [],
      "5": [],
      "6": [],
      "7": [],
      "8": [],
      "9": [],
      "10: []
    }
```
