


## Setup Enviroment for Windows
- Install Make: https://gnuwin32.sourceforge.net/packages/make.htm
- Add path:
- Check: make -v
### Hoặc:
- install ubuntu wsl, user/pass: u/1
- cp -r /mnt/c/Users/savaobay/Desktop/firmware /home/u

- sudo apt update && sudo apt upgrade
- sudo apt install build-essential
- cd firmware
- sudo make deps

- nano ~/.profile
- add to end of file and save (Ctrl+S)

- BR2_DL_DIR="${HOME}/buildroot_dl"
- [ ! -d "$BR2_DL_DIR" ] && mkdir -p $BR2_DL_DIR
- export BR2_DL_DIR

- source ~/.profile

- nano ~/.bashrc
- add to end of file and save
- export PATH=$(echo "$PATH" | tr ':' '\n' | grep -v ' ' | paste -sd:)
- source ~/.bashrc


 
## build
Open cmd by Admin
cd to Master Folder:
Run:

- build default: `make BOARD=ssc337de_ultimate`	=> Build all
- build app: `make BOARD=ssc337de_ultimate br-serial` => Build App
- binary path: home\u\firmware\output\build\serial\src

## flash
- build default: `make BOARD=ssc337de_ultimate`	=> Make all


## SCP Tool
- https://sourceforge.net/projects/winscp/files/WinSCP/6.5.1/WinSCP-6.5.1.msi/download
- 
