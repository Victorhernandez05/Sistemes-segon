Víctor Hernández Elías 
---
title: "Target, servei i script"
---
Víctor Hernández Elías 

## Resum de la idea

Target (miscripts.target): punt de sincronització. Agrupa unitats (serveis) per controlar-les conjuntament.

Servei (reporte_sistema.service): executa l’script que genera l’informe i l’envia per correu.

Script (/usr/local/bin/reporte_sistema.sh): recull informació del sistema i la envia amb mail (prové de mailutils).


### Crear el target (fitxer .target)

Un target a systemd és un punt de sincronització, semblant a un "grup" d’unitats. Serveix per agrupar serveis i controlar-los conjuntament.

**sudo nano /etc/systemd/system/miscripts.target**

![imagen](<target.png>)

[Unit] → Conté metadades com el nom i la descripció.

[Install] → Indica a quin altre target s’enganxa. 

En aquest cas, a multi-user.target (nivell multiusuari, habitual en servidors).

### Crear el servei (fitxer .service)

Un servei defineix quan s’executa un programa o script sota systemd.

**sudo nano /etc/systemd/system/reporte_sistema.service**

![imagen](<servei.png>)

**Recargar, habilitar i executar:** 

sudo systemctl daemon-reload

sudo systemctl enable reporte_sistema.service

sudo systemctl start reporte_sistema.service

### Crear l’script que genera i envia l’informe

Aquest script /usr/local/bin/reporte_sistema.sh està dissenyat per generar un informe de l'estat del sistema automàticament a l'inici i enviar-lo per correu a un administrador (en aquest cas victorhernandez@iesebre.com).

**sudo nano /usr/local/bin/reporte_sistema.sh**

![imagen](<script.png>)

Permisos: **sudo chmod +x /usr/local/bin/reporte_sistema.sh**

### Instal·lar dependències de correu

**sudo apt install mailutils -y**

![imagen](<correo.png>)

I com podem veure a la imatge ens envia el report general del sistema al engegar la màquina o reiniciar-la

### Com obtenir / canviar el default target

**systemctl get-default**

![imagen](<get-default.png>)

Establir un target per defecte (si vols arrencar directament a miscripts.target com a target per defecte; normalment es fa que miscripts.target sigui WantedBy=multi-user.target i s’executi a l'arrencada):

- [Material teórico (PDF)](https://github.com/mireiaconsarnau/machine_learning/raw/main/unidad1/l1.pdf)
- [Vídeo de recapitulación de conceptos clave (YOUTUBE)](https://youtu.be/p27AhdHxi_o)

