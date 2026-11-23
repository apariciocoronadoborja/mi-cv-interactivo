# Currículum Interactivo con Inteligencia Artificial

Página web profesional y responsiva de currículum interactivo en un **único archivo `index.html`**, lista para desplegar en **GitHub Pages**.

## 🚀 Características Principales

1. **Cabecera y Perfil Profesional**:
   - Nombre: Borja Aparicio Coronado.
   - Titular: Ingeniero de Software & Especialista en Inteligencia Artificial.
   - Enlaces directos a Email, LinkedIn, GitHub y acceso rápido al chat.
   
2. **Sección Multimedia con 3 Tarjetas de Vídeo (.mp4 locales)**:
   - `pitch.mp4`: Elevator pitch de presentación personal y propuesta de valor.
   - `proyecto.mp4`: Demostración técnica y caso de estudio de proyecto destacado.
   - `habilidades.mp4`: Recorrido por competencias técnicas y metodologías.
   - Incluye estados de carga y mensaje de reserva (fallback) si los vídeos aún no se han colocado.

3. **Asistente Virtual con Gemini API**:
   - Conexión vía endpoint REST oficial de Google AI Studio (`v1beta/models/...:generateContent`).
   - Soporte para **gemini-2.5-flash** y **gemini-1.5-flash**.
   - Respuestas enriquecidas en Markdown (listas, negritas, código con `marked.js`).
   - Preguntas rápidas de sugerencia (chips) para reclutadores.

4. **Almacenamiento Seguro de API Key (Cliente / localStorage)**:
   - El visitante introduce su propia API Key de Google Gemini mediante un modal intuitivo.
   - Se guarda exclusivamente en el `localStorage` del navegador.
   - **Cero exposición en el código fuente** o repositorios públicos.
   - Indicador visual en la barra superior del estado de la clave (🟢 Activa / 🟡 Pendiente).

5. **System Instruction Especializado**:
   - Diseñado meticulosamente para actuar como tu asistente profesional y embajador técnico.
   - Responde únicamente basándose en tu experiencia, stack técnico, proyectos y datos de contacto.
   - Rechaza amablemente preguntas ajenas a tu perfil profesional.

6. **Manejo Visual de Errores en el Chat**:
   - Avisos con tarjetas de alerta si la clave no está configurada, es inválida (400/403), si se alcanza el límite de cuota (429) o si ocurre una falla de red.
   - Botón directo de acción ("Configurar API Key" o "Reintentar").

---

## 📁 Estructura del Proyecto

```text
curriculum-interactivo/
├── index.html       # Archivo único con HTML, CSS moderno y JS integrado
├── README.md        # Documentación de uso y despliegue
├── pitch.mp4        # (Coloca aquí tu vídeo de presentación)
├── proyecto.mp4     # (Coloca aquí tu vídeo de proyecto destacado)
└── habilidades.mp4  # (Coloca aquí tu vídeo de habilidades y stack)
```

---

## 🛠️ Cómo Probar en Local

Puedes abrir directamente el archivo `index.html` en tu navegador o usar un servidor local ligero:

```bash
# Opción con Python:
python3 -m http.server 8080

# Luego abre en tu navegador:
# http://localhost:8080
```

---

## 🌐 Cómo Desplegar en GitHub Pages

1. **Crea un repositorio en GitHub** (por ejemplo, `curriculum-interactivo` o `<tu-usuario>.github.io`).
2. Sube los archivos al repositorio:
   ```bash
   git init
   git add .
   git commit -m "feat: currículum interactivo con IA y vídeos"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<tu-repositorio>.git
   git push -u origin main
   ```
3. En GitHub, dirígete a: **Settings** > **Pages**.
4. En **Build and deployment**:
   - Source: **Deploy from a branch**.
   - Branch: `main` / `(root)`.
   - Haz clic en **Save**.
5. En unos instantes tu currículum interactivo estará en línea en:
   `https://<tu-usuario>.github.io/<tu-repositorio>/`
