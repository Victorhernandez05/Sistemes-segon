### Víctor Hernández Elías
# Administració de sistemes operatius | Documentació Kernel
## Preparatius i requisits previs
Assegura’t que tens prou espai en disc i que tens les eines bàsiques instal·lades.

sudo apt update

sudo apt install -y build-essential libncurses-dev flex bison openssl libssl-dev dkms libelf-dev libudev-dev libpci-dev libiberty-dev autoconf dwarves

<img width="1052" height="312" alt="image" src="https://github.com/user-attachments/assets/31643c2a-aadd-47ea-8334-535cf94ddc67" />


### 1. Situa’ns a la carpeta de descàrregues
cd ~/Descàrregues
pwd
<img width="442" height="90" alt="image" src="https://github.com/user-attachments/assets/94dd294c-c21d-445c-a717-2da9db1db00e" />

### 2. Descarregar el kernel (exemple: 6.14.1)

<img width="728" height="598" alt="image" src="https://github.com/user-attachments/assets/4668a03d-d7f1-4f97-b763-02d14d259e6d" />

### 3. Descomprimir l’arxiu del kernel
tar -xf linux-6.14.1.tar.xz

<img width="760" height="23" alt="image" src="https://github.com/user-attachments/assets/249027c9-6ea9-4206-bae5-17aeea0892fc" />

crea la carpeta linux-6.14.1
ls -l

<img width="717" height="368" alt="image" src="https://github.com/user-attachments/assets/1e953111-55ee-4ea3-ba0f-a41eef123628" />

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

<img width="725" height="282" alt="image" src="https://github.com/user-attachments/assets/456e328a-bb1d-4d9d-bb4f-cb53a9ca4181" />

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



