Apuntes.
RDB (relational database)

RDBMS (Relational DataBase Magement System) Sistema Manejador de Bases de datos relacionales.

La diferencia entre ambos es que las BBDD son un conjunto de datos pertenecientes ( o al menos en teoría) a un mismo tipo de contexto, que guarda los datos de forma persistente para un posterior uso, y el Sistema de gestión de BBDD o sistema manejador, es el que nos permite acceder a ella, es un software, herramienta que sirve de conexión entre las BBDD y el usuario (nos presenta una interfaz para poder gestionarla, manejarla).

RDBMS

- MySQL
- PostgreSQL
- Etc

Todas toman un lenguaje base, pero cada uno lo apropia, imponiéndole diferentes reglas y características.

**RDBMS** significa **R**elational **D**atabase **M**anagement **S**ystem o sistema manejador de bases de datos relacionales. Es un programa que se encarga de seguir las reglas de **Codd** y se puede utilizar de manera programática.

Lo que yo usé y me funcionó en Lubuntu 18 (que seguro funcionará para Ubuntu también)

```
sudo apt-get update
sudo apt-get install mysql-server
sudo apt-get install mysql-workbench
```

Para ver la versión descargada:

```
mysql --version
```

Para configurar workbench:
(Que les recomiendo que hagan esto ahora y copien y peguen los comandos tal cual, ya que en las próximas clases les ahorrará tiempo al tratar con un tipo de error).

```
sudo mysql -u root
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'
```

Para abrir workbench:

```
sudo mysql-workbench
```

- Click al local host por default.
- Escribir la contraseña ‘password’
- Listo.

Despues de instalar MySQL en la consola (deje el link en el video anterior), instalamos MySQL Workbench:

```
sudo apt update
sudo apt install mysql-workbench
```

Luego en la consola:

```
sudo mysql -u root -p

mysql> use mysql
mysql> SELECT User, Host, plugin FROM mysql.user;
```

Debemos cambiar el plugin de auth_socket a mysql_native_password.

```
mysql> UPDATE user SET plugin='mysql_native_password' WHERE User='root';
mysql> FLUSH PRIVILEGES;
```

Revisamos los cambios:

```
mysql> SELECT User, Host, plugin FROM mysql.user;
```

En MySQL Workbench modificamos la instancia para poner la clave de root.

[Esto me ayudó](https://www.youtube.com/watch?v=SJm91cvE_ks)

Espero que les funcione 😄

![image-20210702181308127](/home/digdata/.config/Typora/typora-user-images/image-20210702181308127.png)

