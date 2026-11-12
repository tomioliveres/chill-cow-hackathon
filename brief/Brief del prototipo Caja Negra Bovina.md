# Brief del prototipo: Caja Negra Bovina

Nov 12, 2026 · @Movisuelos

## La idea en una frase

Ayudamos a los **frigoríficos exportadores** a **demostrar ante la UE que cada tropa viajó sin maltrato** mediante **datos que ya existen en la cadena** (la caravana obligatoria, el DT-e, el celular del chofer y las cámaras y registros de la planta), para que **pierdan menos carne por golpes y certifiquen bienestar animal en cada embarque**.

El prototipo de mañana tiene que mostrar tres cosas en vivo:

1. Un viaje que se registra solo con el celular del chofer: una frenada brusca aparece en el panel del frigorífico.
2. La recepción de la tropa: se leen las caravanas, se marca un animal caído y el checklist UE se completa.
3. El informe final por tropa: cumplimiento UE, índice de riesgo y un QR de certificado para el comprador europeo.

Regla de diseño del mentor: **no se fabrica ningún chip ni dispositivo nuevo para el animal**. Todo sale de lo que el animal y la cadena ya tienen.

Alcance: solo **bienestar animal en el transporte, del campo a la planta**. Quedan fuera la cría, el feedlot y la verificación de deforestación (EUDR), que se mencionan solo como escalabilidad.

## Problema

El viaje del campo a la planta es una caja negra: nadie registra cómo viajó la tropa, y casi 6 de cada 10 animales llegan golpeados. El frigorífico lo descubre recién en la res, cuando ya perdió la carne, y no tiene cómo demostrarle a la UE que la tropa viajó bien.

| Dato | Valor | Fuente |
| --- | --- | --- |
| Animales con al menos una lesión al llegar a faena | 58,8 % de 15.361 | IPCVA, 2008 |
| Carne perdida por recortes de lesiones | ≈1,37 kg por animal | IPCVA, 2008 |
| Peso vivo perdido en el viaje | 2 % a 10 % según la distancia | CFI |
| Exigencia de la UE | Certificar en cada embarque bienestar animal equivalente al europeo | Reg. (CE) 1099/2009, art. 12 |

A quién le pasa: al **frigorífico exportador** de Córdoba o la región Centro, que recibe tropas de muchos campos y transportistas distintos, paga la carne perdida y firma la certificación ante la UE.

