# openbootcamp-python

## Instalación y primeros pasos

librerias backend:
django
flask

bases de datos:
psycopg
pygresql
pysqlite3

calculos con python:
numpy
scipy
pandas

## Configuracion del intérprete

python3 --version

pip / pip3 -> para instalar librerias a nivel de sistema

pip install scipy
pip uninstall scipy

para obtener ayuda de la libreria, dentro del interprete:
help(numpy)

para ver doc concreta de una funcion:
help(nombremodulo.nombremetodo)

pypi.org -> para buscar paquetes

pip list -> para ver los modulos instalados

pip show nombremodulo -> info del paquete

virtual envs:

```
mkdir demo1
cd demo1
vi requirements.txt # este fichero utiliza pip
```

requirements.txt
flask==0.12.1

pip install -r requirements.txt

3 formas de utilizarlos:

1. comando virtualenv

```
mkdir demo1
cd demo1
virtualenv venv
source demo1/venv/bin/activate
```

which python -> para saber el python que estoy utilizando

deactivate -> para salir del entorno virtual

2. pyenv

no es compatible con windows
pyenv permite instalar diferentes versiones de pyton
virtualenv solo permite usar las que tengamos instaladas en el sistema

3. pipenv

```
mkdir demo2
cd demo2
pipenv shell # para entrar al entorno virtual
```

deactivate -> para salir

pipenv install numpy -> no haria falta entrar al entorno

esto crea un fichero que se llama Pipfile, donde estará la referencia al a dependencia instalada anteriormente

para instalar una libreria desde un repo de git 

pipenv install -e git+https://github.com/requests/requests.git#egg=requests

pipenv lock

mkdir demo4
cp demo2/Pipfile.lock demo3

pipenv install --ignore-pipfile

pipenv graph -> para ver las dependencias entre librerias

pipenv check -> para saber si la libreria tiene fallos conocidos / insegura

## Tipos de objetos en Python

Son objetos.
Las variables en Python son una referncia a una zona de memoria que guarda un contenido/valor exacto.
Los valores numericos son inmutables.

``` python
a = 5
type(a) # tipo de dato de la variable
<class 'int'>
id(a) # direccion de memoria de la variable
10918688
``` 

tipos de datos inmutables: enteros, cadenas y tuplas (tupla = (1,2,3))
tipos de datos mutables: lista -> lista = [1,2,3]


import pprint
pprint.pprint(diccionario)

diccionario.pop('clave1')

diccionario.del('clave2') ---- TODO buscar: no funciona en python 3 ?

sets: no pueden tener valores duplicados / repetidos
conjunto = {1,2,3}
los conjuntos tienen operaciones matematicas

a | b -> union del conjunto a con el conjunto b -> valores no repetidos cuando se juntan ambos sets
a & b -> interseccion -> que tengo en comun en los dos conjuntos
a - b -> diferencia -> que valores no estan en uno pero no en otro conjunto
a ^ b -> diferencia simetrica -> que valores son unicos en los dos

Metodos y operadores:

Cadenas:
 
miTexto.Capitalize()

Operadores:

= asignacion
+ suma
- resta
// dividir
% modulo
** potenciacion
+= 




















