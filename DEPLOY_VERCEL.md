# GUÍA DE DESPLIEGUE EN VERCEL 🚀
## Archivo Paranormal Desclasificado

Esta guía contiene todos los pasos necesarios para publicar y desplegar tu proyecto en **Vercel** de manera gratuita, rápida y con dominio HTTPS permanente.

---

## 📁 Archivos Clave Incluidos en el Proyecto:
1. **`vercel.json`**: Ya está creado en la raíz del proyecto. Configura las rutas automáticas (evita errores 404 en recargas de página) y la compresión de archivos estáticos.
2. **`package.json`**: Incluye el comando de compilación optimizado (`"build": "vite build"`).
3. **`dist/`**: Carpeta de salida generada automáticamente al compilar.

---

## 🛠️ Método 1: Despliegue con GitHub y Vercel (Recomendado)

Este método es el más fácil y permite que cada vez que actualices el código, Vercel actualice la web automáticamente:

### Paso 1: Subir tu código a GitHub
1. Ve a [github.com](https://github.com) y crea un nuevo repositorio (por ejemplo: `archivo-paranormal`).
2. Sube los archivos de tu proyecto al repositorio (usando Git o arrastrando los archivos):
   ```bash
   git init
   git add .
   git commit -m "Archivo Paranormal v1"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/archivo-paranormal.git
   git push -u origin main
   ```

### Paso 2: Conectar con Vercel
1. Entra a [vercel.com](https://vercel.com) e inicia sesión (puedes usar tu cuenta de GitHub o Google).
2. En el panel principal (Dashboard), haz clic en **"Add New..."** -> **"Project"**.
3. Selecciona tu repositorio de GitHub `archivo-paranormal` y haz clic en **"Import"**.

### Paso 3: Configurar el proyecto en Vercel
Vercel detectará automáticamente que es un proyecto **Vite**:
- **Framework Preset**: `Vite`
- **Root Directory**: `./` (dejar por defecto)
- **Build Command**: `npm run build`
- **Output Directory**: `dist`
- **Install Command**: `npm install`

*(Si utilizas alguna variable de entorno como `GEMINI_API_KEY`, puedes agregarla en la sección **"Environment Variables"**, aunque no es obligatoria para las funciones visuales y relatos).*

### Paso 4: Desplegar
- Haz clic en el botón azul **"Deploy"**.
- En unos 30-45 segundos, verás los fuegos artificiales de Vercel y tu enlace público oficial tipo:  
  `https://archivo-paranormal.vercel.app`

---

## 💻 Método 2: Despliegue Directo con Vercel CLI (Desde la Terminal)

Si tienes Node.js en tu computadora o usas la consola:

1. Abre tu terminal en la carpeta del proyecto.
2. Ejecuta el comando de Vercel:
   ```bash
   npx vercel
   ```
3. Responde a las preguntas interactivas:
   - `Set up and deploy?`: **Y**
   - `Which scope?`: Selecciona tu cuenta
   - `Link to existing project?`: **N**
   - `Project name`: Presiona Enter o pon `archivo-paranormal`
   - `In which directory is your code located?`: `./`
   - `Want to modify settings?`: **N**
4. Para pasar a producción inmediatamente:
   ```bash
   npx vercel --prod
   ```

---

## 🔑 Clave de Acceso en tu Despliegue en Vercel

Cuando abras tu enlace de Vercel desde cualquier celular o PC, la terminal de seguridad militar pedirá la clave:
- **Clave Maestra:** `UMBRA-1994` (o `1994`)
- También puedes entrar directamente sin escribir clave compartiendo tu enlace así:  
  `https://tu-proyecto.vercel.app?key=1994`

---

## ❓ Preguntas Frecuentes y Solución de Problemas:

1. **¿Da error 404 al recargar páginas?**  
   No te preocupes: el archivo `vercel.json` ya tiene la regla `"rewrites": [{"source": "/(.*)", "destination": "/index.html"}]` para redirigir todo correctamente a la SPA.
2. **¿Funciona en teléfonos móviles?**  
   Sí, está 100% optimizado para pantallas táctiles (Samsung Galaxy, iPhone, etc.) incluyendo los ojos de rastreo, sonidos retro y selector de fotos de perfil.
