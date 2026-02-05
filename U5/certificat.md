## Documentació de la Configuració del Servidor WEB Segur (HTTPS)

# Aquesta pràctica detalla el procés per configurar un servidor web local amb un certificat de seguretat personalitzat per al domini web.victor.local.
El primer pas és fer que el nom de domini apunti a la IP del servidor.
 - Propietats del Host (A) a la consola DNS.
   
 <img width="442" height="488" alt="image" src="https://github.com/user-attachments/assets/ec568150-08aa-4d72-b928-0a182fa1a8ab" />

Mitjançant la comanda nslookup web.victor.local es confirma que el servidor respon correctament a la IP assignada

<img width="565" height="164" alt="image" src="https://github.com/user-attachments/assets/f8419aed-6a00-4623-81f1-59c4e2bdcd3d" />


### Creació de la Plantilla de Certificat (WebServer-SAN)

Es duplica la plantilla "Servidor web" i se li posa el nom WebServer-SAN.


<img width="480" height="513" alt="image" src="https://github.com/user-attachments/assets/a583fa16-f32e-4133-8bcf-f35ecc0783d3" />
