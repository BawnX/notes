# **1. Detección de Navegador y Entorno de Ejecución**

## **User-Agent y Cabeceras HTTP**
- Verificar el `User-Agent` para detectar navegadores falsos o herramientas como Selenium, Puppeteer, Playwright.
- Buscar cabeceras ausentes o modificadas (ej: `Accept-Language`, `Sec-CH-UA`).
- Emuladores y bots suelen tener `User-Agent` genéricos o personalizados.
## **JavaScript y APIs del Navegador**
- **Feature Detection:** Verificar si APIs comunes están disponibles o alteradas:
	if (!navigator.bluetooth || !navigator.hardwareConcurrency) {
	    // Posible entorno controlado
    }
- **WebGL Renderer:** Extraer el renderizador de GPU (`WEBGL_debug_renderer_info`).
    - Emuladores y máquinas virtuales suelen tener valores genéricos (ej: "VMware", "VirtualBox").
- **Resolución y Color Depth:**
    - Bots suelen usar resoluciones atípicas (ej: 800x600) o profundidad de color baja.
## **Eventos de Mouse y Teclado**
- Los humanos tienen movimientos irregulares, aceleración y delays.
- Bots suelen hacer clicks perfectos (coordenadas exactas) o mover el mouse en líneas rectas.
- Ejemplo de detección:
    document.addEventListener("mousemove", (e) => {
        if (e.movementX % 5 === 0 && e.movementY % 5 === 0) {
            // Movimiento robótico (múltiplos exactos)
        }
    });
# **2. Red y Geolocalización**
## **WebRTC y Dirección IP Local**
- Los emuladores en la nube (AWS, Lambda) pueden revelar IPs internas.
- Verificar `RTCPeerConnection` para detectar IPs de hosting.
## **Dirección IP y Proxy/VPN**
- Bloquear IPs de proveedores cloud (AWS, Google Cloud, Azure).
- Verificar si la IP coincide con la geolocalización del navegador (`navigator.geolocation`).
## **Latencia y Tiempo de Respuesta**
- Los bots en la nube pueden tener latencia inusual (ej: servidores lejos del usuario real).
## **Timezone vs. Geolocalización**
- Si la IP es de EE.UU. pero el `Intl.DateTimeFormat()` muestra hora de China → posible emulación.
## **Idioma del Navegador vs. IP**
- Si `navigator.language` es "en-US" pero la IP es de Rusia → inconsistencia.
# **3. Configuración**
## **Canvas Fingerprinting**
- Cada navegador y GPU renderiza imágenes de forma única.
- Emuladores y bots suelen tener firmas genéricas.
- Ejemplo:
    const canvas = document.createElement("canvas");
    const ctx = canvas.getContext("2d");
    ctx.fillText("test", 10, 10);
    const fingerprint = canvas.toDataURL(); // Hash único
## **AudioContext Fingerprinting**
- Analizar la respuesta del sistema de audio (`AudioContext`).
- Máquinas virtuales suelen tener valores inconsistentes.
## **Tiempos de Respuesta**
- Humanos tienen delays aleatorios entre acciones.
- Bots suelen ejecutar acciones en intervalos perfectos (ej: clicks cada 500ms exactos).
## **Scroll y Touch Events**
- Los emuladores rara vez simulan scroll suave o gestos multitouch.
- Verificar si hay eventos `touchstart`, `touchend` en dispositivos que no son táctiles.
## **Variables Globales de Automatización**
- Muchas herramientas dejan rastros en `window`:
    if (window.driver || window.callPhantom || window._selenium) {
        // Bot detectado
    }
## **Propiedades del Navegador Alteradas**
- Chrome headless tiene `navigator.webdriver = true`.
- Ejemplo:
    if (navigator.webdriver || navigator.plugins.length === 0) {
        // Posible automatización
    }
# **4. Puntuación (Scoring) y Respuesta**
## **Asignar Peso a Cada Señal**
- Ejemplo de scoring:
    - `User-Agent` sospechoso: +20 puntos.
    - `navigator.webdriver = true`: +50 puntos.
    - Movimiento de mouse robótico: +30 puntos.
    - IP en AWS: +10 puntos.
## **Acciones Según el Riesgo**
- **Score bajo (<30):** Acceso normal.
- **Score medio (30-70):** Pedir CAPTCHA o 2FA.
- **Score alto (>70):** Bloquear acceso o redirigir a verificación manual.
# **Herramientas Recomendadas**
- **FingerprintJS** (detección avanzada de huella digital).
- **Cloudflare Bot Management** (detección de bots).
- **reCAPTCHA v3** (Google, para puntuar riesgo).
- **Akamai Bot Manager** (solución empresarial).
# **5. Puntos a considerar**
- Set Dispositivos 
- Reglas por disposivo o grupo disposivo
- Investigar fingerprint
- servicio ips (Nudata  o google analitics)
- Investigar AudioContext