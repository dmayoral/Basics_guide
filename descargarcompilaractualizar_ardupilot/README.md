# Descargar/compilar/actualizar ardupilot

#####Descargar ardupilot

Debes descargar ardupilot del repositorio de Github [/Beaglepilot/ardupilot](https://github.com/BeaglePilot/ardupilot).

Con el siguiente comando consigues un repositorio local:

````
git clone https://github.com/BeaglePilot/ardupilot.git
```

#####Compilar ardupilot

Supongamos que se quiere compilar `ArduCopter` en Linux:

```
cd ardupilot/ArduCopter

make clean;make linux
```
Probablemente nos indicará que hace falta un `make configure`. Introducimos dicho comando y ejecutamos de nuevo `make linux`.

En el caso de que queramos compilar `ArduCopter` en el PXF, se ha de hacer practicamente lo mismo:

```
cd ardupilot/ArduCopter

make clean;make pxf

```

#####Actualizar ardupilot

Supongamos que se desea actualizar la versión de ardupilot de nuestra erle-board:
- Descargamos el repositorio de ardupilot.
- Comporbamos que el último comit de nuestro repositorio local coindice con el del remoto (web) haciendo `git log`.
-  También podemos comprobar que copila.
-  Borramos el directorio `ardupilot`de la placa:
```
rm -r ardupilot/
```
-  Copiamos a erle-board el nuevo directorio:
```
  scp -r ardupilot/ root@192.168.7.2:/root
 ```
