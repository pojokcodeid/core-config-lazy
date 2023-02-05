# core-config-lazy
## Kebutuhan Dasar
### Linux (Fedora)
1. Acess Root
```bash
visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL
```
2. Install Node Js
- create directori download 
```
mkdir download
cd download
```
- install wget 
```
sudo dnf install wget
```
- Download noe JS dari halaman resminya 
```
wget https://nodejs.org/dist/v18.13.0/node-v18.13.0-linux-x64.tar.xz
```
- Install unzip dan xz
```bash
sudo dnf install unzip
sudo dnf install xz
sudo apt install xz-utils
```
- Extrak file downloadan 
```
tar -xf [nama file node js tadi di download]
```
- rename file extrac tadi 
```
mv [nama file extrak] [nama tujuan]
```
- copy folder ke home 
```bash
cp -r [nama folder] /home/asep/
```
- daftarkan env
```bash
sudo dnf install nano
cd ../
nano .bashrc
```
- masukan path 
```bash
export PATH=/home/asep/nodejs/bin:$PATH
ctrl + x
y
enter
```
3 Install git 
```
sudo dnf install git
```
4 Install Neovim
- download neovim
```bash
cd download
wget https://github.com/neovim/neovim/releases/download/v0.8.3/nvim-linux64.tar.gz
tar -xf nvim-linux64.tar.gz
mv nvim-linux64 nvim
cp -r nvim /home/asep/
```
- register path
```bash
cd ../
nano .bashrc
export PATH=/home/asep/nvim/bin:$PATH
```
5 Install GCC dan G++
```bash
sudo dnf install gcc
sudo dnf install g++
```
### Linux (Debian Base)
- Pastikan Akun Sudah Administrator

```bash
visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL
```

- Lakukan install Neovim

```bash
sudo apt-get install wget
mkdir download
cd download
wget https://github.com/neovim/neovim/releases/download/v0.8.3/nvim-linux64.deb
sudo apt-get install ./nvim-linux64.deb
nvim --version
```

- Check ketersediaan GCC

```bash
sudo apt-get install gcc
sudo apt-get install g++
gcc --version
```

- Install git

```bash
sudo apt-get install git
git --version
```

- Install NodeJS

```bash
sudo apt-get install curl
sudo apt install build-essential libssl-dev
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
source ~/.bashrc
nvm install 18.12.1
node --version
npm --version
```

- Install unzip, ripgrep

```bash
sudo apt-get install unzip
sudo apt-get install ripgrep
```

- Install Lazygit

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep '"tag_name":' |  sed -E 's/.*"v*([^"]+)".*/\1/')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
sudo tar xf lazygit.tar.gz -C /usr/local/bin lazygit
lazygit --version
```
### Arch Linux
```bash
sudo pacman -S git
sudo pacman -Sy nodejs
sudo pacman -S npm
sudo pacman -S unzip
sudo pacman -S neovim
```

```
git clone https://github.com/pojokcodeid/core-config-lazy.git ~/.config/nvim
```

## Panduam Windows 
## Kebutuhan Dasar

1. Install Neovim 8.0+ https://github.com/neovim/neovim/releases/tag/v0.8.3
2. C++ (windows) Compiler https://www.msys2.org/
3. GIT https://git-scm.com/download/win
4. NodeJs https://nodejs.org/en/
5. Ripgrep https://github.com/BurntSushi/ripgrep
6. Lazygit https://github.com/jesseduffield/lazygit
7. Nerd Font https://github.com/ryanoasis/nerd-fonts
8. Windows Terminal (Windows) https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=en-id&gl=id
9. Powershell (windows) https://apps.microsoft.com/store/detail/powershell/9MZ1SNWT0N5D?hl=en-id&gl=id

```
git clone https://github.com/pojokcodeid/core-config-lazy.git "$env:LOCALAPPDATA\nvim"
```