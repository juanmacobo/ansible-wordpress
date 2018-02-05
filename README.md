# ansible-wordpress
Despliegue wordpress con ansible


# Pasos a seguir para levantar el escenario:
**Clonar el repositorio:**
```
git clone git@github.com:juanmacobo/ansible-wordpress.git
```

**Asegurarse de que en la máquina anfitriona no se encuentre ninguna interfaz con la dirección 172.16.100.0/24.**


**Arrancar el escenario vagrant con el comando:**
```
vagrant up --provision
```

**Añadir la siguiente linea al fichero /etc/resolv.conf de la máquina anfitriona:**
```
nameserver 172.16.100.101
```

**Introducir en el navegador la siguiente dirección:**
```
wordpress.example.com
```
