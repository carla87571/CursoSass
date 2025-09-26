# CursoSass
Curso de Fundamentos de Sass: Crea tu Landing Page

# 🌱 EcoStore Platzi

Una landing page moderna y responsiva para una tienda ecológica, desarrollada con HTML5, CSS3 y **Sass/SCSS** como parte del curso de Sass en Platzi.

## 🚀 Demo en Vivo

🔗 **[Ver Demo](https://carla87571.github.io/CursoSass/ecoStorePlatzi/)**

## 📋 Descripción del Proyecto

EcoStore es una landing page para una tienda online especializada en productos ecológicos y sostenibles. El proyecto demuestra el uso avanzado de **Sass/SCSS** con características modernas como variables, mixins, herencia y anidación.

### 🎯 Características Principales

- 🎨 **Diseño moderno y limpio** con paleta de colores earth-tone
- 📱 **Diseño responsive** que se adapta a diferentes dispositivos
- ♻️ **Tema ecológico** enfocado en sostenibilidad
- 🛍️ **Catálogo de productos** con tarjetas interactivas
- 🗺️ **Sección de ubicación** con mapa integrado
- 🔗 **Enlaces a redes sociales** funcionales
- ✨ **Animaciones hover** suaves y elegantes

## 🛠️ Tecnologías Utilizadas

### Frontend
- **HTML5** - Estructura semántica
- **CSS3** - Estilos y animaciones
- **Sass/SCSS** - Preprocesador CSS avanzado
- **Google Fonts** - Tipografía IBM Plex Sans

### Herramientas de Desarrollo
- **Visual Studio Code** - Editor de código
- **Live Sass Compiler** - Compilación automática de SCSS
- **Live Server** - Servidor de desarrollo local
- **Git & GitHub** - Control de versiones
- **GitHub Pages** - Hosting y deploy

## 📂 Estructura del Proyecto

```
ecoStorePlatzi/
├── 📁 assets/
│   ├── 📁 img/
│   │   ├── 📁 products/     # Imágenes de productos
│   │   ├── 📁 gallery/      # Galería de estilos
│   │   └── 📁 icons/        # Iconos de redes sociales
│   └── 📁 svg/              # Iconos SVG
├── 📁 css/
│   ├── main.css             # CSS compilado
│   └── main.css.map         # Source map
├── 📁 scss/
│   └── main.scss            # Archivo principal Sass
├── 📁 .vscode/
│   └── settings.json        # Configuración Live Sass
└── index.html               # Página principal
```

## 🎨 Características de Sass Implementadas

### Variables Globales
```scss
$primary-color: #FFEFE7;      // Fondo principal
$secondary-color: #FFDAC6;    // Tarjetas healthcare
$tertiary-color: #BABD8D;     // Tarjetas furniture
$primary-text-color: #7C6A0A; // Color de texto
$font-stack: "IBM Plex Sans", sans-serif;
$paragraph-size: 1.5em;
```

### Mixins Reutilizables
```scss
// Flexbox centralizado con parámetros
@mixin flex-center($direction, $content, $align) {
    display: flex;
    flex-direction: $direction;
    justify-content: $content;
    align-items: $align;
}

// Reset de botones
@mixin buttonStyle {
    background: none;
    border-style: none;
}
```

### Herencia con @extend
```scss
.furniture {
    @extend .healthcare;  // Hereda estilos base
    .product-card {
        background-color: $tertiary-color;  // Personalización
        color: white;
    }
}
```

### Anidación Organizada
```scss
nav {
    .icons {
        button {
            @include buttonStyle;
            &:hover {
                transform: scale(1.1);
            }
        }
    }
}
```

## 📱 Secciones de la Página

### 🧭 Navegación
- Logo EcoStore
- Iconos de perfil, wishlist y carrito

### 🌍 Hero Section
- Mensaje sobre impacto ecológico
- Call-to-action button

### 🏥 Cuidado de la Salud
- 6 productos ecológicos para el cuidado personal
- Tarjetas con hover effects

### 🏠 Decoración del Hogar
- 6 productos de mobiliario sostenible
- Diseño coherente con herencia CSS

### ❓ ¿Por qué nosotros?
- Compromiso ambiental
- Innovación en diseño

### 🖼️ Galería de Estilos
- Showcase de productos en uso
- Imágenes con efectos hover

### 📍 Ubicación
- Mapa de la tienda
- Información de contacto

### 📱 Footer
- Enlaces a redes sociales
- Información corporativa

## 🚀 Instalación y Uso

### Prerrequisitos
- Visual Studio Code
- Extensión Live Sass Compiler
- Extensión Live Server

### Pasos para desarrollo local

1. **Clonar el repositorio**
```bash
git clone https://github.com/carla87571/CursoSass.git
cd CursoSass/ecoStorePlatzi
```

2. **Abrir en VS Code**
```bash
code .
```

3. **Activar Live Sass Compiler**
- Presiona `Ctrl + Shift + P`
- Busca "Live Sass: Watch Sass"
- O click en "Watch Sass" en la barra de estado

4. **Iniciar Live Server**
- Click derecho en `index.html`
- Selecciona "Open with Live Server"

5. **¡Listo!** Tu proyecto estará corriendo en `http://127.0.0.1:5500`

## 🎨 Paleta de Colores

| Color | Hex | Uso |
|-------|-----|-----|
| ![#FFEFE7](https://via.placeholder.com/15/FFEFE7/000000?text=+) | `#FFEFE7` | Fondo principal |
| ![#FFDAC6](https://via.placeholder.com/15/FFDAC6/000000?text=+) | `#FFDAC6` | Tarjetas healthcare |
| ![#BABD8D](https://via.placeholder.com/15/BABD8D/000000?text=+) | `#BABD8D` | Tarjetas furniture |
| ![#7C6A0A](https://via.placeholder.com/15/7C6A0A/000000?text=+) | `#7C6A0A` | Texto principal |
| ![#FA9500](https://via.placeholder.com/15/FA9500/000000?text=+) | `#FA9500` | Botones y footer |
| ![#E86424](https://via.placeholder.com/15/E86424/000000?text=+) | `#E86424` | Texto destacado |

## 🔧 Configuración de Sass

El proyecto utiliza Live Sass Compiler con la siguiente configuración:

```json
{
    "liveSassCompile.settings.formats": [
        {
            "format": "expanded",
            "extensionName": ".css",
            "savePath": "~/../css"
        }
    ]
}
```

## 📱 Responsive Design

- **Desktop**: Diseño completo con 3 columnas de productos
- **Tablet**: Adaptación a 2 columnas  
- **Mobile**: Vista de 1 columna con stack vertical

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para contribuir:

1. Fork el proyecto
2. Crea tu Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la Branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👩‍💻 Autor

**Carla** - [GitHub](https://github.com/carla87571)

## 🙏 Agradecimientos

- **Platzi** por el excelente curso de Sass
- **Comunidad de desarrolladores** por el feedback y soporte
- **Diseño inspirado** en tendencias de sostenibilidad moderna

---

⭐ **¡Si este proyecto te fue útil, no olvides darle una estrella!** ⭐
