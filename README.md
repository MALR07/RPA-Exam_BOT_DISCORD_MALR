# 🤖 Discord RPA Bot - Gestión de Exámenes Automatizada
<img width="1254" height="1254" alt="logo EXAM BOT" src="https://github.com/user-attachments/assets/72021c34-d734-4048-b59e-2d1cc5e6b46c" />

Este repositorio contiene el flujo de automatización (RPA) desarrollado en **n8n** para optimizar la distribución de exámenes y el control de la comunidad en nuestro servidor de Discord. El sistema elimina la necesidad de subir archivos manualmente y estructurar las menciones en cada publicación.

---

## 🚀 Funcionalidades Actuales

* **⚡ Descarga Anónima y Directa:** Utiliza peticiones HTTP limpias para obtener los archivos de exámenes directamente desde Google Drive en formato binario, evitando la necesidad de configurar pesadas APIs de Google y manteniendo los enlaces públicos.
* **🖼️ Visualización Optimizada:** Envía las imágenes en tamaño completo e integradas nativamente dentro del chat de Discord, mejorando drásticamente la estética en comparación con las tarjetas de previsualización tradicionales.
* **🥷 Notificaciones con Spoiler (Menciones Ocultas):** Implementa un sistema de etiquetado avanzado mediante IDs dinámicos encapsulados en etiquetas de spoiler (`||<@&ID>||`). Esto permite que los usuarios o roles reciban el **ping (notificación en el móvil)** de forma efectiva, pero manteniendo el chat limpio mediante un recuadro oculto que solo se revela al hacer clic.
* **🛠️ Selector Manual Integrado:** El flujo cuenta con un nodo selector rápido en el lienzo de n8n que permite alternar cómodamente entre diferentes plantillas de texto preparadas antes de realizar el lanzamiento diario.

---

## 🛠️ Tecnologías Utilizadas

* **n8n (Self-hosted en Docker / Windows):** Motor principal de orquestación y lógica del RPA.
* **Discord API (Webhooks / Bots):** Canal de comunicación y entrega de contenido para la comunidad.
* **Google Drive:** Repositorio en la nube para el almacenamiento de los exámenes.

---

## 📦 Estructura del Proyecto

El archivo principal del flujo está exportado en formato estándar:
* `workflow.json`: Contiene el esqueleto de los nodos, conexiones y lógica del RPA. *(Las credenciales privadas, tokens y claves de acceso de Discord han sido omitidos automáticamente por seguridad y deben configurarse localmente).*

---

## 🔮 Próximas Mejoras (Roadmap)

* [ ] **Control de Asistencia Automatizado:** Integración con un bot oficial de Discord para escuchar en tiempo real las reacciones de los usuarios (ej. emoji `🟢`).
* [ ] **Sincronización con Google Sheets:** Registro automático en una hoja de cálculo con el nombre de usuario, fecha y hora de la peña que ha reaccionado al examen para llevar un control de rendimiento automatizado.

---

## ⚙️ Requisitos e Instalación

1. Descarga el archivo `workflow.json` de este repositorio.
2. Abre tu instancia de **n8n**.
3. Crea un flujo vacío, haz clic en los tres puntos (`...`) de la esquina superior derecha y selecciona **"Import from File"**.
4. Vincula tus propias credenciales de Discord (Token/Webhook) y actualiza los IDs de los canales o roles que vayas a taggear.
