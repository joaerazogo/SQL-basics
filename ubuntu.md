# Instalación y configuración de MySQL en Ubuntu

Esta guía describe la instalación y configuración detallada de MySQL en Ubuntu y su conexión con Jupyter.

#### Paso 1 (Anaconda Python)
Descargue del sitio [https://www.continuum.io/downloads](https://www.continuum.io/downloads) el
instalador de Python 3.7.

#### Paso 2
Instale los paquetes requeridos para conectar `Jupyter` con el servidor.
```
pip install ipython-sql
```

```
pip install pymysql 
```

```
pip install traitlets
```
 
 
#### Paso 3
Instale MySQL server

Habra Terminal y ejecute los siguientes comandos:

```
sudo apt-get update
```

```
sudo apt-get install mysql-server
```

#### Paso 4
Inicie el servidor y permita que el sistema inicie cuando reinicie el computador:

```
systemctl start mysql
```

```
systemctl enable mysql
```

### Paso 5
Desde Terminal puede iniciar el **MySQL Shell** con el siguiente comando:

```
/usr/bin/mysql -u root -p password
```

Luego salta de Terminal y reinicie Ubuntu.


#### Paso 6
En Terminal digite el siguiente comando para editar el archivo de configuración de MySQL 

```
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

Agregue la siguiente linea al final del archivo:

```
secure_file_priv=""
```

Oprima `Ctrl+X` para salir de nano.




