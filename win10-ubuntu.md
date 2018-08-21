# Instalación y configuración de MySQL en Microsft Windows 10

Esta guía describe la instalación y configuración detallada de MySQL en Microsoft Windows 10 y su conexión con Jupyter en el Bash-on-Ubuntu-on-Windows.

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

Abra Terminal y ejecute los siguientes comandos:

```
sudo apt-get update
```

```
sudo apt-get install mysql-server
```


#### Paso 4
Reinicie el prompt e inicie el servicio de MySQL:

```
system mysql start
```

Si requiere detener el servicio digite:

```
system mysql stop
```


### Paso 5
Desde Terminal puede iniciar el **MySQL Shell** con el siguiente comando:

```
sudo mysql -u root -p password
```


