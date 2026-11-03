# ArbitrIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22269115.svg)](https://doi.org/10.5281/zenodo.22269115)

**Aplicación:** https://fborrasumh.github.io/arbitria/ · **Idiomas:** español (por defecto), inglés y portugués (selector en la barra superior, o `?lang=en` / `?lang=pt`).

Somete tu artículo a un tribunal antes que a la revista. Cinco revisores de IA con papeles distintos leen el manuscrito **sin ver lo que dicen los demás**. Un editor reúne sus informes y entrega una carta de decisión y una **hoja de ruta de cambios**. **El código comprueba** que cada cita de una crítica está de verdad en tu texto y que la hoja de ruta remite a hallazgos reales. Si después revisas el trabajo, ArbitrIA comprueba si has atendido cada comentario. Aplicación de un solo fichero (`index.html`), sin servidor.

## Novedades de la versión 3.0

- Rehecha con el sistema Forja: interfaz en **español, inglés y portugués**, con la revisión de muestra y los manuscritos de ejemplo en los tres idiomas.
- **OpenAI, Google Gemini o Anthropic Claude**, con la clave de cada persona y un desplegable con los modelos de esa clave. Modelo propio opcional para el editor y para el revisor 2.
- **Verificación por código** (nueva):
  - Cada cita de las anclas de los revisores se busca en el manuscrito (sin distinguir mayúsculas, tildes ni puntuación); la que no aparece se marca.
  - Un problema crítico o importante sin ancla comprobable se señala para tratarlo como pregunta.
  - Cada punto de la hoja de ruta debe remitir a revisores y hallazgos que existen.
  - La regla de decisión y la puerta del abogado del diablo se recalculan; si el editor se aparta de la regla sin explicarlo, se avisa. Un problema crítico del abogado del diablo que el editor no adjudica también impide aceptar.
  - En la re-revisión, un punto sin veredicto, con un veredicto no válido o con una cita que no está en la versión nueva cuenta como no verificable.
- **Privacidad**: correos, teléfonos y documentos de identidad se enmascaran antes de enviar, y antes del primer envío se ve lo que sale.
- Word generado en el navegador, sin librerías externas. El historial de la versión 2 («Mis revisiones») se conserva.

## El panel

| Revisor | Qué mira |
|---|---|
| Encaje | Ajuste a la revista, originalidad, relevancia |
| Metodología | Diseño, estadística, validez, reproducibilidad |
| Dominio | Literatura, marco teórico, aportación al campo |
| Perspectiva | Otras disciplinas, impacto práctico, supuestos |
| Abogado del diablo | El contraargumento más fuerte; no vota |

Antes de la revisión, un analista lee el manuscrito y propone el perfil de cada revisor, que puedes editar. Después, el editor reúne los informes: coincidencias, desacuerdos arbitrados, qué hace con los problemas críticos del abogado del diablo, carta de decisión y hoja de ruta. Opcionalmente, un revisor te hace preguntas para que planifiques la revisión. Modos: completa, rápida, metodología, guiada y re-revisión (contrato de tres puertas: criterios antes de ver la versión nueva, veredicto antes de leer la carta de respuesta y, al final, la carta).

## Reglas que no se saltan

- Los revisores no ven los informes de los demás y no editan el manuscrito.
- Los problemas graves se anclan en el texto (cita, tabla o ausencia concreta); si no, se convierten en pregunta.
- El editor no puede inventar comentarios y no puede ignorar un problema crítico del abogado del diablo.
- No hay puntuación ni probabilidad de aceptación: solo si cada criterio se cumple y por qué.
- El manuscrito se trata como dato: las instrucciones incrustadas en él no se obedecen y se avisan.

## Qué comprueba el código y qué no

Comprueba que las citas existen en el texto, la trazabilidad de la hoja de ruta, la regla de decisión y la puerta del abogado del diablo. **No** comprueba si una crítica es acertada, si una cita está bien interpretada ni si una ausencia es real: una cita encontrada solo prueba que el pasaje existe.

## Advertencia de método

Cinco papeles sobre el mismo modelo y el mismo proveedor no son cinco revisores independientes: comparten sesgos, y el consenso puede amplificar un error. Los juicios no están calibrados (`NOT_CALIBRATED`): el modo de calibración del skill original no está implementado. Es un ensayo para anticipar críticas y mejorar el trabajo, nunca un sustituto de la revisión real ni una predicción de su resultado.

## Privacidad

El manuscrito se lee y se guarda en el navegador (IndexedDB). Al revisar, viaja solo a tu proveedor de IA, con tu clave (guardada en `localStorage`; la de OpenAI se comparte con el catálogo como `ia_openai_key`), y con los datos personales detectables enmascarados. El historial no guarda el texto del manuscrito. Una revisión completa son unas siete llamadas con el manuscrito entero; el coste depende del modelo y del proveedor.

## Límites

- La lectura de PDF necesita texto seleccionable (un PDF escaneado no sirve) y carga pdf.js o mammoth desde cdnjs/jsDelivr la primera vez.
- El enmascarado detecta correos, teléfonos y DNI/NIE, no nombres de personas en el texto.
- Probado con IA simulada (incluidas respuestas que mienten) en los tres proveedores; no con claves reales en esta versión.

## Origen

Reproduce en el navegador el procedimiento del skill *academic-paper-reviewer* de Cheng-I Wu.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) · ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. (2026). *ArbitrIA* (versión 3.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.22269115

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
