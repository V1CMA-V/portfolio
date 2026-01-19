# Portfolio Personal - Víctor Martínez

Portfolio personal desarrollado con **Astro 5** y **Tailwind CSS v4**. Sitio web moderno, responsivo y optimizado para mostrar proyectos, habilidades y experiencia profesional como desarrollador de software.

## 🚀 Tech Stack

- **Framework**: [Astro 5](https://astro.build) - Sitio estático ultrarrápido
- **Estilos**: [Tailwind CSS v4](https://tailwindcss.com) - Framework CSS de utilidades
- **Lenguaje**: TypeScript
- **Fuentes**: Poppins (Google Fonts)
- **Package Manager**: pnpm

## 📁 Estructura del Proyecto

```text
/
├── public/
│   └── me2.webp              # Imagen de perfil
├── src/
│   ├── assets/
│   │   └── icons/            # 30+ iconos SVG como componentes Astro
│   ├── components/
│   │   ├── Card.astro        # Componente de tarjeta reutilizable
│   │   ├── CardProjects.astro # Tarjeta para proyectos
│   │   ├── Tabs.astro        # Sistema de pestañas interactivo
│   │   └── titleSection.astro # Título de sección
│   ├── layouts/
│   │   └── Layout.astro      # Layout base con metadata
│   ├── sections/
│   │   ├── AboutMe.astro     # Sección "Sobre mí"
│   │   ├── Cta.astro         # Call to action
│   │   ├── Footer.astro      # Pie de página
│   │   ├── Hero.astro        # Hero principal
│   │   ├── Navbar.astro      # Navegación responsive
│   │   ├── Skills.astro      # Habilidades técnicas
│   │   └── Works.astro       # Proyectos destacados
│   ├── pages/
│   │   └── index.astro       # Página principal
│   └── styles/
│       └── global.css        # Estilos globales y tema personalizado
├── astro.config.mjs
├── tailwind.config.js
└── package.json
```

## 🎨 Características

- ✅ **100% Responsivo** - Optimizado para móvil, tablet y escritorio
- ✅ **Tema Personalizado** - Sistema de colores con variables CSS
- ✅ **Navegación Interactiva** - Menú hamburguesa funcional en móvil
- ✅ **Tabs Dinámicos** - Sistema de pestañas para habilidades técnicas
- ✅ **Animaciones Suaves** - Transiciones y efectos hover
- ✅ **SEO Optimizado** - Meta tags configurados
- ✅ **Tipografía Moderna** - Fuente Poppins con letter-spacing personalizado

## 🧞 Comandos

Todos los comandos se ejecutan desde la raíz del proyecto:

| Comando                   | Acción                                           |
| :------------------------ | :----------------------------------------------- |
| `pnpm install`            | Instala las dependencias                         |
| `pnpm dev`                | Inicia el servidor de desarrollo en `localhost:4321` |
| `pnpm build`              | Construye el sitio de producción en `./dist/`    |
| `pnpm preview`            | Previsualiza la build de producción localmente   |
| `pnpm astro ...`          | Ejecuta comandos CLI de Astro                    |

## 🎯 Secciones del Portfolio

1. **Hero** - Presentación principal con imagen de perfil
2. **About Me** - Descripción profesional y enfoque de trabajo
3. **Skills** - Habilidades técnicas organizadas por categorías:
   - Diseño Web
   - Frontend
   - Backend
   - Herramientas
4. **Works** - Proyectos destacados con detalles
5. **Contact** - Información de contacto y disponibilidad

## 🌈 Sistema de Colores

El tema utiliza una paleta personalizada con colores definidos en variables CSS:

- **Primary**: Gris oscuro para estructura
- **Secondary**: Gris medio para elementos secundarios
- **Tertiary**: Gris claro para contraste
- **Accent**: Azul vibrante para CTAs e interacciones
- **Background**: Fondo oscuro principal
- **Text**: Jerarquía de texto con múltiples niveles

## 📱 Redes Sociales

- LinkedIn
- Instagram

## 👨‍💻 Autor

**Víctor Martínez**  
Freelance Web Developer

Especializado en aplicaciones web y móviles con enfoque en experiencia de usuario y escalabilidad.

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia MIT.

---

Desarrollado con ❤️ usando Astro 5 y Tailwind CSS v4
