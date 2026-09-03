# ArbitrIA

**Panel de revisión por pares en un único fichero HTML.**
Herramientas IA para la academia · Universidad Miguel Hernández de Elche

ArbitrIA simula el proceso completo de revisión de una revista internacional: analiza el
campo del manuscrito, configura cuatro identidades revisoras editables, ejecuta cinco
asientos separados por rol que se comprometen sin ver los informes de los demás, y
produce una decisión editorial con su hoja de ruta de revisión.

## Fases

| Fase | Qué hace |
|---|---|
| 0 | Análisis de campo en seis dimensiones, revistas sugeridas y cuatro tarjetas de configuración de revisor, editables antes de ejecutar. |
| 1 | Cinco asientos en paralelo: encaje con la revista, metodología, dominio, perspectiva y abogado del diablo. |
| 2 | Síntesis editorial: consenso, desacuerdos arbitrados, adjudicación visible de cada problema CRITICAL, decisión y hoja de ruta inmutable. |
| 2.5 | Acompañamiento socrático de la revisión, solo preguntas, con triaje del autor en un anexo aparte. |

## Modos

Completa · rápida · foco metodológico · guiada · re-revisión con el contrato de tres
puertas (criterios congelados → veredicto de evidencia sin ver la carta de respuesta →
emparejamiento de afirmaciones).

## Reglas que la aplicación no se salta

- Los revisores no editan el manuscrito: solo producen informes.
- El sintetizador no inventa comentarios; todo se rastrea a un informe de la fase 1.
- Ningún problema CRITICAL del abogado del diablo se ignora en silencio.
- Los juicios son categorías ancladas en criterios (`EXCEEDS`, `MEETS`, `PARTLY_MEETS`,
  `DOES_NOT_MEET`, `NOT_ASSESSED`): no hay puntuación numérica, ranking ni probabilidad
  de aceptación.
- El manuscrito se trata como dato no fiable; las instrucciones incrustadas en él no se
  obedecen.

## Uso

Abre `index.html` en el navegador, pega tu clave de OpenAI (se guarda solo en
`localStorage`) y carga el manuscrito en PDF, DOCX, TXT o MD. Modelos disponibles:
`gpt-4o-mini`, `gpt-5.6-luna`, `gpt-5.6-terra` y `gpt-5.6-sol`, con escalonado por rol y
pista cross-model opcional para el Revisor 2. Exporta a Markdown, Word y JSON.

## Advertencia de método

Cinco personas distintas sobre el mismo modelo y el mismo proveedor no son cinco
revisores independientes: los errores sistemáticos del modelo aparecerán en varios
asientos y el consenso los amplificará. Todo informe declara `NOT_CALIBRATED`. Es un
simulacro para ensayar antes de enviar, nunca un sustituto de la revisión real ni una
predicción de su resultado.

## Licencia

MIT © Fernando Borrás Rocher — ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)
