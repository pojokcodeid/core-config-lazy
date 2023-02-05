# core-config-lazy
## Kebutuhan Dasar
### Linux (Fedora)
1. Acess Root
```
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
```
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
```
cp -r [nama folder] /home/asep/
```
- daftarkan env
```
sudo dnf install nano
cd ../
nano .bashrc
```
- masukan path 
```
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
```
cd download
wget https://github.com/neovim/neovim/releases/download/v0.8.3/nvim-linux64.tar.gz
tar -xf nvim-linux64.tar.gz
mv nvim-linux64 nvim
cp -r nvim /home/asep/
```
- register path
```
cd ../
nano .bashrc
export PATH=/home/asep/nvim/bin:$PATH
```
5 Install GCC dan G++
```
sudo dnf install gcc
sudo dnf install g++
```
### Linux (Debian Base)
- Pastikan Akun Sudah Administrator

```
visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL
```

- Lakukan install Neovim

```
sudo apt-get install wget
mkdir download
cd download
wget https://github.com/neovim/neovim/releases/download/v0.8.3/nvim-linux64.deb
sudo apt-get install ./nvim-linux64.deb
nvim --version
```

- Check ketersediaan GCC

```
gcc --version
```

- Install git

```
sudo apt-get install git
git --version
```

- Install NodeJS

```
sudo apt-get install curl
sudo apt install build-essential libssl-dev
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
source ~/.bashrc
nvm install 18.12.1
node --version
npm --version
```

- Install unzip, ripgrep

```
sudo apt-get install unzip
sudo apt-get install ripgrep
```

- Install Lazygit

```
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep '"tag_name":' |  sed -E 's/.*"v*([^"]+)".*/\1/')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
sudo tar xf lazygit.tar.gz -C /usr/local/bin lazygit
lazygit --version
```


```
git clone https://github.com/pojokcodeid/core-config-lazy.git ~/.config/nvim
```
