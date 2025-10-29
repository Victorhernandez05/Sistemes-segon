Víctor Hernández Elías

**Serveis Windows**


**Objectiu general**

Crear un script PowerShell que:

- S’executi automàticament com a servei
- Registre la data i hora d’inici
- Identifiqui l’usuari i l’ordinador
- Detecti la IP local i el temps d’activitat (uptime)
- Comprovi si hi ha connexió a Internet
- Escrigui tota la informació en un fitxer de log


1. Instal·lació de NSSM (Non-Sucking Service Manager)

<img width="786" height="404" alt="image" src="https://github.com/user-attachments/assets/baff084b-159f-4a09-8d9d-837142bd7eeb" />

Anem al link de descarga seleccionem l’opció marcada: https://nssm.cc/download






- Extreu el contingut i col·locar-lo en una carpeta accessible 
- Obrir PowerShell com a administrador
- Executar nssm install per crear un nou servei

<img width="751" height="459" alt="image" src="https://github.com/user-attachments/assets/b9fc5deb-d7cb-47cb-8e8f-03dd053c6cea" />

<img width="754" height="462" alt="image" src="https://github.com/user-attachments/assets/010ab853-007b-44cf-b7b2-e77ad32233aa" />


2. Configuració del servei amb NSSM

Obrim el “services.msc” i busquem el server.

<img width="751" height="362" alt="image" src="https://github.com/user-attachments/assets/4a77a8a1-f5b5-4725-951e-2a425e0a1d6b" />


Llavors anem a “propiedades>Tipo de inicio: Automático”.

<img width="751" height="505" alt="image" src="https://github.com/user-attachments/assets/e9b3446f-385f-48ff-b12d-2ae1d230a2f5" />




3. Creació del script log_inici.ps1

<img width="868" height="323" alt="image" src="https://github.com/user-attachments/assets/4adb7535-e5ec-4df6-a1b4-f6e33b352e51" />

Executem el powershell com administració.

<img width="747" height="143" alt="image" src="https://github.com/user-attachments/assets/8bc6bf4d-0a12-4edb-9bbb-ef436a3f08f2" />


Llavors un cop dins executem el script.

<img width="855" height="64" alt="image" src="https://github.com/user-attachments/assets/173aa8ec-8bdd-4016-91c3-7bab2f2c53f0" />


I mostra el log en el fitxer txt.

<img width="866" height="212" alt="image" src="https://github.com/user-attachments/assets/ef5ae21c-89bb-4552-916d-0e4475074996" />
