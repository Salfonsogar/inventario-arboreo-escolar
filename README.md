# Inventario arbóreo escolar

Aplicación de captura en campo para el **censo digital del arbolado de las instituciones educativas del municipio de Valledupar (Cesar)**, en el marco del proyecto interdisciplinario de la Universidad Popular del Cesar.

**Sitio publicado:** https://salfonsogar.github.io/inventario-arboreo-escolar/

## Qué implementa

La aplicación implementa el *Protocolo de campo para el inventario dasométrico, fitosanitario y de salud ambiental de los árboles en las instituciones educativas* (Universidad Popular del Cesar, 2026). Cubre las secciones del diccionario de datos del protocolo:

| Sección | Contenido |
| --- | --- |
| 8.1 | Identificación y registro (institución, GPS, fotografías, código único) |
| 8.2 | Identificación taxonómica |
| 8.3 | Variables dasométricas (DAP/CAP, alturas, copa, inclinación, estado de desarrollo) |
| 8.4 | Emplazamiento y conflictos con la infraestructura |
| 8.5 | Estado fitosanitario (raíz y cuello, fuste, ramas, copa y follaje, agentes bióticos y abióticos) |
| 8.6 | Historial de intervención |
| 8.7 | Evaluación del riesgo ISA-TRAQ (con las matrices de probabilidad de falla, impacto y consecuencias) |
| 8.8 | Recomendación de manejo |
| 8.9 | Variables complementarias |
| 8.10 | Confort térmico (ΔT, índice de calor, sombra útil) |
| 8.11 | Saneamiento y salud ambiental (criaderos de mosquitos, sistemas de agua, infiltración) |
| 8.12 | Interacción con la comunidad escolar |
| 10 | Cálculo del Índice de Valor del Árbol Escolar (IVAE, pesos provisionales) |

Además calcula automáticamente el DAP a partir del CAP, el área de copa, el ΔT, el índice de calor, el nivel de riesgo y el IVAE, y verifica la lista de control de calidad de la Tabla 26 del protocolo.

## Características

- **Interfaz tipo aplicación móvil** con las mismas pantallas del prototipo original: inicio con ilustración y tarjetas de resumen, lista de árboles con búsqueda y filtros, mapa esquemático por institución y panel de estadísticas.
- **Funciona sin conexión.** Los registros se guardan en el almacenamiento local del dispositivo (RF-01).
- **Motor guiado por el diccionario de datos del protocolo:** 18 pasos de captura con validaciones (RF-04, RF-07).
- **Datos piloto de demostración:** la primera vez que se abre, la aplicación carga **128 registros de ejemplo** (14 especies, DAP promedio 46,3 cm, altura promedio 10,2 m) para mostrar el comportamiento del panel y del mapa. Se pueden restablecer o borrar desde «Exportar datos».
- **Exportación** a CSV (para la hoja de cálculo del proyecto) y GeoJSON (para el SIG).
- **Sin dependencias externas** ni CDN: un único archivo `index.html` autónomo (las tipografías Bricolage Grotesque y Atkinson Hyperlegible van incrustadas).

## Archivos

- `index.html` — aplicación de captura en campo (interfaz e implementación del protocolo).
- `app-original.html` — prototipo anterior, conservado como respaldo (fuente de las tipografías y del diseño).
- `docs/protocolo-de-campo.md` — protocolo de campo en formato Markdown (fuente del diccionario de datos).

## Actualizaciones

Para publicar cambios basta con reemplazar `index.html` y hacer:

```bash
git add -A
git commit -m "update"
git push
```

GitHub Pages publica automáticamente desde la rama `main` (raíz `/`).
