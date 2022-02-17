# Instal·lació MongoDB
#### Crear el seguent fitxer:
    ~$ sudo nano /etc/yum.repos.d/mongodb.org-4.4.repo
#### Amb el seguent contingut:
    [mongodb-org-4.4]
    name=Repositorio de MongoDB para CentOS 7
    baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/4.4/x86_64/
    gpgcheck=1
    enabled=1
    gpgkey=https://www.mongodb.org/static/pgp/server-4.4.asc
#### Actualitzem el yum:
    ~$sudo yum update
    
#### Instal·lem el mongoDB:    
    ~$ sudo yum install -y mongodb-org
    
#### Per fer la connexió hem de permitir el servei mongo al firewall:
    sudo firewall-cmd --permanent --add-service=mongodb
    sudo firewall-cmd --reload
