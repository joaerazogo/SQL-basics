**Notas de Instalación para Windows.**
	
> * MySQL Server requiere la instalación o actualización de Microsoft Visual C++, lo cual se puede ver impedido por algunos antivirus durante  la configuración del instalador. Asegurese de que su antivirus no bloquee dicha acción.


> * Para controlar el acceso a las bases de datos, MySQL Server permite la gestión de usuarios y contraseñas. Es necesario elegir la forma **NO** recomendada por el sistema durante la configuración de contraseñas y evitar la encriptación de los datos de usuario.


> * El instalador crea directorios para el almacenamiento de datos del programa y para la gestión de información en las bases de datos, en el disco C:. En Windows, el directorio necesario se encuentra por defecto oculto en el explorador de archivos, por lo que es necesario hacer visibles todas las carpetas ocultas.
	

> * Cuando se complete la instalación es necesario desactivar el modo `secure-file-priv` que impide que los archivos en el directorio de datos sean accesados por fuera del servidor. Para ello, se debe abrir el archivo `my.ini` que se encuentra en el directorio `C:\ProgramData\MySQL\MySQL Server 8.0` para Windows y asegurarse de que el campo identificado como `#Secure File Priv.` se encuentre de la siguiente forma:</div>

      # Secure File Priv.
      secure-file-priv=""

> Luego, reinicie el equipo para actualizar la sesión de MySQL Server. 



**Notas de Instalación para Mac OS.**

> * Para controlar el acceso a las bases de datos, MySQL Server permite la gestión de usuarios y contraseñas. Es necesario elegir la forma **NO** recomendada por el sistema durante la configuración de contraseñas y evitar la encriptación de los datos de usuario.

> En mac OS, para cambiar el valor de la variable. entre al directorio /Library/LaunchDaemons
y agregue la línea:

	 <string>—secure-file-priv=</string>

en el archivo 'com.oracle.oss.mysql.mysqld.plist'



#### Paso 4
Realice la conexión entre Jupyter y MySQL Server. Para seguir las instrucciones, asegurese de contar con Jupyter Notebook conectado al kernel de Python a través del promt de comandos o desde Anaconda promt, y tener correctamente instalados los paquetes mencionados. 

	1. Abra una un libro de Jupyter con el kernel de Python
	
	2. Ejecute los siguientes comandos:
		
		from traitlets.config import Bool, Unicode
		
		%load_ext sql
		
		%sql mysql+pymysql://USUARIO:CONTRASEÑA@localhost

# Información adicional

El shell de MySQL permite crear sesiones interactivas usando JavaScript, Python y SQL.

* [Instalador](https://dev.mysql.com/downloads/shell/).


* [Guía del usuario](https://dev.mysql.com/doc/mysql-shell-excerpt/5.7/en/).


Para cambiar el password de administrador use:


      SET PASSWORD FOR 'root'@'localhost' = PASSWORD('MyNewPass');


      ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';

