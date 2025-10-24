BkManager – CRUD con Django y MySQL

Aplicación web desarrollada con **Django 5** que permite administrar una colección de libros mediante operaciones **CRUD** (crear, leer, actualizar y eliminar).  
La aplicación utiliza una base de datos **MySQL** (configurada en XAMPP) y permite agregar libros con título, descripción e imagen, generando automáticamente un **ID único** para cada registro.


## 🚀 Características principales

- 🗃️ CRUD completo de libros (crear, listar, editar, eliminar)
- 🖼️ Carga de imágenes para cada libro (usando Pillow)
- ⚙️ Base de datos MySQL integrada mediante PyMySQL
- 🌐 Backend en Django 5
- 🎨 Interfaz limpia con Bootstrap y HTML base
- 🔐 Configuración fácil y rápida para entornos locales (XAMPP)


---

## 🧰 Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- [Python 3.10 o superior](https://www.python.org/downloads/)
- [Git](https://git-scm.com/)
- [XAMPP (con MySQL) - [MariaDB 11.8.3]](https://www.apachefriends.org/es/index.html)
- pip (gestor de paquetes de Python)
- virtualenv (opcional pero recomendado)

---

## ⚙️ Instalación paso a paso

### 1 Clonar el repositorio

- ```bash
- git clone https://github.com/nicogomezdev/CRUD-DJANGO.git
- cd bookmanager

### 2 Crea tu entorno virtual
- python -m venv venv

    ## Activalo
- venv\Scripts\activate
- source venv/bin/activate


### 3 Crea dependencias
- pip install -r requirements.txt

### 4 Configura la base de datos en settings.py
- python manage.py migrate
- python manage.py runserver

### 5 Requisitos
asgiref==3.9.2
Django==5.2.6
pillow==11.3.0
PyMySQL==1.1.2
sqlparse==0.5.3
tzdata==2025.2

### 6 Configura la base de datos
- Actualiza la versión de MARIA DB en XAMPP a la version 11.8.3 o superior
- Inicia XAMPP y activa el módulo MySQL. 

- Abre phpMyAdmin y crea una base de datos llamada libreria

    ### verifica que en settings tengas la configuracion
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'libreria',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'localhost',
        'PORT': '3306'
    }
} 

### 7 Migraciones
Ejecuta los siguientes comandos en la raiz del proyecto 

- python manage.py makemigrations
- python manage.py migrate

(Esto creará las tablas necesarias en MySQL)


   ### Crea el superusuario para acceder al panel de administración de DJANGO
python manage.py createsuperuser

### 8 ejecución del proyecto 
Ejecuta el siguiente comando

python manage.py runserver

   ### Abre tu navegador

-Entra a la siguiente URL http://127.0.0.1:8000/

### 9 Funcionalidades del CRUD
- Agregar libro
- Editar libro
- Eliminar libro
- Listar libro


### Autor
NicoDev -- Johan Nicolas Gomez Buitrago 
Desarrollador web con experiencia en Python, Django, HTML, CSS, java y JavaScript.

Github: https://github.com/nicogomezdev

###                         NICO DEV. ALWAYS LEARNING, ALWAYS BUILDING


