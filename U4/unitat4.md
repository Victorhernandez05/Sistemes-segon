
Víctor Hernández Elías

### 1. Configuració de les Interfícies de Xarxa

El servidor es configura amb dos adaptadors de xarxa per separar el tràfic de la xarxa interna de la simulació de xarxa externa:

<img width="749" height="364" alt="image" src="https://github.com/user-attachments/assets/82a0c122-0b57-48b8-ac8e-11d726de4b45" />

Adaptador de Xarxa Interna:
Adreça IP: 192.168.2.101.
Màscara de subxarxa: 255.255.255.0.
DNS preferit: 127.0.0.1 (un cop instal·lat l'AD).



<img width="396" height="451" alt="image" src="https://github.com/user-attachments/assets/7efe4133-dbed-4719-a6f2-c32c7879743b" />



Adaptador de Xarxa Externa:
Adreça IP: 10.10.1.1.
Màscara de subxarxa: 255.255.255.0.

<img width="396" height="450" alt="image" src="https://github.com/user-attachments/assets/16d52d45-b3df-4588-a01d-e7f9c0777eed" />


### 2. Implementació d'Active Directory (AD DS)

Es promou el servidor com a controlador de domini principal per gestionar el bosc i els usuaris:
Instal·lació del Rol: Es selecciona "Servicios de dominio de Active Directory" des de l'Administrador del Servidor.
Configuració del Domini:
Operació: Agregar un nou bosc.
Nom del domini arrel: Víctor.local.
Capacitats del Controlador:
S'activen les funcions de Catàleg global (GC) i Servidor DNS.
S'estableix el nivell funcional del bosc i domini a Windows Server 2016


<img width="571" height="352" alt="image" src="https://github.com/user-attachments/assets/ddbe5ce0-4a4c-401f-b985-826b75547f77" />

<img width="600" height="477" alt="image" src="https://github.com/user-attachments/assets/ca75b81b-7f3a-4cb3-ab46-ce2e88b11be3" />

<img width="664" height="541" alt="image" src="https://github.com/user-attachments/assets/14cd3fe5-b126-49f2-83b0-ede55abc87a9" />


<img width="663" height="531" alt="image" src="https://github.com/user-attachments/assets/a3585068-dd16-45ea-9544-684daf5cf9b9" />



<img width="655" height="484" alt="image" src="https://github.com/user-attachments/assets/60e79305-8a24-42f7-a652-2d2ff16beb5e" />


<img width="655" height="487" alt="image" src="https://github.com/user-attachments/assets/f3ccc9bb-97bc-4149-940d-c6bbc93bdd5e" />















### 3. Integració i Gestió de Clients

Per validar el domini, s'integra una estació de treball Windows 10:
Configuració IP del Client: S'assigna la IP 192.168.2.102 i es defineix com a DNS l'IP del servidor 192.168.2.101.
Unió al Domini: Es realitza la unió des de les propietats del sistema, rebent la confirmació: "Se unió correctamente al dominio Victor.local".
Creació d'Usuaris: Es crea l'usuari Prueba1 dins del contenidor "Users" de l'Active Directory per permetre l'accés des dels clients.


<img width="660" height="487" alt="image" src="https://github.com/user-attachments/assets/61abc001-4300-4ced-91dd-9cb9523e67d7" />





<img width="658" height="499" alt="image" src="https://github.com/user-attachments/assets/86f07fd2-b514-459b-af6c-8468eccdd935" />




















### 4. Recursos Compartits i Seguretat de Fitxers

Es configura una carpeta compartida per a l'intercanvi de dades:
Recurs compartit: Carpeta anomenada "Dades".
Permisos de Recurs: S'atorga "Control total" a l'usuari Prueba1.
Permisos NTFS (Seguretat): Es configuren els permisos a la pestanya de Seguretat per permetre la modificació i lectura de fitxers al mateix usuari.


<img width="530" height="443" alt="image" src="https://github.com/user-attachments/assets/0dc4e720-b9b8-4eee-a58c-79319d90d258" />

<img width="354" height="440" alt="image" src="https://github.com/user-attachments/assets/fa029760-9661-4db3-a99a-ca54ede75421" />















### 5. Servei d'Accés Remot (VPN) i Enrutament

Es configura el rol d'Accés Remot per permetre connexions segures des de la xarxa externa:
Instal·lació de Serveis: Es seleccionen els serveis de rol DirectAccess y VPN (RAS) i Enrutamiento.
Configuració RRAS:
S'habilita l'Accés a VPN i l'Enrutament LAN.
Assignació d'IPs: Es defineix un interval d'adreces estàtiques per als clients VPN des de 172.16.0.0 fins a 172.16.0.10.
Permisos de Marcado: Es concedeix el permís "Permitir acceso" a l'usuari Prueba1 a la pestanya de Marcado (Dial-in).



<img width="669" height="475" alt="image" src="https://github.com/user-attachments/assets/60fd0612-de7b-45f2-989e-c76ff1f8b494" />





<img width="665" height="479" alt="image" src="https://github.com/user-attachments/assets/f7a3d903-d5df-4294-ab03-5bf1f3eb2c7a" />





<img width="663" height="604" alt="image" src="https://github.com/user-attachments/assets/e568aa12-3a2e-45e9-8a08-8b2cb5445b43" />





<img width="656" height="446" alt="image" src="https://github.com/user-attachments/assets/53a030ed-192d-4c12-bbf1-71e565af20b6" />




<img width="487" height="596" alt="image" src="https://github.com/user-attachments/assets/1773c8a8-b225-49fe-8358-0f9e7ef856fc" />








### 6. Verificació de Resultats

Connexió VPN: El client estableix amb èxit la connexió "VPN VICTOR", mostrant l'estat "Conectado".
Mapeig de Xarxa: El recurs compartit queda connectat al client com la Unitat Z: (\\192.168.2.101\Dades), permetent la creació de fitxers de forma remota.




<img width="656" height="445" alt="image" src="https://github.com/user-attachments/assets/88988ef7-7f0f-4a66-80f0-fbbb7906c0da" />


<img width="630" height="494" alt="image" src="https://github.com/user-attachments/assets/d989730a-9239-4444-bc33-9031b66385d7" />


