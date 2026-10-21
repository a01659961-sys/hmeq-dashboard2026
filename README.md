# HMEQ — Prototipo de Dashboard V2

Prototipo navegable en español basado en las Partes I, II y IV de **Diseño de Dashboard.pdf** y en el User Flow (Figura 3, página 7). Usa tres pantallas analíticas: Panorama general, Variables de riesgo y Análisis de préstamos.

## Abrir en Visual Studio Code

1. Descomprime `HMEQ_prototipo_V2.zip`.
2. En VS Code, usa **File > Open Folder** y abre `HMEQ_prototipo_V2`.
3. Abre `index.html` con la extensión **Live Server**, o haz doble clic en el archivo `index.html` para abrirlo en un navegador.
4. Ingresa con **demo / demo**. Elige cualquier rol de demostración.
5. Sigue las decisiones **Sí / No** en la tarjeta azul. También puedes usar la barra lateral para explorar las vistas.
6. Para demostrar el escenario sin resultados, elige **Sí** en «¿Desea aplicar filtros?»; en «Escenario de prueba» selecciona «Sin resultados (simulado)» y pulsa «Aplicar filtros».

## Archivos

- `index.html`: estructura y componentes visuales.
- `styles.css`: diseño responsive de escritorio/móvil.
- `app.js`: flujo interactivo, navegación, gráficas y estados.

## Datos y limitaciones

Los valores utilizados provienen de la **Parte IV** del PDF proporcionado por el equipo. BAD global = 19.92%, n=5,958 (1,187 incumplieron y 4,771 cumplieron). Los intervalos de DEBTINC, DELINQ y LOAN siguen las cifras documentadas.

**Importante:** el PDF no contiene las filas originales de HMEQ. En consecuencia, este prototipo NO recalcula tasas con JOB, REASON o YOJ. Los controles de filtros ilustran el User Flow; el estado vacío se simula explícitamente. Las gráficas de tasas usan solo cifras reportadas y deben validarse nuevamente contra el dataset antes de una implementación productiva.

La autenticación es ficticia (no hay servidor ni control real de permisos). Nunca uses esta implementación en un entorno bancario real. Las acciones no aprueban, rechazan ni predicen créditos.

## Diferencia entre secciones del informe

La Parte II describe **tres pantallas analíticas** y su User Flow. La Parte III del documento describe **cinco pantallas** (inicio de sesión, resumen de cartera, comparación de segmentos, detalle de segmento y perfil de crédito) y propone otras rutas. Esta entrega implementa la versión de **tres pantallas + inicio de sesión ilustrativo**, pues es la que solicitaste conservar, y no pretende cubrir de forma completa el flujo alternativo de cinco pantallas. Antes de entregar el proyecto, el equipo debe unificar ambos diseños para evitar contradicciones en el reporte.

## Para convertirlo en un dashboard real

Incorpora el CSV original de HMEQ, depura BAD, define los intervalos, recalcula tasas por grupos tras los filtros, registra qué fuentes y cifras están actualizadas y conecta una autenticación real si el producto lo requiere.
