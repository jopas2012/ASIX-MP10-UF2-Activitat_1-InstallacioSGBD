# Instal·lació MySQL

#### Descarguem els repositoris del MySQL:    
    sudo wget https://dev.mysql.com/get/mysql80-community-release-el7-3.noarch.rpm
    
#### Preparem els repositoris del MySQL:     
    sudo rpm -Uvh mysql80-community-release-el7-3.noarch.rpm
    
#### Instal·lem els repositoris:
    sudo yum install mysql-server

## 1.	A on es troben físicament els fitxers de dades?
    Les dades es troben en el directori /var/lib/mysql ja que en el fitxer de configuració ens ho indica:
#### Fitxer Configuració
  ![image](https://user-images.githubusercontent.com/61474562/154503886-4212dd73-373d-4651-a57d-45ae6d8a8579.png)

#### Directori on es guarden les dades del MySQL:
  ![image](https://user-images.githubusercontent.com/61474562/154504216-8afaa355-5feb-4c13-bb2b-44b9bcab43c5.png)

## 2.	A on es troba el fitxer de configuració? Quin és el seu contingut?
    El fitxer de configuració es troba al directori /etc i té el nom de my.cnf.
    El seu contingut són bàsicament exemples de configuració, rutes on es guarden les dades del mysql, logs i fitxers:
  ![image](https://user-images.githubusercontent.com/61474562/154504642-3b408932-6e9d-495b-a632-de2072112f7c.png)

## 3.	El procés de mysqld escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple? Important: No realitzis els canvis. Només indica els passos que faries.
     Hauríem d’afegir la línia: port=33306 al fitxer /etc/my.cnf
  ![image](https://user-images.githubusercontent.com/61474562/154504835-52490df0-5931-4270-b3bd-75db538c030c.png)

## 4.	Un cop finalitzada la instal·lació i veure que funciona, mostra el resultat de la comanda: ps -ef | grep mysql
  ![image](https://user-images.githubusercontent.com/61474562/154504920-4b885b9c-4159-4703-b530-ee2d668a3d5e.png)

## 5.	Quines són les característiques principals que ofereix MySQL 8.0 enfront de la 5.7
  - Funcions especialitzades a treballar amb JSON.
  - MySQL 8 dóna suport a funcionalitats GIS, que inclou metadades de sistema de referència, tipus espacials, índexs espacials i funcions espacials.
  - UTF8 per defecte.
  - Incorpora un diccionari de dades transaccionals que emmagatzema informació sobre objectes de base de dades.
  - Les taules admeses de la base de dades del sistema mysql ara són InnoDB.
