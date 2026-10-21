# QA ejecutado

Fecha: 20 de octubre de 2026. Navegador: Chromium mediante Playwright, movimiento reducido.

## Fuente académica — PASS

Lectura de pp. 6–9, 19–22 del Gimnasio 5 antes de construir el banco. Errata p. 24 registrada en README y validada por usuario. Revisión de signos, mínimos, máximos, exactitud y omisión. Verificación automática de las 24 claves; cada clave aceptada y alteración de cada ranura rechazada. Identidad f + max(T−f,0) − max(f−T,0) = T comprobada para f de 0 a 1000 en pasos de 10, T=500. Ejemplo final comprobado por sustitución.

## Cinco partidas completas — PASS

Cada fila corresponde a siete retos resueltos en la interfaz, final visible y replay iniciado. IDs en la ejecución final:

| Vista emulada | Retos | Resultado |
|---|---|---|
| Móvil 390 × 844 | 2, 6, 8, 12, 15, 20, 22 | PASS |
| iPad vertical 820 × 1180 | 1, 4, 8, 12, 17, 19, 24 | PASS |
| iPad horizontal 1180 × 820 | 3, 5, 8, 12, 14, 21, 22 | PASS |
| Desktop 1440 × 1000 | 1, 5, 8, 13, 14, 21, 24 | PASS |
| Móvil 375 × 812 | 2, 4, 9, 13, 14, 18, 24 | PASS |

En cada partida: selección pieza → ranura; intento incompleto; deshacer; reinicio y deshacer del reinicio; error deliberado con conservación del armado; corrección; activación; feedback y siguiente; resultado 7/7 y 6 aciertos iniciales; replay limpio. Segunda ronda de cada partida completada con foco + Enter. Sin errores JavaScript. Se verificó ancho del documento ≤ viewport y altura ≥44 px de todas las fichas en cada ronda. Cinco partidas previas también completadas antes del ajuste de encabezado compacto.

Capturas generadas fuera del repositorio en el directorio temporal del harness (`metas-390.png`, `metas-820.png`, `metas-1180.png`, `metas-1440.png`, `metas-375.png`). Inspección visual de captura móvil. La validación responsive es emulada en Chromium, no una prueba de Safari ni de dispositivo físico.

## Duración y pendientes

Objetivo de diseño 70–120 s; cronómetro visible sin límite obligatorio. **Pendiente medir con estudiantes**: no se interpreta la velocidad de automatización como duración pedagógica. Pendientes pruebas físicas de iPad/Safari, lector de pantalla y percepción del sonido. Contraste, etiquetas semánticas y modo de movimiento reducido implementados; no se declara auditoría WCAG formal.
