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


<img width="386" height="363" alt="image" src="https://github.com/user-attachments/assets/2a1fac1e-e2d5-4812-a02b-a40052cef7b0" />


<img width="390" height="432" alt="image" src="https://github.com/user-attachments/assets/1d2ca3d5-a7ab-450b-86ed-7b53fd937d79" />

S'ha creat un fitxer de text amb la configuració necessària, especificant el domini web.victor.local i la plantilla WebServer-SAN.


<img width="526" height="471" alt="image" src="https://github.com/user-attachments/assets/b0b6d9e4-1bff-446a-8fd4-6be708ad719f" />


 S'executa certreq -new C:\web.inf C:\web.req per generar el fitxer de sol·licitud

 <img width="695" height="162" alt="image" src="https://github.com/user-attachments/assets/d8b81502-8a2e-4142-b266-0f7987db13bc" />
