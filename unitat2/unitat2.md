Víctor Hernández Elías

**Serveis Windows**


**Objectiu general**

Aquest script PowerShell està dissenyat per:

Executar-se automàticament com a servei, en iniciar l’equip o reiniciar-lo.

- Registrar la data i hora d’execució per tenir una traçabilitat temporal de cada informe generat.

- Identificar l’usuari actiu i el nom de l’ordinador on s’executa el script.

- Detectar la IP local assignada a la màquina i calcular el temps d’activitat (uptime) des de l’últim reinici.

- Comprovar l’estat de la connexió a Internet mitjançant una prova de connexió (Google DNS).

Recollir informació tècnica del sistema:

- Sistema operatiu 

- Quantitat de memòria RAM instal·lada

- Espai lliure i total dels discos locals

- Processos més actius per ús de CPU i memòria

- Serveis actualment en execució

1. Instal·lació de NSSM (Non-Sucking Service Manager)

<img width="754" height="463" alt="image" src="https://github.com/user-attachments/assets/0a51f0be-1c85-4dae-8cd2-f28f59600408" />


Al moodle ves a l’opció marcada i descarga-la.






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

<img width="715" height="692" alt="image" src="https://github.com/user-attachments/assets/aeb429a7-d854-4ba0-acfe-a9a71b52c3b2" />

<img width="716" height="178" alt="image" src="https://github.com/user-attachments/assets/fcba54c6-e80f-4e4a-a566-9a26af9ed92e" />




