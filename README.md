# Pós-Instalação

Comandos
![Comandos](img/commands.png)


Atualizar o repositório e o sistema
```
sudo pacman -Syu
```

Instalar algumas ferramentas
```
sudo pacman -S nano git curl wget
```

Instalar firewall
```
sudo pacman -S gufw
```

Instalar gestor de firmewere
```
sudo pacman -S fwupd
```

Habilitar leitura para dispositivos NTFS da micrisoft
```
sudo pacman -S ntfs-3g
```

Habilitar serviço de bluetooth
```
sudo systemctl start bluetooth.service --now
```

Habilitar para mostrar apps do repositório padrão na loja de apps

kde
```
sudo pacman -S gnome-software-packagekit-plugin
```

gnome
```
sudo pacman -S packagekit-qt5
```

Instalar helper do AUR
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

yay -Y --gendb

yay -S google-chrome
```