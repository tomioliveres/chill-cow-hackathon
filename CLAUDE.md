# Chill Cow — Hack to the Future 2026

Contexto del proyecto para cualquier integrante del equipo (o su sesión de Claude) que siga trabajando acá. Leé también `docs/DECISIONES.md` antes de cambiar el pitch o el prototipo.

## Qué es

- **Hackathon:** Hack to the Future (Córdoba, 12 y 13/11/2026, ITC + Córdoba Cluster, financiado por la UE / Global Gateway). Vertical **Agro** (transición verde y sostenible).
- **Producto:** **Chill Cow** (así se escribe en la marca). Monitoreo del bienestar animal en el **transporte del campo a la planta** para **frigoríficos exportadores** que necesitan demostrar ante la UE que cada tropa viajó sin maltrato.
- **Idea en una frase:** usamos datos que ya existen en la cadena (caravana electrónica obligatoria leída por NFC, DT-e, celular del chofer, cámaras y registros de la planta) para calcular un **Índice de bienestar por tropa** y emitir un informe/certificado para el comprador europeo.
- **Regla del mentor:** ningún chip ni dispositivo nuevo en el animal.

## Equipo (orden por apellido)

Bejega Matias · Hoffmann Augusto · Laria Micaela · Marmay Tomas · Oliveres Tomas · Pereira Celeste · Tello Marysol Ariadna

## Agenda del día 2 (13/11/2026)

- 9:00–10:45 ajustes finales
- **10:45 pitch de la vertical (3 minutos)**
- 8 finalistas, ronda final 13:15
- Criterios del jurado: impacto 25 %, innovación 20 %, factibilidad técnica/económica 20 %, escalabilidad 15 %, vínculo con el ecosistema 10 %, pitch/equipo 10 %

## Mapa de carpetas

| Carpeta | Qué hay |
|---|---|
| `prototipo/` | `index.html`: prototipo clickeable (abrir en el navegador). `capturas/`: screenshots de cada paso. |
| `pitch/` | `ChillCow_Pitch.pdf` / `.html`: deck final en un solo archivo. `ChillCow_Guion_Pitch.pdf`: guion cronometrado. `project/`: fuente del deck (una slide HTML por archivo en `slides/`, orden en `deck.json`). `Hack to the Future - PITCH.pdf`: requisitos de la organización para el pitch. |
| `brief/` | Brief del prototipo (pantallas, índice, guion de demo). Base del producto. |
| `guia-de-marca/` | Manual de marca (HTML/PDF) y `chillcow-tokens.css`. Usar solo la identidad visual, no los mockups de ejemplo del manual. |
| `material-hackaton/` | Material de la organización (cómo redactar la idea, prehackathon). |
| `docs/DECISIONES.md` | Decisiones tomadas, con el porqué y los datos verificados. |

## Prototipo

- Abrir `prototipo/index.html` en el navegador.
- Dos modos (barra superior): **Demo completa** (viaje en vivo) y **Modo pitch** (pasos 1 Carga → 4 Informe + Certificado; teclas ← → / 1–5 / PageDown).
- Atajos por URL: `#paso-1` … `#paso-5` (5 = certificado con la barra) y `#cert` (certificado público en inglés, sin barra; es a donde apunta el QR). `?tema=claro|oscuro` fuerza el tema.
- Demo en vivo: 1 s = 2 min simulados (viaje de 4 h 10 min ≈ 125 s). Graba sola 1 curva + 1 frenada; el presentador agrega 1 frenada (tecla F o el `···` oculto bajo el teléfono), toca "Llegué", "Leer caravanas", marca la caravana 07 como caída → índice **67 Atención** (Accidentes 67 / Condiciones 100).
- En el pitch de 3 minutos el viaje en vivo no entra: usar los atajos `#paso-N`.
- Si editás `index.html`, mantené `<meta charset="utf-8">` o se rompen los acentos al abrirlo como archivo.

## Pitch

- Orden del deck: portada → gancho → problema → solución → demo → qué lo hace distinto → impacto → escala; después, slides de respaldo: mercado, qué aprendimos, plan B, fuentes.
- La organización exige mostrar: equipo, una persona real con el problema y "qué aprendimos".
- Ángulo UE: reciprocidad / cláusulas espejo y la cuota de carne del acuerdo UE–Mercosur (99 mil t).
- Si cambiás una slide de `pitch/project/slides/`, hay que regenerar `ChillCow_Pitch.html` y `ChillCow_Pitch.pdf` (se arma con Chrome headless e impresión a 1920×1080).

## Versiones publicadas (links de Claude)

Son artifacts privados de la cuenta de Tomás Oliveres; pedile acceso si los necesitás. La fuente de verdad son los archivos de este repo.

- Prototipo: https://claude.ai/artifact/3h6sa3s4rEHHHWAi8ckqNs (certificado: mismo link + `#cert`)
- Deck: https://claude.ai/artifact/MXEGZ2gTCveqYtLzihQHXR
- Guía del pitch de 3 minutos: https://claude.ai/artifact/FStGS8VtmpBQp58MAL5qSu
- Doc de respaldo con datos y normativa: https://claude.ai/artifact/K8Q9roMxYoQBzZE4yBT29i
- Brief del prototipo: https://claude.ai/artifact/UfyDJE4xkF8uNWe3ugWNXq

## Commits y push (en la computadora de Tomás Oliveres)

Repo: https://github.com/tomioliveres/chill-cow-hackathon (público, rama `main`). Autorizado por Tomás:

1. Antes de hacer commit y push a `main`, cambiar a la cuenta dueña del repo: `gh auth switch -u tomioliveres`.
2. Hacer el commit y el push.
3. Apenas se confirme el push, volver a la cuenta por defecto: `gh auth switch -u atomdev1`.

La carpeta `estudio/` no se sube nunca (está en `.gitignore`). Los compañeros pushean con su propia cuenta si Tomás los agrega como colaboradores.

## Reglas de relato (obligatorias en pitch, deck, docs y prototipo)

- La idea **arrancó de cero en la hackathon**. No mencionar estudios académicos previos, nombres de proyectos anteriores ni el hardware (collar/sensor) propuesto antes.
- "Qué aprendimos" = la regla del mentor "ningún dispositivo nuevo en el animal".
- No hay contacto real con un frigorífico: la persona del problema es el rol **"la jefa de calidad de un frigorífico exportador"**, nunca un nombre inventado.
- Se habla de **Índice de bienestar** (100 = perfecto; Calma 70–100, Atención 40–69, Alerta < 40), con sub-índices Accidentes y Condiciones del viaje. Nunca "índice de estrés".
- No inventar números: la columna de hematomas de la pantalla 8 dice "Se carga al faenar".
- Las recomendaciones de la pantalla 8 son un ejemplo ficticio basado en historial, no IA predictiva.
