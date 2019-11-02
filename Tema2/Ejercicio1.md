# Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

En Python está `virtualenv` que para crear un entorno virtual basta con especificarle la ruta donde crear dicho entorno. Adicionalmente, con la opción `-p` o `--python` se le puede especificar la versión de python que se va a usar en dicho entrono virtual.

Ejemplo:
```bash
python --version # para ver la versión por defecto instalada en el sistema
# En este caso la 3.6.8
virtualenv entorno # crearía una carpeta llamada *entrono* donde su interior
#sería un entorno virtual de python 3.6.8 con sus propias librerías
cd entorno && source bin/activate # entraríamos en el entorno y lo activaríamos
# a partir de ahora, las librerías que se necesiten e instalen será solo en el 
# propio entorno
pip install django # instalaría DJango en el entorno pero no en el SO
deactivate # sale de entorno virtual
python -m django # si no teníamos DJango instalado, no lo seguiremos teniendo
virtualenv -p `which python2` entorno2 # crearíamos un nuevo entorno con python2
cd ../entorno2 && source bin/activate && pip install django # instalaríamos
# DJango en python2
```