# README.md

# Blog de Curiosidades

Este es un proyecto de blog desarrollado con Django 5.2.4. Permite a los usuarios registrarse, iniciar sesión, crear, editar y eliminar publicaciones. El proyecto utiliza una base de datos SQLite y una estructura modular con aplicaciones separadas para cuentas de usuario y publicaciones de blog.

## Características

- Registro y autenticación de usuarios.
- Creación, edición y eliminación de publicaciones (solo por el autor).
- Listado y detalle de publicaciones.
- Interfaz básica con estilos CSS personalizados.
- Protección CSRF en formularios.
- Panel de administración de Django habilitado.

## Estructura del Proyecto

```
blog_july/
├── accounts/           # App para gestión de usuarios
├── blog/               # App para gestión de publicaciones
├── django_base/        # Configuración principal del proyecto Django
├── static/             # Archivos estáticos (CSS)
├── templates/          # Plantillas HTML
│   ├── _base.html      # Plantilla base
│   ├── post_detail.html
│   ├── post_new.html
│   ├── posts_list.html
│   ├── post_delete.html
│   ├── update_post.html
│   └── registration/   # Plantillas de autenticación (login, signup)
├── db.sqlite3          # Base de datos SQLite
├── manage.py           # Script de gestión de Django
├── requirements.txt    # Dependencias del proyecto
└── .gitignore
```

## Instalación

1. **Clona el repositorio:**
   ```sh
   git clone <URL-del-repositorio>
   cd blog_july
   ```

2. **Crea y activa un entorno virtual (opcional pero recomendado):**
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Instala las dependencias:**
   ```sh
   pip install -r requirements.txt
   ```

4. **Realiza las migraciones:**
   ```sh
   python manage.py migrate
   ```

5. **Crea un superusuario (opcional, para acceder al admin):**
   ```sh
   python manage.py createsuperuser
   ```

6. **Ejecuta el servidor de desarrollo:**
   ```sh
   python manage.py runserver
   ```

7. **Accede a la aplicación:**
   - Blog: [http://localhost:8000/](http://localhost:8000/)
   - Admin: [http://localhost:8000/admin/](http://localhost:8000/admin/)

## Uso

- **Registro:** Haz clic en "Registrarse" en la barra de navegación.
- **Inicio de sesión:** Haz clic en "Iniciar sesión".
- **Crear publicación:** Haz clic en "Nueva Publicación" (requiere autenticación).
- **Editar/Borrar publicación:** Solo disponible para el autor de la publicación desde la vista de detalle.

## Personalización

- **Estilos:** Modifica los archivos en `static/css/`.
- **Plantillas:** Edita los archivos en `templates/`.
- **Modelos:** Modifica los modelos en `blog/models.py` y `accounts/models.py`.

## Dependencias

- Django==5.2.4
- asgiref==3.9.1
- sqlparse==0.5.3

Ver [requirements.txt](requirements.txt) para más detalles.

## Licencia

Este proyecto es solo para fines educativos. Puedes modificarlo y adaptarlo según tus necesidades.

---

Si tienes dudas o sugerencias, abre un issue o contacta al autor.