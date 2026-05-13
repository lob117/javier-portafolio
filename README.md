# javier-portafolio
# Portafolio Interactivo | Ingeniería Aplicada

Este repositorio contiene el código fuente de mi portafolio profesional web. Está diseñado como una Single Page Application (SPA) utilizando HTML5, CSS3 y Vanilla JavaScript, sin depender de frameworks pesados. 

Más allá de ser una web estática, el sitio actúa como un cliente en vivo que consume telemetría IoT en tiempo real desde la nube y renderiza dashboards dinámicos.

## 🚀 Características Técnicas Destacadas

* **Enrutamiento SPA Nativo:** Navegación fluida entre secciones (Inicio, IoT, UAV, Automatización) manejada íntegramente con JavaScript manipulando el DOM y clases CSS (`showView()`), evitando recargas de página.
* **Consumo de API Serverless:** Integración asíncrona (`fetch`) con un endpoint de AWS API Gateway acoplado a una Lambda que consulta una base de datos PostgreSQL (Neon).
* **Optimización FinOps (Page Visibility API):** El script de monitoreo IoT en tiempo real utiliza `document.addEventListener("visibilitychange")` para pausar las peticiones HTTP (polling cada 30s) cuando la pestaña está oculta, protegiendo los límites del *Free Tier* de AWS.
* **Renderizado de Grafana Snapshot:** Lógica avanzada para hacer fetch de un snapshot JSON desde `snapshots.raintank.io` y dibujar los gráficos de series de tiempo nativamente usando `Chart.js` como respaldo interactivo.
* **Diseño Responsive y CSS Variables:** Uso extensivo de variables CSS (`:root`) para mantener la paleta de colores cyberpunk/técnica, y CSS Grid/Flexbox para adaptar el contenido a dispositivos móviles.

## 🛠️ Stack Tecnológico Frontend

* **Estructura:** HTML5 Semántico
* **Estilos:** CSS3 (Grid, Flexbox, Keyframe Animations, Custom Properties)
* **Lógica:** Vanilla JavaScript (ES6+, Async/Await, Fetch API)
* **Librerías Externas:** Chart.js (v4.4.1) para renderizado de gráficos y Google Fonts (Orbitron, Rajdhani, Space Mono).

## 📂 Estructura de las Vistas

1.  **Inicio (`#view-inicio`):** Resumen de perfil, stack de tecnologías y galería de accesos rápidos a proyectos.
2.  **IoT Dashboard (`#view-iot`):** Visualización de datos de la estación meteorológica ESP32 en tiempo real, métricas clave (Temperatura, Humedad, Sensación Térmica, Nivel) y esquema de arquitectura Cloud.
3.  **UAV & GIS (`#view-uav`):** Repositorio multimedia de vuelos fotogramétricos, modelos de elevación (DEM), mapas interactivos y nube de puntos.
4.  **Automatización (`#view-auto`):** Demostración de flujos de trabajo en n8n y accesos directos a repositorios de RPA, IA y Web Scraping.

## ⚙️ Despliegue

Este proyecto está optimizado para ser alojado en entornos estáticos severless.
Puede ser desplegado directamente utilizando:
* **GitHub Pages:** Sirviendo desde la rama `main` (configuración recomendada).
* **Cloudflare Pages:** Vinculando el repositorio para despliegues automáticos globales en el borde (Edge).

## 👤 Autor

**Javier José Lobato Ceballos**
*Ingeniero Electrónico*

Especializado en el desarrollo de sistemas ciberfísicos, combinando el diseño de hardware embebido (IoT), procesamiento de datos geoespaciales (GIS/UAV) y arquitecturas en la nube. 

---
*Diseñado y codificado desde cero - 2025*
