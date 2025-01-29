# Proyecto Urban Grocers

## Creación de un kit para el usuario o usuaria 


### 1. Nombre del proyecto: 
qa-project-urban-Grocers-app-es

### 2. Descripcion del proyecto:
Lo que se pretende es crear un kit dentro de un usuario en especifico, para ello, se nos dan 9 listas de \
comprobacion  que nos ayudaran a evaluar diferentes tipos de datos.

### 3. La fuente de documentación utilizada:

 - apiDoc

### Descripcion de las tecnologias y tecnicas utilizadas:

 - Python: Este es el lenguage de programacion usando para automatizar las pruebas.
 - Json: Lenguaje usado para enviar y recibir datos por medio de la API
 - Requests: Se instalo esta biblioteca para poner interactuar con la API.
 - Pytest: Usado para poder correr o ejecutar las pruebas automatizadas. 
- auThoken: El el token de autenticacion usado para crear un nuevo kit de producto.
- Linea de comandos: Usado para cargar el código en GitHub

### Pasos para ejecutar las pruebas:

- conectar tu GitHub
- Clonar el repositorio en la computadora
- Trabajar con el proyecto de forma local
- Installar la libreria requets y Pytest
- Verificar que hayan 6 archivos en total onfiguration.py, data.py, sender_stand_request.py\
create_kit_name_kit_test.py, README.md, y .gitignore.
- almacenar todas las rutas en el archivo configuration.py
- Poner los cuerpos de la solicitud POST en el archivo data.py.
- Poner las solicitudes para resolver las listas de comprobacion en el archivo sender_stand_request.py
- Agregar las listas de comprobaciones en el archivo create_kit_name_kit_test.py
 
### Casos de Prueba:


1.	El número permitido de caracteres (1): kit_body = { "name": "a"}	Código de respuesta: 201


2.	El número permitido de caracteres (511): kit_body = { "name":"El valor de prueba para esta comprobación será\
inferior a"}	Código de respuesta: 201 


3.	El número de caracteres es menor que la cantidad permitida (0): kit_body = { "name": "" }	Código de respuesta: 400


4.	El número de caracteres es mayor que la cantidad permitida (512): kit_body = { "name":"El valor de prueba para\
esta comprobación será inferior a” }	Código de respuesta: 400


5.	Se permiten caracteres especiales: kit_body = { "name": ""№%@"," }	Código de respuesta: 201 


6.	Se permiten espacios: kit_body = { "name": " A Aaa " }	Código de respuesta: 201 


7.	Se permiten números: kit_body = { "name": "123" }	Código de respuesta: 201 


8.	El parámetro no se pasa en la solicitud: kit_body = { }	Código de respuesta: 400


9.	Se ha pasado un tipo de parámetro diferente (número): kit_body = { "name": 123 }	Código de respuesta: 400