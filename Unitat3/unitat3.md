### Víctor Hernández Elías
# Administració de sistemes operatius | Documentació Kernel
## Preparatius i requisits previs
Assegura’t que tens prou espai en disc i que tens les eines bàsiques instal·lades.

sudo apt update

sudo apt install -y build-essential libncurses-dev flex bison openssl libssl-dev dkms libelf-dev libudev-dev libpci-dev libiberty-dev autoconf dwarves

<img width="1052" height="312" alt="image" src="https://github.com/user-attachments/assets/31643c2a-aadd-47ea-8334-535cf94ddc67" />


### 1. Situa’ns a la carpeta de descàrregues
cd ~/Descàrregues

pwd  # comprova que ets a la carpeta correcta

### 2. Descarregar el kernel (exemple: 6.14.1)

### 3. Descomprimir l’arxiu del kernel

tar -xf linux-6.14.1.tar.xz
crea la carpeta linux-6.14.1
ls -l

### 4. Entrar dins la carpeta del kernel

cd linux-6.14.1
pwd  # comprova que estàs a linux-6.14.1


### 5. Fer còpia de main.c
cp -v kernel/main.c kernel/main.c.orig   # exemple: si el fitxer està a kernel/main.c

ls -l kernel/main.c kernel/main.c.orig


### 6. Modificar el kernel (canvis desitjats)

<img width="1050" height="186" alt="image" src="https://github.com/user-attachments/assets/7d7d6ef8-8d9b-4bec-bac4-9fdb3381a4f7" />

### 7. Crear el patch, aplicar i comprovar-lo.

<img width="1002" height="197" alt="image" src="https://github.com/user-attachments/assets/9a6bb9d2-bc91-466c-abf5-815095c9e4f0" />

### 8. Comentar els TIMEOUT de /etc/default/grub

<img width="1046" height="527" alt="image" src="https://github.com/user-attachments/assets/09e36542-eec3-4ed6-831d-b0a3d535c719" />


### 9. Actualitzar GRUB perquè apliqui els canvis
sudo update-grub

### 10. Fer menuconfig i desactivar virtualització

<img width="851" height="693" alt="image" src="https://github.com/user-attachments/assets/9b5f2f09-56b9-4ccd-871f-6108e6724c64" />

<img width="813" height="411" alt="image" src="https://github.com/user-attachments/assets/77a63d8b-1c54-497c-951d-adb0089e06fb" />


### 11. Guardar en .config i comprovar que existeix

ls -l .config
o ls -la .config

### 12. Netjar compilacions anteriors i preparar dependencies

make clean

make prepare

### 13. Inciar la compilació

sudo make-kpkg --initrd kernel_image kernel_headers



