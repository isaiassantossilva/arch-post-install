# Pós-Instalação

Comandos
![Comandos](img/commands.png)


### Atualizar o repositório e o sistema
```
sudo pacman -Syu
```

### Instalar algumas ferramentas
```
sudo pacman -S nano git curl wget zip unzip
```

### Instalar algumas fontes
```
sudo pacman -S noto-fonts-cjk
```

### Instalar firewall (opcional)
```
sudo pacman -S gufw
```

### Instalar gestor de firmware (opcional)
```
sudo pacman -S fwupd
```

### Habilitar leitura para dispositivos NTFS da microsoft
```
sudo pacman -S ntfs-3g
```

### Habilitar serviço de bluetooth
```
sudo systemctl start bluetooth.service --now
```
ou
```
sudo systemctl start bluetooth
sudo systemctl enable bluetooth
```

### Otimizar a vida da bateria do notebook
```
sudo pacman -S tlp
sudo systemctl enable tlp
sudo systemctl mask systemd-rfkill.service systemd-rfkill.socket
```

### Habilitar para mostrar apps do repositório padrão na loja de apps
kde
```
sudo pacman -S packagekit-qt6
```

gnome
```
sudo pacman -S gnome-software-packagekit-plugin
```

### Instalar helper do AUR
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# yay -Y --gendb
```

### Instalar google chrome
```
yay -S google-chrome
```

### Instalar vscode
```
yay -S visual-studio-code-bin
```

### Instalar vizualizador de imagem
```
flatpak install flathub org.kde.gwenview
```

### Instalar reprodutor de vídeo
```
flatpak install flathub io.mpv.Mpv
```