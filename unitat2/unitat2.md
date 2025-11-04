Víctor Hernández Elías

**Serveis Windows**


**Objectiu general**

 Script PowerShell que:

- S’executi automàticament com a servei
- Registre la data i hora d’inici
- Identifiqui l’usuari i l’ordinador
- Detecti la IP local i el temps d’activitat (uptime)
- Comprovi si hi ha connexió a Internet
- Escrigui tota la informació en un fitxer de log


1. Instal·lació de NSSM (Non-Sucking Service Manager)

<img width="754" height="463" alt="image" src="https://github.com/user-attachments/assets/0a51f0be-1c85-4dae-8cd2-f28f59600408" />


Al moodle ves a l’opció marcada i descarga.






- Extreu el contingut i col·loca-lo en una carpeta accessible 
- Obrir PowerShell com a administrador
- Executar nssm install per crear un nou servei

<img width="743" height="313" alt="image" src="https://github.com/user-attachments/assets/9ed746da-f7d1-4a14-8318-d44204078f87" />



2. Configuració del servei amb NSSM

Obrim el “services.msc” i busquem el server.

<img width="760" height="523" alt="image" src="https://github.com/user-attachments/assets/bcb66910-2059-43e1-b5cb-13141c61bb45" />



Llavors anem a “propiedades>Tipo de inicio: Automático”.

<img width="751" height="505" alt="image" src="https://github.com/user-attachments/assets/e9b3446f-385f-48ff-b12d-2ae1d230a2f5" />




3. Creació del script log_inici.ps1

<img width="1004" height="664" alt="image" src="https://github.com/user-attachments/assets/095b76f7-6fd7-48db-a1c6-ce9dba02e539" />


<img width="782" height="664" alt="image" src="https://github.com/user-attachments/assets/6304c76f-41d3-428b-9bc5-9bb8467864a8" />


I aquest es el log en el fitxer txt.

<img width="715" height="692" alt="image" src="https://github.com/user-attachments/assets/aeb429a7-d854-4ba0-acfe-a9a71b52c3b2" />çç



