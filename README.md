# Pós-Instalação

### Comandos
![Comandos](img/commands.png)

### Atualizar o repositório e o sistema
```
sudo pacman -Syu
```

### Instalar algumas ferramentas
```
sudo pacman -S nano git curl wget zip unzip ntfs-3g
```

### Instalar algumas fontes
```
sudo pacman -S noto-fonts ttf-jetbrains-mono-nerd
```

### Instalar zsh
```
sudo pacman -S zsh
chsh -s $(which zsh)
reboot
```

Binds de algumas teclas
```
echo >> ~/.zshrc
echo '# Bind keys' >> ~/.zshrc
echo 'bindkey "^[[H" beginning-of-line' >> ~/.zshrc
echo 'bindkey "^[[F" end-of-line' >> ~/.zshrc
echo 'bindkey "^[[3~" delete-char' >> ~/.zshrc
echo 'bindkey "^H" backward-kill-word' >> ~/.zshrc
echo 'bindkey "^[[3;5~" kill-word' >> ~/.zshrc
echo 'bindkey "^[[1;5D" backward-word' >> ~/.zshrc
echo 'bindkey "^[[1;5C" forward-word' >> ~/.zshrc
```

Instalar plugins
```
sudo pacman -S zsh-autosuggestions zsh-syntax-highlighting
echo >> ~/.zshrc
echo '# Plugins' >> ~/.zshrc
echo 'source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc
echo 'source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc
```

Instalar buscador de linha de comando
```
sudo pacman -S fzf
echo >> ~/.zshrc
echo '# Fzf' >> ~/.zshrc
echo 'source <(fzf --zsh)' >> ~/.zshrc
```

Instalar Starship Prompt
```
sudo pacman -S starship
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
starship preset nerd-font-symbols -o ~/.config/starship.toml
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

### Habilitar flatpak
```
sudo pacman -S flatpak
```

### Habilitar helper do AUR (yay)
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

cd ..
rm -rf yay
```

### Habilitar snap
```
git clone https://aur.archlinux.org/snapd.git
cd snapd
makepkg -si

sudo systemctl enable --now snapd.socket
sudo systemctl enable --now snapd.apparmor.service

sudo ln -s /var/lib/snapd/snap /snap

cd ..
rm -rf snapd
```

### Mostrar apps do repositório padrão na loja de apps
kde
```
sudo pacman -S packagekit-qt6
```
gnome
```
sudo pacman -S gnome-software-packagekit-plugin
```

### Instalar gerenciador de flatpaks
```
flatpak install flathub io.github.flattool.Warehouse
```

### Instalar gerenciador de permissões para flatpaks
```
flatpak install flathub com.github.tchx84.Flatseal
```

### Instalar Flatsweep (Gerenciador de arquivos residuais para flatpak)
```
flatpak install flathub io.github.giantpinkrobots.flatsweep
```

### Instalar vizualizador de imagem
kde
```
flatpak install flathub org.kde.gwenview
```
gnome
```
flatpak install flathub org.gnome.eog
```

### Instalar reprodutor de vídeo
```
flatpak install flathub io.mpv.Mpv
```

### Instalar firewall
```
sudo pacman -S gufw
```

### Instalar gestor de firmware
```
sudo pacman -S fwupd
```

### Instalar google chrome
```
yay -S google-chrome
```

### Instalar vscode
```
yay -S visual-studio-code-bin
```

### Instalar docker e docker compose
```
sudo pacman -S docker docker-compose
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER
```

### Instalar Podman Desktop
```
flatpak install flathub io.podman_desktop.PodmanDesktop
```

### Instalar distrobox
```
sudo pacman -S distrobox
```

### Instalar gerenciador de versões universal
```
yay -S asdf-vm
```

### Instalar gnome boxes
```
sudo pacman -S gnome-boxes
```

### Instalar qBittorrent
```
flatpak install flathub org.qbittorrent.qBittorrent
```

### Instalar bottles
```
flatpak install flathub com.usebottles.bottles
```

### Instalar gradia (Editor de imagens)
```
flatpak install flathub be.alexandervanhee.gradia
```

### Instalar onlyoffice
```
flatpak install flathub org.onlyoffice.desktopeditors
```

### Instalar gear lever (Utilitário para AppImage)
```
flatpak install flathub it.mijorus.gearlever
```

### Instalar Dev Toolbox (Utilitário para desenvolvimento)
```
flatpak install flathub me.iepure.devtoolbox
```

### Instalar Free Download Manager
```
flatpak install flathub org.freedownloadmanager.Manager
```

### Instalar LocalSend (Utilitário para compartilhar arquivos na mesma rede)
```
flatpak install flathub org.localsend.localsend_app
```

### Instalar Flameshot (Utilitário screenshots)
```
flatpak install flathub org.flameshot.Flameshot
```

### Instalar CPU-X
```
flatpak install flathub io.github.thetumultuousunicornofdarkness.cpu-x
```

### Instalar GPU-Viewer
```
flatpak install flathub io.github.arunsivaramanneo.GPUViewer
```

### Instalar PortProton (Utilitário para rodar alguns apps de Windows)
```
flatpak install flathub ru.linux_gaming.PortProton
```

### Instalar Obsidian
```
flatpak install flathub md.obsidian.Obsidian
```

### Instalar Embellish (Utilitário para baixar fontes)
```
flatpak install flathub io.github.getnf.embellish
```

### Instalar Master PDF Editor (AppImage)
```
https://code-industry.net/public/Master_PDF_Editor_5.9.94-x86_64.AppImage
```

### Instalar Muon (Snap)
```
sudo snap install muon-ssh --classic
```
