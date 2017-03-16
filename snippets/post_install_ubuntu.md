Post instalación Ubuntu
=======================

## Upgrade

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo apt-get install linux-headers-`uname -r`
```

# Compilations

```
sudo apt-get install build-essential
sudo apt-get install automake make cmake libtool autoconf
```

## Commons

```
sudo apt-get install vim terminator rar unrar zip unzip skype cheese curl ssh
sudo apt-get install ttf-mscorefonts-installer
sudo fc-cache
```

Configurar editor por defecto

```
sudo update-alternatives --config editor
```

## Gimp

```
sudo apt-get install gimp gimp-data gimp-plugin-registry gimp-data-extras
```

## Gnome3

```
sudo add-apt-repository -y ppa:gnome3-team/gnome3
sudo apt-get install gnome-shell gnome-tweak-tool gnome-shell-extensions
```

## Google Chrome

```
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable
```

## Java

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
sudo update-java-alternatives -s java-8-oracle
```

## Git

```
sudo apt-get install git-core
git config --global user.name "My name"
git config --global user.email "myemail@mail.com"
git config --global color.ui true
git config --global credential.helper cache
```

[Generar ssh para github & gitlab.](https://help.github.com/articles/connecting-to-github-with-ssh/) Luego de agregar las keys comprobar:

```
ssh -T git@github.com
```

## Optimizations

```
sudo apt-get remove unity-lens-music
sudo apt-get autoremove unity-scope-musicstores
sudo mv /usr/bin/bluetooth-applet /usr/bin/bluetooth-applet-old
sudo apt-get remove deja-dup
sudo apt-get autoremove gnome-online-accounts
sudo apt-get install preload
```

## Clean up

```
sudo apt-get -f install
sudo apt-get autoremove
sudo apt-get -y autoclean
sudo apt-get -y clean
```
