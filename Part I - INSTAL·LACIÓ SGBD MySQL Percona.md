# 1. Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata.
      
## Primer canvien les polítiques de contrasenya del mysql amb les següents comandes:
    SET GLOBAL validate_password.policy=LOW;
    SET GLOBAL validate_password.length=6;

## Amb la comanda mysql_secure_installation canviem la contrasenya del root i ens securitza el mysql:
 ![image](https://user-images.githubusercontent.com/61474562/154500390-175c5daf-aef7-41b6-af08-5682138afce3.png)
 ![image](https://user-images.githubusercontent.com/61474562/154500504-3726ef96-e382-4220-80c1-67ba2d96f012.png)

# 2. Quines són les instruccions per arrancar / verificar status / apagar servei de la base de dades de Percona Server en el CentOS 7:
    Arrancar: systemctl start mysql.service
    Verificar status: systemctl status mysql.service
    Apagar servei: systemctl stop mysql.service

# 3.	A on es troba i quin nom rep el fitxer de configuració del SGBD Percona Server?
    El fitxer de configuració es troba al directori /etc i té el nom de my.cnf
  
  ![image](https://user-images.githubusercontent.com/61474562/154501528-79c16b20-5272-453a-b307-6a8cee389849.png)
  ![image](https://user-images.githubusercontent.com/61474562/154501957-be1cfab4-fe51-46d1-aa33-d6dbea20451e.png)

# 4.	A on es troben físicament els fitxers de dades (per defecte). Com ho has sabut?
    Es troba en el directori /var/lib/mysql
    Ho he sabut perquè en el fitxer de configuració hi ha una variable que s’anomena datadir i té la ruta de on es guarden les dades.
  ![image](https://user-images.githubusercontent.com/61474562/154502427-a4ed1af2-6ab0-4557-b70d-3b2a86ebc18d.png)
  
# 5.	Crea un usuari anomenat asix en el sistema operatiu i en SGBD de tal manera que aquest usuari del sistema operatiu no hagi d'introduir l'usuari i password cada vegada que cridem al client mysql?
    Per fer que l’usuari asix inici sessió sense haver d’introduir l’usuari i contrasenya hem de editar el fitxer my.cnf i introduir les següents línies:
  ![image](https://user-images.githubusercontent.com/61474562/154502955-d585a89a-a73d-4a0c-93f8-1e11ef1083d4.png)
     
    Comprovació:
  ![image](https://user-images.githubusercontent.com/61474562/154503074-06c6cc93-963a-467d-949d-1e9cd1ce38f8.png)

# 6.	El servei de MySQL (mysqld) escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple?
    Hauríem d’afegir la línia: port=33306 al fitxer /etc/my.cnf
  ![image](https://user-images.githubusercontent.com/61474562/154503285-aed83825-0e58-4c4a-b01c-df76bde9ede8.png)






