# 🎨 Portfolio Astro - Modern Professional Portfolio

Un portafolio moderno, responsivo y completamente estático construido con **Astro** y **Tailwind CSS**.

## ✨ Características

- ✅ **100% Estático** - Generado en build time, sin base de datos ni backend
- ✅ **Completamente basado en JSON** - Todo el contenido se importa desde archivos JSON locales
- ✅ **Fully Responsive** - Optimizado para móvil, tablet, laptop y desktop
- ✅ **Astro 4** - Framework ultraligero con cero JavaScript por defecto
- ✅ **Tailwind CSS 3** - Utilidades CSS modernas
- ✅ **Componentes Reutilizables** - Arquitectura limpia y modular
- ✅ **Alto Rendimiento** - Optimal Core Web Vitals
- ✅ **SEO Friendly** - Meta tags y mejores prácticas implementadas

## 📁 Estructura del Proyecto

```
portfolio-astro/
├── src/
│   ├── components/           # Componentes Astro reutilizables
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── ProjectCard.astro
│   │   ├── ResearchCard.astro
│   │   ├── ExperienceTimeline.astro
│   │   ├── SkillsGrid.astro
│   │   ├── Contact.astro
│   │   ├── Footer.astro
│   │   ├── Button.astro
│   │   └── Section.astro
│   ├── layouts/              # Layouts Astro
│   │   └── Layout.astro
│   ├── pages/                # Páginas (routing con Astro)
│   │   └── index.astro
│   ├── data/                 # Archivos JSON con el contenido
│   │   ├── profile.json
│   │   ├── navigation.json
│   │   ├── projects.json
│   │   ├── research.json
│   │   ├── experience.json
│   │   ├── skills.json
│   │   ├── social-links.json
│   │   └── contact.json
│   └── styles/               # Estilos globales
│       └── global.css
├── public/                   # Archivos estáticos (imágenes, favicon)
│   └── images/
├── astro.config.mjs          # Configuración de Astro
├── tailwind.config.mjs       # Configuración de Tailwind
├── postcss.config.mjs        # Configuración de PostCSS
├── tsconfig.json             # Configuración de TypeScript
└── package.json              # Dependencias del proyecto
```

## 🚀 Instalación y Ejecución

### Requisitos
- **Node.js**: 18.0.0 o superior
- **npm**: 9.0 o superior

### 1. Instalar dependencias
```bash
cd /home/gianni/Projects/portfolio-astro
npm install
```

### 2. Ejecutar servidor de desarrollo
```bash
npm run dev
```

El servidor estará disponible en `http://localhost:3000` (o el puerto que Astro asigne)

### 3. Construir para producción
```bash
npm run build
```

Los archivos estáticos se generarán en la carpeta `dist/`

### 4. Previsualizar build de producción
```bash
npm run preview
```

## 📝 Editar el Contenido

**Todo el contenido del portafolio está en archivos JSON en `/src/data/`**

### profile.json
Información personal y profesional básica:
```json
{
  "name": "Tu Nombre",
  "role": "Tu Rol Profesional",
  "tagline": "Tu tagline",
  "shortBio": "Bio corta",
  "longBio": "Bio extendida",
  "location": "Ciudad, País",
  "availability": "Disponibilidad",
  "avatar": "/images/avatar.png",
  "resumeUrl": "/resume.pdf"
}
```

### projects.json
Array de proyectos con descripción, tecnologías, links, etc.
```json
[
  {
    "id": "1",
    "slug": "project-slug",
    "title": "Nombre del Proyecto",
    "shortDescription": "Descripción corta",
    "fullDescription": "Descripción larga",
    "techStack": ["React", "TypeScript", "Node.js"],
    "tags": ["frontend", "fullstack"],
    "image": "/images/project.png",
    "demoUrl": "https://...",
    "repoUrl": "https://...",
    "featured": true,
    "status": "shipped"
  }
]
```

### research.json
Array de artículos, publicaciones y contenido:
```json
[
  {
    "id": "1",
    "title": "Título del Artículo",
    "summary": "Resumen",
    "date": "2024-03-15",
    "type": "article",
    "url": "https://...",
    "tags": ["tech", "learning"]
  }
]
```

### experience.json
Array de experiencia laboral con timeline:
```json
[
  {
    "id": "1",
    "company": "Nombre de Empresa",
    "role": "Tu Posición",
    "startDate": "2020-01",
    "endDate": null,
    "current": true,
    "summary": "Resumen del rol",
    "achievements": ["Logro 1", "Logro 2"]
  }
]
```

