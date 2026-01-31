# PixelArt3D Designer

PixelArt3D Designer es una herramienta orientada a la **creación de diseños pixel art pensados específicamente para impresión 3D FDM multicolor**, con especial foco en flujos de trabajo compatibles con **Bambu Studio y AMS**.

El objetivo del proyecto es separar claramente:
- el **diseño lógico** (pixel art),
- de la **generación del archivo imprimible** (3MF),
permitiendo así un modelo de personalización controlado, reproducible y escalable.

---

## 🧩 Concepto del proyecto

El sistema se basa en tres capas diferenciadas:

1. **Administración**
   - Gestión de filamentos disponibles (colores activos/inactivos).
   - Definición de límites técnicos (número máximo de colores, tamaño de pixel, profundidad, tipo de producto).
   - Control de parámetros globales de impresión.

2. **Usuario (Editor Pixel Art)**
   - Editor basado en matriz (pixel art).
   - Selección de colores limitada a los filamentos activos.
   - Aplicación automática de restricciones según el producto.
   - El usuario **no genera archivos STL ni 3MF**.

3. **Producción (Backend / Administración interna)**
   - Conversión del diseño lógico (matriz + parámetros) en geometría 3D.
   - Optimización de la malla (fusión de regiones por color).
   - Generación del archivo **3MF listo para ser abierto en Bambu Studio**.
   - Esta capa no es accesible para el usuario final.

Este enfoque permite proteger el know-how del proceso de fabricación y evitar la distribución directa de archivos imprimibles.

---

## 🖨️ Enfoque técnico

- Destinado a **impresión FDM multicolor**
- Pensado para:
  - Bambu Studio
  - AMS / AMS Lite
- El archivo final generado es un **3MF estándar**, compatible con asignación de filamentos desde el slicer.

---

## 🔐 Licencia

Este proyecto está licenciado bajo la **GNU Affero General Public License v3.0 (AGPL-3.0)**.

Esto implica que:
- El código es libre y abierto.
- Cualquier modificación utilizada como **servicio web** debe ser publicada bajo la misma licencia.
- No se permite el uso privativo del software como SaaS sin compartir las modificaciones.

La licencia protege el proyecto frente a usos comerciales cerrados no autorizados, manteniendo al mismo tiempo un modelo abierto y colaborativo.

Consulta el archivo `LICENSE` para más detalles.

---

## 🚧 Estado del proyecto

🛠️ Proyecto en fase inicial / prototipo.  
La estructura, APIs y funcionalidades pueden cambiar durante el desarrollo.

---

## 📌 Nota

Este proyecto **no pretende sustituir un slicer**, sino actuar como una capa previa de diseño y control que garantice:
- coherencia técnica,
- repetibilidad,
- y calidad en la impresión final.

