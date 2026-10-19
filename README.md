# AI Factory Challenge — Simulador web

Sitio estático para GitHub Pages. Abre `index.html` o publica el repositorio con Pages.

## Uso
1. Selecciona **CARGAR EXCEL**.
2. Elige un `.xlsx` con hoja `Schedule` y columnas `job`, `operation`, `machine`, `start`, `finish`, `processingTime`.
3. Pulsa **INICIAR** y ajusta la velocidad.

## Privacidad
Los Excel se procesan en el navegador; no hay código que los suba a un servidor. Se descarga la biblioteca SheetJS desde jsDelivr para leer Excel, por lo que se requiere Internet. En producción, conviene alojar localmente una versión revisada y fijada de la biblioteca, configurar CSP y mantenerla actualizada.

## Validaciones
Archivo hasta 2 MB, máximo 5000 operaciones, sin solapamientos de máquina, sin violación de precedencias de trabajos, duraciones coherentes. La página valida la coherencia del calendario, pero **no** verifica que corresponda a una instancia original dada.
