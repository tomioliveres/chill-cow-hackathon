# Decisiones y datos — Chill Cow

Registro de lo que se decidió el 12/11/2026 y por qué. Si algo cambia, agregalo acá con fecha.

## Producto y alcance

| Decisión | Por qué |
|---|---|
| No fabricar chip ni dispositivo nuevo para el animal. | Regla del mentor: usar lo que el animal y la cadena ya tienen. |
| Medir con la caravana electrónica obligatoria (leída por NFC) + celular del chofer + DT-e + cámara de descarga + registros de hematomas en la res. | La identificación electrónica SENASA es obligatoria desde el 1/1/2026 al destete (Res. 530/2025 y 841/2025). Una caravana pasiva solo da identidad en puntos de lectura: temperatura, golpes y caídas salen del entorno (camión, corrales, manga, cámaras) o de la res. |
| Alcance: solo bienestar animal en el transporte, del campo a la planta. | Foco para la demo. Cría, feedlot y deforestación (EUDR) quedan como escalabilidad. |
| Cliente y pagador: frigorífico exportador que absorbe el costo del estrés (es dueño del animal al faenar y exporta a mercados que castigan el corte oscuro). | Es quien pierde plata y quien necesita demostrar cumplimiento ante la UE. Se excluye el modelo matarife-abastecedor. |
| Nombre: **Chill Cow**. | Decidido el 12/11. |
| Índice de bienestar por tropa, 0–100, con sub-índices Accidentes y Condiciones del viaje. Nunca "estrés". | Lenguaje positivo y medible con los datos disponibles. |
| El informe muestra dos veredictos: Reg. (CE) 1099/2009 (vinculante) y Reg. (CE) 1/2005 (referencia). | El 1099/2009 art. 12 aplica a importaciones desde la llegada a la planta. El 1/2005 de transporte solo rige dentro de la UE; se usa como benchmark. |
| Hablar de "merma" en lugar de huella de carbono. | Pedido del mentor: los datos de carbono disponibles son débiles; la merma está respaldada (IPCVA 1,37 kg/animal; CFI 2–10 % de peso vivo según distancia). |
| Cuando el índice es < 70, las pantallas 5 y 6 muestran un "protocolo de recuperación en corral" recomendado (feromona, con advertencias de SENASA y veterinario). | Pedido del mentor: que el sistema proponga una acción, no solo un número. |
| Prototipo = HTML clickeable, sin código funcional (NFC y acelerómetro simulados). | Tiempo de hackathon. |

## Datos verificados para el pitch

**Golpes y pérdidas**
- IPCVA, Cuadernillo Técnico Nº 5 (mayo 2008, UNICEN, Frigorífico Gorina, 15.361 animales, datos 2006): 58,8 % con al menos una lesión, ~1,37 kg perdidos por animal, US$ 3,15/animal, US$ 42,4 M/año a nivel nacional. Es el origen del "casi 6 de cada 10 animales golpeados".
- Córdoba 2011–12: 86 % de reses con hematomas.
- Uruguay, INIA/INAC, 4ª auditoría (2023): 76,5 % de reses con hematomas; los hematomas cuestan US$ 5,56/animal = 31 % de las pérdidas (⇒ ~US$ 18/animal en total, **dato derivado**); pH alto 3,4 % (9 % en 2013).
- Descuento por corte oscuro (USDA): US$ 30–55/cwt, promedio ~38 ⇒ ~15–20 % del valor de la res (**derivado**).
- **No usar:** "20 % de las pérdidas de calidad" y "+40 % de lesiones" (no se encontró fuente).

**Mercado**
- Argentina: ~25 exportadores (Consorcio ABC) = 39–41 % de la faena.
- Uruguay: 31 plantas (2,4 M de cabezas en 2025). Paraguay: 12–13 plantas ≈ 85 %. Brasil: ~62–73 plantas habilitadas para exportar.
- Grupos regionales (JBS, Minerva, Marfrig) operan en varios países: vía de escalabilidad.

**Feromona (protocolo de recuperación)**
- FerAppease ~US$ 3/cabeza, distribuida en Argentina por Biogénesis Bagó (marzo 2026). Registro SENASA **no verificado**.
- Evidencia: baja el cortisol de forma consistente; en un estudio de transporte el riesgo de DFD bajó de 42,2 % a 26,2 %; en otro, sin efecto. No hay ensayo independiente sobre golpes. Presentarlo como recomendación, no como promesa.

Citar los datos uruguayos como regionales y marcar los derivados como tales.

## Pitch

- Pitch de 3 minutos el 13/11 a las 10:45. Requisitos de la organización en `pitch/Hack to the Future - PITCH.pdf`: 7 bloques, mostrar equipo, persona real y "qué aprendimos".
- La demo del viaje en vivo (~125 s) no entra en 3 minutos: se usan los atajos `#paso-N` del prototipo.
- El jurado escanea el QR del informe: el link del prototipo (`#cert`) tiene que estar compartido públicamente antes del pitch.
