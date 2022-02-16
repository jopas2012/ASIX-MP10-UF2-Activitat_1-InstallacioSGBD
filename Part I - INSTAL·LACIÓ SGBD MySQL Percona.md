# 1.	Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata.
      
## Primer canvien les polítiques de contrasenya del mysql amb les següents comandes:
    SET GLOBAL validate_password.policy=LOW;
    SET GLOBAL validate_password.length=6;
## Amb la comanda mysql_secure_installation canviem la contrasenya del root i ens securitza el mysql:
    ![sdsd]("/bdd instalas SGBD/Imagen1.png")
