# Fundación - Sitio Web

## 🚀 Inicio Rápido

## cd "c:\Users\Administrador\Desktop\Cosas\IA\Fundacion"
npm run dev

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Construir para producción
npm run build

# Preview del build
npm run preview
```

## 📁 Estructura del Proyecto

```
├── public/
│   └── images/
│       ├── carousel/       ← Imágenes del carrusel
│       ├── equipo/         ← Fotos del equipo
│       └── noticias/       ← Imágenes de las noticias
├── src/
│   ├── components/         ← Componentes de la página
│   ├── content/
│   │   └── noticias/       ← Archivos .md de noticias
│   ├── data/
│   │   ├── site.json       ← Info general del sitio
│   │   ├── equipo.json     ← Datos del equipo
│   │   └── carousel.json   ← Config del carrusel
│   ├── layouts/
│   └── pages/
└── package.json
```

## ✏️ Guía para el Admin

### Agregar una noticia nueva

1. Crear un archivo `.md` en `src/content/noticias/`
2. El archivo debe empezar con el siguiente formato:

```markdown
---
titulo: "Título de la noticia"
descripcion: "Descripción corta para la tarjeta"
fecha: 2025-06-15
imagen: "/images/noticias/nombre-imagen.jpg"
autor: "Nombre del autor"
---

Acá va el contenido completo de la noticia en formato Markdown.
```

3. Agregar la imagen correspondiente en `public/images/noticias/`

### Modificar el carrusel

Editar `src/data/carousel.json`:
- Agregar o quitar objetos del array `imagenes`
- Cada imagen necesita `src` (ruta en `/images/carousel/`) y `alt` (descripción)
- Subir la imagen a `public/images/carousel/`

### Modificar datos del equipo

Editar `src/data/equipo.json`:
- Cambiar `imagenGrupal` para la foto grupal
- Modificar el array `integrantes` con nombre, rol, descripción e imagen

### Modificar info general del sitio

Editar `src/data/site.json`:
- Nombre, descripción, misión, visión, objetivos, trabajo
- Datos de contacto (email, teléfono, dirección, redes sociales)

## 🖼️ Imágenes

Las imágenes placeholder son SVGs. Reemplazarlas con imágenes reales (.jpg, .png, .webp).

**Tamaños recomendados:**
- Carrusel: 1200x600px
- Equipo grupal: 800x400px
- Equipo individual: 400x400px
- Noticias: 600x400px

## 🌐 Deploy

Este sitio es estático. Se puede hacer deploy en:
- **Netlify**: Conectar el repo y listo
- **Vercel**: Conectar el repo y listo
- **GitHub Pages**: Usar el action de Astro

Comando de build: `npm run build`
Directorio de salida: `dist/`
