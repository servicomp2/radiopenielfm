# Peniel 91.3 FM - PWA

![Peniel FM Logo](logo-peniel.png)

**Peniel 91.3 FM** - Cara a Cara con Dios  
Radio cristiana familiar transmitiendo fe, esperanza y amor las 24 horas del día.

## 🌟 Características

- ✨ **Diseño Moderno**: Interfaz hermosa con efectos glassmorphism y animaciones suaves
- 📱 **PWA (Progressive Web App)**: Instalable en dispositivos móviles y escritorio
- 🎵 **Streaming en Vivo**: Reproductor de audio integrado
- 🖼️ **Slider de Fondo**: Imágenes rotativas con transiciones suaves
- 🎨 **Diseño Responsivo**: Optimizado para todos los dispositivos
- ⚡ **Rápido y Ligero**: Optimizado para Cloudflare Pages

## 🚀 Despliegue en Cloudflare Pages

### Opción 1: Conectar con Git (Recomendado)

1. **Crear repositorio en GitHub**

   ```bash
   git init
   git add .
   git commit -m "Initial commit: Peniel FM PWA"
   git branch -M main
   git remote add origin https://github.com/tu-usuario/peniel-fm.git
   git push -u origin main
   ```

2. **Configurar Cloudflare Pages**
   - Ir a [Cloudflare Dashboard](https://dash.cloudflare.com)
   - **Pages** → **Create a project** → **Connect to Git**
   - Seleccionar tu repositorio
   - **Build settings**:
     - Framework preset: `None`
     - Build command: (dejar vacío)
     - Build output directory: `/`
   - Click **Save and Deploy**

3. **Configurar dominio personalizado**
   - En Cloudflare Pages, ir a **Custom domains**
   - Agregar `penielfm.com`
   - Cloudflare configurará automáticamente los DNS

### Opción 2: Despliegue Directo (Drag & Drop)

1. Ir a [Cloudflare Pages](https://pages.cloudflare.com/)
2. Click en **Create a project**
3. Seleccionar **Upload assets**
4. Arrastrar la carpeta completa del proyecto
5. Configurar dominio personalizado en **Custom domains**

## 📁 Estructura del Proyecto

```
peniel/
├── index.html          # Página principal
├── styles.css          # Estilos CSS
├── app.js              # JavaScript principal
├── manifest.json       # Configuración PWA
├── sw.js              # Service Worker
├── _headers           # Configuración Cloudflare (headers)
├── _redirects         # Configuración Cloudflare (redirects)
├── logo-peniel.png    # Logo de la emisora
├── slider/            # Imágenes del slider
│   ├── img1.jpg
│   ├── img2.jpg
│   └── img3.jpg
└── icons/             # Iconos PWA
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    ├── icon-512.png
    └── apple-touch-icon.png
```

## 🛠️ Desarrollo Local

Para probar la aplicación localmente:

```bash
# Opción 1: Usar npx serve
npx serve .

# Opción 2: Usar Python
python -m http.server 8000

# Opción 3: Usar Node.js http-server
npx http-server -p 8000
```

Luego abrir: `http://localhost:8000`

## ✏️ Personalización

### Cambiar Textos

Editar `index.html` y buscar las secciones:

- **Hero**: Líneas 92-99 (Título y descripción)
- **Nosotros**: Líneas 142-148 (Misión)
- **Contacto**: Líneas 179-213 (Info de contacto)

### Cambiar Colores

Editar `styles.css` líneas 2-9:

```css
--color-primary: #00d4ff; /* Color principal (cyan)
*/
--color-secondary: #00ced1; /* Color secundario (turquesa) */
--color-dark: #1a1a1a; /* Color oscuro */
--color-light: #ffffff; /* Color claro */
```

### Cambiar Imágenes del Slider

1. Reemplazar archivos en la carpeta `slider/`
2. Mantener nombres: `img1.jpg`, `img2.jpg`, `img3.jpg`
3. O editar `index.html` líneas 54-66 para cambiar rutas

### Cambiar Stream de Audio

Editar `index.html` línea 109:

```html
<iframe src="TU_URL_DE_STREAM_AQUI" ...></iframe>
```

## 🔧 Configuración PWA

Para que los usuarios puedan instalar la app:

1. **HTTPS requerido**: Cloudflare lo provee automáticamente
2. **Service Worker**: Ya está configurado en `sw.js`
3. **Manifest**: Configurado en `manifest.json`

### Botón de Instalación

El botón flotante "Instalar App" aparece automáticamente cuando:

- El sitio se carga por HTTPS
- El navegador soporta PWAs
- La app no está instalada aún

## 📱 Probando la PWA

### En Chrome/Edge (Desktop)

1. Abrir el sitio
2. Click en el ícono de instalación en la barra de direcciones
3. O usar el botón flotante "Instalar App"

### En Chrome/Safari (Mobile)

1. Abrir el sitio
2. **Android**: "Agregar a pantalla de inicio"
3. **iOS**: Menú → "Agregar a inicio"

## 🎨 Características de Diseño

- **Glassmorphism**: Efectos de vidrio esmerilado
- **Slider automático**: Cambia cada 5 segundos
- **Animaciones suaves**: fadeIn, pulse, float
- **Botón flotante**: Con efecto de brillo pulsante
- **Contraste mejorado**: Sombras de texto para mejor legibilidad
- **Responsive**: Mobile-first design

## 📞 Soporte

Para soporte técnico: servicomp.cesar@gmail.com

## 📄 Licencia

© 2026 Peniel 91.3 FM - Todos los derechos reservados
