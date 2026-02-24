
## 1. Instal·lació de l'entorn LAMP
Primer de tot, actualitzem els repositoris i instal·lem el servidor web.

<img width="927" height="203" alt="image" src="https://github.com/user-attachments/assets/783f6d84-55fd-4303-ae99-1aeac009fb55" />

<img width="1017" height="25" alt="image" src="https://github.com/user-attachments/assets/44ccc8fd-fc08-4b91-8817-1d5cd6f5f1a7" />
<img width="1412" height="324" alt="image" src="https://github.com/user-attachments/assets/9ed2bc9e-c00f-4290-a708-f065112621d3" />


## 2. Creació del fitxer index.php

Anem al directori arrel per defecte d'Apache.

<img width="461" height="83" alt="image" src="https://github.com/user-attachments/assets/a27d64ab-f0f9-4cb5-9f48-6f68ca8c06ef" />

Esborrem tota la configuració del fitxer i afegim "Hello World".

<img width="968" height="90" alt="image" src="https://github.com/user-attachments/assets/397b0b7b-17ce-4c1f-a3bd-0b8ab332f128" />

## 3. Generació i instal·lació del Certificat SSL

Com que el certificat no està signat per una entitat certificadora oficial (CA), el navegador dirà que la connexió no és segura.


Generar el certificat i la clau

<img width="1514" height="528" alt="image" src="https://github.com/user-attachments/assets/ecceb167-db44-443f-9eae-681c17c14a7a" />


<img width="1062" height="389" alt="image" src="https://github.com/user-attachments/assets/13260234-732a-471a-b27a-b4405f765ed8" />

## Habilitar el mòdul SSL i el lloc per defecte:
<img width="1057" height="328" alt="image" src="https://github.com/user-attachments/assets/a5350b4c-bac3-4b2f-9fad-46edfeec75dd" />


#### Un cop fets els anteriors pasos anem a la pagina amb la nostra IP.
<img width="1385" height="767" alt="image" src="https://github.com/user-attachments/assets/5e575452-0878-4497-92c6-bed3d9e7c6f5" />

Aquesta és la prova que el servidor Apache està funcionant sota HTTPS, però amb l'advertència esperada.
El fet que aparegui el botó "Accepto el risc i vull continuar" confirma que la configuració d'Apache és correcta.

<img width="637" height="209" alt="image" src="https://github.com/user-attachments/assets/8ba3a74a-464c-4d8b-91ca-f1aeedf00b07" />