### skills.json
Habilidades organizadas por categorías:
```json
{
  "frontend": ["React", "TypeScript", "Astro"],
  "backend": ["Node.js", "Python", "PostgreSQL"],
  "tools": ["Git", "Docker", "AWS"],
  "cloud": ["AWS", "Vercel"],
  "design": ["Figma", "UI/UX"],
  "languages": ["JavaScript", "TypeScript", "Python"]
}
```

### social-links.json
Enlaces a redes sociales y contacto:
```json
{
  "github": "https://github.com/...",
  "linkedin": "https://linkedin.com/in/...",
  "twitter": "https://twitter.com/...",
  "email": "tu@email.com",
  "website": "https://tuportafolio.com"
}
```

### contact.json
Información de contacto y disponibilidad:
```json
{
  "title": "Título de la sección",
  "intro": "Texto introductorio",
  "email": "tu@email.com",
  "availabilityMessage": "Tu mensaje de disponibilidad"
}
```

### navigation.json
Menú de navegación principal:
```json
[
  {
    "label": "Home",
    "href": "/",
    "external": false
  },
  {
    "label": "About",
    "href": "/#about",
    "external": false
  }
]
```

## 🎨 Personalización de Estilos

### Tailwind CSS
Modifica `tailwind.config.mjs` para cambiar colores, tipografías y otros temas.

### Estilos Globales
Edita `src/styles/global.css` para cambios en animaciones, scrollbar, etc.

### Componentes
Cada componente en `src/components/` usa Tailwind CSS y es completamente personalizable.

## 🔧 Configuración

### astro.config.mjs
Configuración principal de Astro. Actualmente incluye:
- `site`: URL base del sitio

### postcss.config.mjs
Configuración de PostCSS para Tailwind CSS

### tsconfig.json
Configuración de TypeScript para soporte de tipos

## 📸 Añadir Imágenes

Las imágenes se deben colocar en `/public/images/`

Editan las rutas en los JSON:
```json
"image": "/images/nombre-imagen.png"
```

O en componentes:
```astro
<img src="/images/nombre-imagen.png" alt="Descripción" />
```

## 🌐 Desplegar

### Vercel (Recomendado)
1. Push a GitHub
2. Conecta el repositorio en vercel.com
3. Deploy automático

### Netlify
1. Push a GitHub
2. Conecta en netlify.com
3. Build command: `npm run build`
4. Publish directory: `dist`

### GitHub Pages
Actualiza `site` en `astro.config.mjs` y usa el flujo automático.

## 📋 Secciones Incluidas

- ✅ **Hero** - Presentación principal con visual llamativo
- ✅ **About** - Información personal y profesional
- ✅ **Projects** - Grid de proyectos con cards responsivas
- ✅ **Research** - Artículos y publicaciones
- ✅ **Experience** - Timeline profesional
- ✅ **Skills** - Stack tecnológico por categorías
- ✅ **Contact** - Sección de contacto y CTA
- ✅ **Header** - Navegación responsiva
- ✅ **Footer** - Pie de página

## 🎯 Características Responsive

✅ Mobile First Design
✅ Breakpoints optimizados (sm, md, lg, xl, 2xl)
✅ Navegación móvil con menú hamburguesa
✅ Imágenes responsivas
✅ Grid y flexbox adaptativos
✅ Tipografía escalable
✅ Sin scroll horizontal accidental

## 📊 Performance

- **Astro**: Cero JavaScript por defecto
- **HTML Estático**: Genera archivos .html puros
- **Tailwind**: PurgeCSS automático elimina CSS no usado
- **Optimización**: Solo envía CSS y HTML necesarios

## 🐛 Troubleshooting

### Problema: npm install falla

```bash
# Intenta con --legacy-peer-deps
npm install --legacy-peer-deps

# O reinstala completamente
rm -rf node_modules package-lock.json
npm install
```

### Problema: Tailwind CSS no se aplica

1. Verifica que `src/styles/global.css` esté importado en `Layout.astro`
2. Revisa que `tailwind.config.mjs` tiene el contenido correcto
3. Reinicia el servidor: `npm run dev`

### Problema: Componentes no se renderizan

1. Verifica que los archivos .json estén en `/src/data/`
2. Revisa que los paths en los imports sean correctos
3. Busca errores en la consola

## 📚 Recursos

- [Documentación Astro](https://docs.astro.build/)
- [Documentación Tailwind CSS](https://tailwindcss.com/docs)
- [Astro Community](https://astro.build/chat)

## 📄 Licencia

Libre para usar y personalizar.

---

**¡Disfruta creando tu portafolio! 🚀**
