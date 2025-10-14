---
layout: default
title: "Target, servei i script"
---

## Resum de la idea

Target (miscripts.target): punt de sincronització. Agrupa unitats (serveis) per controlar-les conjuntament.

Servei (reporte_sistema.service): executa l’script que genera l’informe i l’envia per correu.

Script (/usr/local/bin/reporte_sistema.sh): recull informació del sistema i la envia amb mail (prové de mailutils).


### Crear el target (fitxer .target)

**sudo nano /etc/systemd/system/miscripts.target**

![imagen](<target.png>)

Contingut d'exemple:

### Crear el servei (fitxer .service)

**sudo nano /etc/systemd/system/reporte_sistema.service**

Contingut d'exemple pensat per executar l’script una vegada a l'arrencada:

![imagen](<servei.png>)

### Crear l’script que genera i envia l’informe

**sudo nano /usr/local/bin/reporte_sistema.sh**

![imagen](<script.png>)


Contingut d’exemple (personalitza el correu receptor):

![imagen](<correo.png>)

### Instal·lar dependències de correu

A Debian/Ubuntu (i derivats) l’opció senzilla:

![imagen](<get-default.png>)


- [Material teórico (PDF)](https://github.com/mireiaconsarnau/machine_learning/raw/main/unidad1/l1.pdf)
- [Vídeo de recapitulación de conceptos clave (YOUTUBE)](https://youtu.be/p27AhdHxi_o)

