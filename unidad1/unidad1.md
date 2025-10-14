---
layout: default
title: "Target, servei i script"
---

## Resum de la idea

Target (miscripts.target): punt de sincronització. Agrupa unitats (serveis) per controlar-les conjuntament.

Servei (reporte_sistema.service): executa l’script que genera l’informe i l’envia per correu.

Script (/usr/local/bin/reporte_sistema.sh): recull informació del sistema i la envia amb mail (prové de mailutils).


2) Crear el target (fitxer .target)

Editor: sudo nano /etc/systemd/system/miscripts.target

## Exemple de target

![Captura del target](/Captura%20de%20pantalla%20de%202025-10-14%2009-45-55.png)

Contingut d'exemple:

- [Material teórico (PDF)](https://github.com/mireiaconsarnau/machine_learning/raw/main/unidad1/l1.pdf)
- [Vídeo de recapitulación de conceptos clave (YOUTUBE)](https://youtu.be/p27AhdHxi_o)

