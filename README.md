# Libreavedrio - Granja Avícola Ecológica

<div align="center">
  <img src="./public/images/screenshot.png" alt="Libreavedrio Web Preview" width="600">
</div>

Este proyecto es la página web oficial de **Libreavedrio**, una granja avícola ecológica situada en la Sierra Norte de Madrid. La web está diseñada para ser una landing page moderna, responsive y fácil de configurar, que refleja los valores de sostenibilidad y bienestar animal de la granja.

## 📁 Estructura del Proyecto

El proyecto sigue una estructura limpia y modular para facilitar su mantenimiento:

-   `index.html`: Punto de entrada principal de la aplicación. Contiene la estructura semántica de la landing page.
-   `src/`: Directorio con el código fuente del sitio.
    -   `config.css`: Archivo central de configuración de estilos mediante variables CSS (design tokens).
    -   `style.css`: Estilos principales y componentes del sitio (layout, secciones, formularios, etc.).
    -   `main.js`: Lógica principal en JavaScript (interacciones, desplazamiento suave, validación y envío de formularios).
-   `public/`: Contiene los recursos estáticos como imágenes (`images/`), iconos (`favicon.png`) y utilidades gráficas (`marker.svg`).

## 🛠️ Configuración de Estilos (`src/config.css`)

El archivo `src/config.css` funciona como el **panel de control visual** de la web. Aquí se definen las variables globales de CSS que permiten cambiar la apariencia del sitio de forma centralizada.

### Propiedades Disponibles:

#### 🎨 Colores
-   `--color-bg`: Color de fondo principal (Gris suave).
-   `--color-bg-alt`: Color de fondo alternativo (Beige suave para secciones).
-   `--color-text`: Color de texto principal (Charcoal Black).
-   `--color-marker`: Color para elementos decorativos y marcadores (Maroon).
-   `--color-accent`: Color de acento (Terracotta Orange).
-   `--color-secondary`: Color secundario (usado para contrastes fuertes).
-   `--color-nav-bg`: Fondo de la barra de navegación.

#### 🖋️ Tipografía
-   `--font-heading`: Fuente utilizada para títulos (`Montserrat`).
-   `--font-body`: Fuente utilizada para el cuerpo de texto (`Open Sans`).

#### 📐 Elementos "Anarquica" (Acento visual)
-   `--rot-slight`, `--rot-bold`, `--rot-chaos`: Controlan las rotaciones de los elementos para dar ese efecto "desordenado" pero estético.
-   `--shadow-bold`: Sombras sólidas para tarjetas y botones.

#### 📏 Espaciado y Dimensiones
-   `--spacing-section`: Espaciado vertical entre secciones.
-   `--spacing-container`: Margen lateral interno de los contenedores.
-   `--width-container`: Ancho máximo del contenido (1000px).
-   `--header-height`: Altura fija del header.
-   `--bezier-stroke-width`: Grosor de las líneas curvas separadoras.

#### 🖱️ Interacción y Scroll
-   `--scroll-offset`: Margen superior al saltar a una sección (140px por defecto).

## 🚀 Desarrollo

Para ejecutar el proyecto localmente:

1.  Instala las dependencias:
    ```bash
    npm install
    ```
2.  Inicia el servidor de desarrollo:
    ```bash
    npm run dev
    ```

## 🌐 Despliegue en GitHub Pages

Este proyecto utiliza el paquete `gh-pages` para desplegar la versión compilada.

### Configuración Inicial (Solo si empiezas de cero)

1. **Instalar el paquete**:
   ```bash
   npm install --save-dev gh-pages
   ```

2. **Scripts en `package.json`**:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
2. **Vite Config (`vite.config.js`)**:
   Asegúrate de que el `base` coincide con el nombre de tu repositorio:
   ```javascript
   export default defineConfig({
     base: '/libreavedrio/',
   })
   ```

### 🚀 Cómo Desplegar Cambios

Para actualizar la web con tus últimos cambios locales, simplemente ejecuta:

```bash
npm run deploy
```

Este comando automáticamente:
1. Compila el proyecto (`npm run build`).
2. Crea/actualiza una rama invisible llamada `gh-pages` con los archivos de la carpeta `dist`.
3. Sube esa rama a GitHub.

### 🔑 Solución a problemas de Permisos (403 Forbidden)

Si al intentar desplegar recibes un error de permisos, asegúrate de estar logueado con la cuenta correcta en tu terminal usando **GitHub CLI**:

1. Instala GitHub CLI: `brew install gh`
2. Autentícate: `gh auth login` (Elige protocolo **HTTPS** y **Yes** para autenticar Git).
3. Asegúrate de que el remoto sea el correcto: `git remote set-url origin https://github.com/carlesgutierrez/libreavedrio.git`

### 🔄 Flujo de Trabajo Recomendado

- **Guardar Código Fuente**: `git push origin main` (Esto guarda tus archivos de desarrollo).
- **Actualizar Web Pública**: `npm run deploy` (Esto publica los cambios para que el mundo los vea).


---
Diseñado y desarrollado para representar la esencia de la agricultura ecológica y el respeto animal.