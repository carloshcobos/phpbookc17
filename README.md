# 📰 PHP & MySQL CMS – Proyecto Capítulo 17 (Jon Duckett)

Este proyecto corresponde al **Capítulo 17** del libro *PHP & MySQL: Server-side Web Development* de Jon Duckett*.  
Implementa un **sistema de gestión de contenidos (CMS)** con:

- Sección pública para visualizar artículos, categorías y búsquedas.  
- Panel de administración para gestionar contenido.  
- Integración con Twig, PHPMailer y HTMLPurifier.  
- Estructura modular y organizada con namespaces y clases.

---

## 🧩 Estructura del Proyecto

```
Proyecto
│
├── config                 # Configuración de base de datos y rutas
├── public                 # Archivos accesibles al público
│   ├── css                # Estilos del sitio
│   ├── font/icons         # Fuentes e íconos
│   ├── img                # Imágenes
│   ├── js                 # Scripts del frontend
│   └── uploads            # Archivos subidos
│
├── src                    # Código fuente y lógica de negocio
│   ├── classes            # Clases PHP organizadas por funcionalidad
│   │   ├── CMS            # Artículos, categorías, usuarios
│   │   ├── Email          # Envío de correos
│   │   └── Validate       # Validaciones
│   └── pages/admin        # Páginas del panel de administración
│
├── templates/admin         # Plantillas Twig
│
├── var/cache              # Caché de Twig
│
└── vendor                 # Dependencias instaladas con Composer
```

---

## ⚙️ Dependencias principales

- `twig/twig` — Motor de plantillas  
- `phpmailer/phpmailer` — Envío de correos  
- `ezyang/htmlpurifier` — Sanitización de HTML  
- `symfony/polyfill` — Compatibilidad PHP

Instalación:

```bash
composer install
```

---

## 🧠 Flujo general

1. `config/` define las rutas y la conexión a la base de datos.  
2. Las clases en `src/classes/` gestionan contenido, usuarios y validaciones.  
3. Las vistas Twig en `templates/` renderizan el HTML.  
4. `src/pages/` actúa como punto de entrada para las páginas públicas y el panel admin.  
5. Twig almacena la caché en `var/cache/`.

---

## ▶️ Ejecución local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/usuario/cms-jon-duckett.git
   cd cms-jon-duckett
   ```
2. Instala dependencias:
   ```bash
   composer install
   ```
3. Configura la base de datos en `/config/config.php`.
4. Inicia el servidor local:
   ```bash
   php -S localhost:8000 -t public
   ```
5. Abre en el navegador:  
   👉 http://localhost:8000

---

## 🧱 Clases principales

- **CMS/**
  - `Article.php` → Gestión de artículos  
  - `Category.php` → Gestión de categorías  
  - `User.php` → Usuarios y autenticación  
- **Email/**
  - `Mailer.php` → Envío de correos  
- **Validate/**
  - `Validator.php` → Validaciones de formularios  

---

## 📦 Requisitos

- PHP ≥ 7.4  
- MySQL ≥ 5.7  
- Composer  
- Servidor local (XAMPP, MAMP o Laragon)

---

## 🧾 Licencia

Proyecto educativo basado en el libro *PHP & MySQL: Server-side Web Development* de Jon Duckett.  
Uso exclusivamente formativo y no comercial.

📘 **Autor original:** Jon Duckett  
🧑‍💻 **Estructura y README:** [Tu Nombre]  
📚 **Capítulo:** 17 – *CMS Project*