Todas las cifras y normas están respaldadas en el documento [Respaldo oficial: bienestar animal en el transporte bovino y exportación a la UE](https://claude.ai/artifact/K8Q9roMxYoQBzZE4yBT29i). No usar el "20 %" ni el "40 %" de los paneles anteriores: no tienen fuente.

## Usuarios

El cliente que paga es el frigorífico exportador; el chofer solo carga datos. El panel del frigorífico es la pantalla principal de la demo.

| Usuario | Dónde está | Qué necesita | Dispositivo | Prioridad en la demo |
| --- | --- | --- | --- | --- |
| Jefe de recepción de hacienda (frigorífico) | Corrales y rampa de descarga | Saber qué tropas llegan, cuáles vienen con problemas y registrar la llegada en minutos | Tablet o PC | Principal |
| Veterinario oficial o de calidad (frigorífico) | Recepción e inspección | Ver la evaluación de cada envío a la llegada, como pide la UE | Tablet o PC | Principal |
| Responsable de exportación o calidad | Oficina | Informe por tropa y certificado para el comprador europeo | PC | Principal |
| Chofer del camión | Cabina, en ruta | Iniciar el viaje y no tener que tocar nada más; avisos simples si algo sale de norma | Su propio celular | Secundaria |
| Comprador o auditor europeo | En la UE | Verificar el certificado de una tropa sin cuenta ni login | Cualquier dispositivo, por QR | Secundaria |

Criterio de diseño para el chofer: **sin leer y sin tocar mientras maneja**. Semáforo, vibración o sonido, nunca texto largo.

## Cómo funciona

&#91;embedded content: recorrido de la tropa · 5 pasos\]

Los pasos 1 a 4 juntan datos que hoy ya se generan pero nadie cruza; el paso 5 los convierte en la evidencia que pide la UE. En el viaje se mide por tropa, y en la carga, la llegada y la res, por animal (gracias a la caravana).

## Cómo cumplimos la norma UE

Cada fila del checklist de la pantalla corresponde a un artículo de una norma real. Las del Reg. 1099/2009 son obligatorias para exportar; las del Reg. 1/2005 son la vara de referencia para el viaje.

| Ítem del checklist | Norma | Umbral | Cómo lo medimos | Qué muestra la pantalla |
| --- | --- | --- | --- | --- |
| Tiempo de viaje | Reg. 1/2005, Anexo I cap. V 1.2 y 1.4 | 8 h en camión estándar; 14 + 1 + 14 h en camión equipado | Hora de carga (caravanas leídas o DT-e) contra hora de descarga | Horas de viaje y semáforo |
| Temperatura en el viaje | Reg. 1/2005, Anexo I cap. VI 3.1 | 5 °C a 30 °C, tolerancia ±5 °C | Clima en la ruta por el GPS del celular del chofer | Curva de temperatura con la franja permitida |
| Espacio por animal | Reg. 1/2005, Anexo I cap. VII | 0,95–1,3 m² (\~325 kg); 1,3–1,6 m² (\~550 kg) | Cabezas leídas ÷ m² de la jaula, con el peso del DT-e o la balanza | m² por animal contra el rango |
| Manejo durante el viaje | Reg. 1/2005, Anexo I cap. III 1.8 (golpes y manejo brusco) | Sin umbral numérico: buena práctica | Frenadas y curvas bruscas por acelerómetro del celular | Eventos en la línea de tiempo del viaje |
| Evaluación del envío a la llegada | Reg. 1099/2009, Anexo III 1.1 | Evaluar cada envío al llegar | Informe de la tropa listo antes de la descarga | Ficha de la tropa con prioridades |
| Animales caídos o que no caminan | Reg. 1099/2009, Anexo III 1.11 | No arrastrarlos | Cámara en la rampa o marca del operario en la recepción | Contador de caídos con caravana asociada |
| Espera en corrales | Reg. 1099/2009, Anexo III 1.2 y 1.6 | Agua permanente; alimento si pasan más de 12 h | Hora de llegada contra hora de faena | Horas en corral y alerta a las 12 h |
| Resultado en la res | Calidad del producto (no es norma UE) | — | Hematomas y decomisos que ya registra la inspección | Hematomas por tropa, comparados con el índice |

Lo que el prototipo **no** promete: no mide cortisol, temperatura corporal ni golpes por animal dentro del camión. En el viaje medimos **por tropa**; por animal medimos en la carga, en la descarga y en la res.

## Pantallas del prototipo

Son ocho pantallas: seis imprescindibles para la demo y dos deseables si sobra tiempo. Las del frigorífico van en escritorio o tablet; las del chofer, en celular.

| # | Pantalla | Usuario | Qué muestra | Acciones | Prioridad |
| --- | --- | --- | --- | --- | --- |
| 1 | Iniciar viaje | Chofer (celular) | Datos de la tropa del DT-e (origen, destino, cabezas) y botón grande "Iniciar viaje" | Escanear el DT-e o la caravana (NFC o QR) e iniciar | Imprescindible |
| 2 | Viaje en curso | Chofer (celular) | Semáforo grande, tiempo de viaje y aviso si hubo una frenada brusca o calor fuera de rango | Ninguna mientras maneja; "Llegué" al final | Imprescindible |
| 3 | Tropas entrantes | Recepción (frigorífico) | Lista de tropas en viaje y por llegar: transportista, origen, hora estimada, semáforo | Abrir una tropa | Imprescindible |
| 4 | Detalle de la tropa en viaje | Recepción y veterinario | Recorrido en mapa, línea de tiempo con eventos (frenadas, paradas), temperatura con franja permitida, horas de viaje | Ver eventos | Imprescindible |
| 5 | Recepción de la tropa | Recepción y veterinario | Caravanas leídas contra las esperadas del DT-e, animales caídos, m² por animal, checklist UE que se completa solo | Leer caravanas, marcar animal caído, confirmar recepción | Imprescindible |
| 6 | Informe y certificado UE | Exportación o calidad | Checklist UE con cumple o no cumple por ítem, índice de riesgo, QR del certificado | Descargar o compartir | Imprescindible |
| 7 | Certificado público | Comprador europeo | Versión de solo lectura del informe, sin login, abierta desde el QR | Ninguna | Deseable |
| 8 | Cierre con la res | Calidad | Hematomas y decomisos de la tropa contra su índice de riesgo; ranking de transportistas | Comparar tropas | Deseable |

Idioma de la interfaz: español para los usuarios argentinos; el certificado público (pantalla 7), en inglés para el comprador europeo.

## Índice de riesgo y semáforo

El índice es una suma de puntos por eventos, de 0 a 100: cualquiera del jurado puede entender por qué una tropa salió en rojo. Los puntos y umbrales son **valores iniciales propuestos por el equipo**, que se calibran después comparando con los hematomas reales en la res.

| Evento | Cuándo cuenta | Puntos | Máximo |
| --- | --- | --- | --- |
| Viaje largo | Más de 8 h de viaje | +20 | 20 |
| Viaje sin descanso | Más de 14 h sin parada de 1 h | +40 | 40 |
| Temperatura fuera de rango | Por cada hora fuera de 5–30 °C | +10 | 30 |
| Frenada brusca | Desaceleración mayor a 0,4 g (umbral a calibrar) | +5 cada una | 25 |
| Curva brusca | Aceleración lateral mayor a 0,3 g (umbral a calibrar) | +3 cada una | 15 |
| Espacio fuera de rango | m² por animal fuera del rango para su peso | +15 | 15 |
| Animal caído a la llegada | Cada animal marcado en la recepción | +20 cada uno | 40 |

El total se corta en 100.

- **Verde, 0 a 29:** la tropa viajó dentro de la norma.
- **Amarillo, 30 a 59:** revisar antes de faenar; prioridad en la recepción.
- **Rojo, 60 o más:** la tropa no cumple; evaluación veterinaria inmediata.

Regla aparte del puntaje: si un ítem obligatorio del Reg. 1099/2009 no se cumple (por ejemplo, un animal caído sin atender), el checklist marca **no cumple** aunque el puntaje sea bajo.

En el pitch se presenta como "índice por eventos, a calibrar con hematomas". No se lo llama "nivel de estrés" porque no medimos cortisol.

## Datos de ejemplo

Tres tropas ficticias, una por color del semáforo. La amarilla es la que se "vive" en la demo. Todos los nombres son inventados: no usar campos, transportistas ni frigoríficos reales.

| Dato | Tropa T-0417 (verde) | Tropa T-0418 (amarilla, demo en vivo) | Tropa T-0419 (roja) |
| --- | --- | --- | --- |
| Origen | Estancia El Cañadón, centro de Córdoba | Campo La Aguada, sur de Córdoba | Establecimiento Los Tres Ombués, oeste de Buenos Aires |
| Destino | Frigorífico Exportador Demo, Gran Córdoba | Frigorífico Exportador Demo, Gran Córdoba | Frigorífico Exportador Demo, Gran Córdoba |
| Transportista | Transportes Demo A | Transportes Demo B | Transportes Demo C |
| Cabezas y categoría | 34 novillos, \~450 kg | 36 novillos, \~450 kg | 38 novillos, \~470 kg |
| Superficie de la jaula | 52 m² | 52 m² | 52 m² |
| m² por animal | 1,53 (dentro de 1,3–1,6) | 1,44 (dentro de 1,3–1,6) | 1,37 (dentro de 1,3–1,6) |
| Distancia y tiempo de viaje | 140 km, 2 h 30 min | 230 km, 4 h 10 min | 610 km, 9 h 20 min |
| Temperatura máxima en ruta | 26 °C | 29 °C | 37 °C durante 2 h |
| Frenadas y curvas bruscas | 1 curva | 2 frenadas, 1 curva | 3 frenadas, 2 curvas |
| Animales caídos a la llegada | 0 | 1 (caravana 032 0000 0418 07) | 1 |
| Puntaje del índice | 3 | 33 | 81 |
| Checklist UE | Cumple | Cumple con observación (animal caído atendido) | No cumple (viaje de más de 8 h y temperatura fuera de rango) |

Cálculo del puntaje con las reglas de la sección anterior:

- **T-0417:** 1 curva (+3) = 3.
- **T-0418:** 2 frenadas (+10), 1 curva (+3), 1 animal caído (+20) = 33.
- **T-0419:** viaje de más de 8 h (+20), 2 h fuera de rango (+20), 3 frenadas (+15), 2 curvas (+6), 1 animal caído (+20) = 81.

El número de caravana tiene formato ilustrativo: el formato oficial de SENASA está por confirmar.

## Demo en vivo y pitch

### Guion de la demo (tropa T-0418)

1. **Carga:** el chofer escanea el DT-e o una caravana de juguete con NFC o QR y toca "Iniciar viaje". En el panel del frigorífico aparece la tropa como "en viaje".
2. **Viaje:** alguien mueve el celular (o un camión de juguete con el celular adentro) y simula una frenada brusca. En el panel aparece el evento en la línea de tiempo y el semáforo pasa a amarillo.
3. **Llegada:** en la recepción se leen las caravanas, el operario marca un animal caído y el checklist UE se completa solo.
4. **Informe:** se abre el informe con el checklist, el puntaje 33 y el QR. Alguien del jurado escanea el QR y ve el certificado en inglés en su propio celular.

Plan B: un video grabado de la misma demo, por si falla la conexión o el celular.

### Estructura del pitch

Sigue los siete puntos de la guía de la organización, con el peso de cada criterio del jurado. Ajustar los tiempos a la duración que confirme la organización.

| Bloque | Qué decimos | Criterio del jurado que suma |
| --- | --- | --- |
| Gancho | "Casi 6 de cada 10 bovinos llegan golpeados a faena, y nadie registra qué pasó en el viaje" (IPCVA) | Impacto (25 %) |
| Problema y a quién le pasa | El frigorífico exportador pierde carne y no puede demostrar bienestar animal ante la UE | Impacto (25 %) |
| Solución | Sin chips nuevos: caravana obligatoria + celular del chofer + registros de la planta | Innovación (20 %) |
| Demo en vivo | Los cuatro pasos del guion | Factibilidad (20 %), Pitch (10 %) |
| Qué la hace distinta | Los monitores actuales (collares, bolos) cubren el campo y el tambo; nadie cubre el viaje, y nosotros no agregamos hardware | Innovación (20 %) |
| Impacto | Menos carne perdida = menos huella desperdiciada; acceso a la UE con evidencia de bienestar | Impacto (25 %) |
| Escala y primer paso | Piloto con un frigorífico exportador de Córdoba; luego transportistas, feedlots y verificación de origen (EUDR) | Escalabilidad (15 %), Ecosistema (10 %) |

## Decisiones pendientes

- [ ] Nombre definitivo del producto ("Caja Negra Bovina" es nombre de trabajo).
- [ ] Guía de diseño: paleta, tipografía y logo (en curso, a cargo del equipo de diseño). El semáforo necesita verde, amarillo y rojo distinguibles también para daltónicos: sumar ícono o texto, no solo color.
- [ ] Cómo presentar el checklist del viaje: "referencia UE" o "anticipo de la norma que se viene".
- [ ] Lectura de caravana en la demo: NFC (solo Android con Chrome) o QR (cualquier celular). Depende de los celulares del equipo.
- [ ] Duración del pitch que fija la organización.
- [ ] Prototipo funcional en código o maqueta navegable (Figma). La pantalla 2 necesita código para leer el acelerómetro real.

## Fuentes

- [Respaldo oficial: bienestar animal en el transporte bovino y exportación a la UE](https://claude.ai/artifact/K8Q9roMxYoQBzZE4yBT29i) (todas las cifras y normas, con sus links)
- [Reglamento (CE) 1099/2009 (EUR-Lex)](https://eur-lex.europa.eu/legal-content/ES/TXT/HTML/?uri=CELEX:32009R1099)
- [Reglamento (CE) 1/2005 (EUR-Lex)](https://eur-lex.europa.eu/legal-content/ES/TXT/HTML/?uri=CELEX:32005R0001)
- [IPCVA, Cuadernillo Técnico Nº5 (2008)](https://www.produccion-animal.com.ar/informacion_tecnica/comercializacion/50-cuadernilllo_5.pdf)
- [Resolución SENASA 53/2017](https://www.boletinoficial.gob.ar/detalleAviso/primera/158733/20170207)
- [Resolución SENASA 841/2025](https://www.argentina.gob.ar/normativa/nacional/norma-419696/texto)
