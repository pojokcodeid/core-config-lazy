# core-config-lazy
## Kebutuhan Dasar
### LInux (Fedora)
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
masukan path 
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
wget https://github.com/neovim/neovim/releases/download/v0.8.2/nvim-linux64.tar.gz
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
# Clone config Neovim
```
git clone https://github.com/pojokcodeid/nvim-lazy.git ~/.config/nvim
```



lik panduan <br>
https://github.com/pojokcodeid/theme-linux/blob/main/fedora/config-neovim.md
### Linux Debian
https://github.com/pojokcodeid/nvim-lazy#readme
### Clone Basic Config
```
git clone https://github.com/pojokcodeid/core-config-lazy.git ~/.config/nvim
```
