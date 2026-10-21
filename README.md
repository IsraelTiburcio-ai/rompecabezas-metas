# ROMPECABEZAS DE METAS

**Construye el modelo correcto.** Microjuego para Optimización I, Gimnasio 5, apartados 5.4, 5.6 y 5.7. HTML, CSS y JavaScript vanilla. Sin instalación ni compilación. Abrir `index.html` o servir esta carpeta con un servidor estático.

## Contenido y operación

24 rompecabezas; 7 por partida, uno aleatorio de cada etapa, sin repeticiones dentro de una partida. Fisher–Yates mezcla retos y piezas. Faltante → exceso → restricción meta → estructural → objetivo mínimo → objetivo máximo → integración. Objetivo de duración: 70–120 segundos, sin expulsión por tiempo. El cronómetro incluye lectura del feedback y ayuda.

Tocar pieza y tocar ranura. Tab y Enter/Espacio ofrecen la misma interacción. Las piezas se consumen una vez; las repetidas tienen identidades independientes. Para retirar una pieza, tocar su ranura sin selección activa. Deshacer guarda estados completos; reiniciar también es reversible. Los errores no borran respuestas. El avance correcto es manual para permitir leer el feedback. Sonido optativo generado con Web Audio; sin archivos externos. Fuentes web con fallback local.

`data.js` contiene exclusivamente construcción del banco y claves. `script.js` implementa selección, validación y partida. Las ranuras tienen roles explícitos y signos fijos. En objetivos exactos se solicita colocar primero el faltante, evitando ambigüedad de conmutación. No se exige una identidad física específica para fichas con igual texto.

## Revisión de fuente y registro académico

Fuente revisada: `GYM 5_251128_083844.pdf`, páginas 6–9, 19–22. Modelo general en p. 21, definiciones en p. 22. Convención: f(x) + d⁻ − d⁺ = T; todas las desviaciones ≥ 0. Meta mínima penaliza d⁻, máxima d⁺ y exacta ambas con pesos positivos. P₁, P₂ son niveles lexicográficos, no números de ponderación.

**Errata observada en p. 24:** la expresión impresa `15x₁ + 25x₂ + d₁⁺ + d₁⁻ = 600` tiene signo positivo para el exceso. Contradice los ejemplos de pp. 6, 20, 21 y 25. Se solicitó validación académica al usuario; autorizó registrar la errata y emplear `+d⁻ −d⁺` mediante «dale». El banco no reproduce esa expresión errónea.

Omitir d⁺ en la ecuación impone f(x) ≤ T; omitir d⁻ impone f(x) ≥ T. No equivale a omitir una de la función objetivo. El reto integrador de omisión trabaja dos expresiones independientes y una tercera meta exacta. La ayuda advierte que la ecuación sola no garantiza complementariedad: la representación natural de faltante/exceso usa los máximos con cero, y la minimización con penalizaciones positivas evita inflación simultánea en los casos aplicables.

Ejemplo final factible: x₁ = 10, x₂ = 20, capacidad 2x₁ + x₂ = 40, utilidad 4x₁ + 3x₂ = 100. d⁻ = d⁺ = 0, objetivo mínimo 0.

## Publicación

Repositorio nuevo `rompecabezas-metas`. Pages mediante Actions sobre `main`; workflow `.github/workflows/pages.yml`.

## QA

Los resultados ejecutados se registran en `QA.md`. Las comprobaciones de viewport son emuladas; no sustituyen una prueba física en iPad ni una medición pedagógica con alumnos.
