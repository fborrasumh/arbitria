# ArbitrIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22269115.svg)](https://doi.org/10.5281/zenodo.22269115)

**Aplicación:** https://fborrasumh.github.io/arbitria/

Somete tu artículo a un tribunal antes que a la revista. Cinco revisores de IA con papeles distintos leen el manuscrito **sin ver lo que dicen los demás**. Un editor reúne sus informes y entrega una carta de decisión y una **hoja de ruta de cambios**. Si después revisas el trabajo, ArbitrIA comprueba si has atendido cada comentario. Aplicación de un solo fichero (`index.html`), sin servidor.

## Novedades de la versión 2.0

- Recorrido guiado con el estilo de Forja: **Inicio → Manuscrito → Panel → Informes → Decisión**. Cada fase lleva a su pantalla.
- **Todo en castellano llano.**
  - La jerga interna del procedimiento se ha sustituido por explicaciones.
  - Las etiquetas se muestran en castellano: «Revisión mayor», «Cumple en parte», «Crítico», «Atendido en parte»…
  - Los revisores aparecen por su nombre, no por sus siglas.
  - Los prompts no cambian: la traducción se hace solo al mostrar y al exportar.
- **Modos explicados en tarjetas:** completa, rápida, metodología, guiada y re-revisión.
- **Ejemplos**: una revisión completa de muestra que se ve sin clave y dos manuscritos con fallos reales para probarla (un estudio cuasiexperimental y uno transversal).
- **Modelos económicos por defecto.** El editor usaba gpt-5.6-sol, el más caro; ahora todos usan gpt-6-luna, con los demás disponibles en los ajustes avanzados.
- **Corregido**: la re-revisión podía devolver «Aceptar» si el verificador no entregaba ningún veredicto. Ahora, sin veredictos, la decisión es «Lo decide una persona».
- **Corregido**: la exportación a Markdown y Word salía con las etiquetas en inglés.

## El panel

| Revisor | Qué mira |
|---|---|
| Encaje | Ajuste a la revista, originalidad, relevancia |
| Metodología | Diseño, estadística, validez, reproducibilidad |
| Dominio | Literatura, marco teórico, aportación al campo |
| Perspectiva | Otras disciplinas, impacto práctico, supuestos |
| Abogado del diablo | El contraargumento más fuerte; no vota |

Antes de la revisión, un analista lee el manuscrito y propone el perfil de cada revisor, que puedes editar. Después, el editor reúne los informes: coincidencias, desacuerdos arbitrados, qué hace con los problemas críticos del abogado del diablo, carta de decisión y hoja de ruta. Opcionalmente, un revisor te hace preguntas para que planifiques la revisión.

## Reglas que no se saltan

- Los revisores no ven los informes de los demás y no editan el manuscrito.
- Los problemas graves se anclan en el texto (cita, tabla o ausencia concreta); si no, se convierten en pregunta.
- El editor no puede inventar comentarios y no puede ignorar un problema crítico del abogado del diablo.
- No hay puntuación ni probabilidad de aceptación: solo si cada criterio se cumple y por qué.
- El manuscrito se trata como dato: las instrucciones incrustadas en él no se obedecen y se avisan.
- En la re-revisión, los criterios se fijan antes de ver la versión nueva y la carta de respuesta solo se lee al final.

## Advertencia de método

Cinco papeles sobre el mismo modelo y el mismo proveedor no son cinco revisores independientes: comparten sesgos, y el consenso puede amplificar un error. Es un ensayo para anticipar críticas y mejorar el trabajo, nunca un sustituto de la revisión real ni una predicción de su resultado.

## Origen

Reproduce en el navegador el procedimiento del skill *academic-paper-reviewer* de Cheng-I Wu.

## Privacidad

El manuscrito se lee en el navegador y solo viaja a OpenAI con la clave del usuario, guardada en `localStorage` (`ia_openai_key`). Las revisiones se guardan en IndexedDB del navegador, sin el texto del manuscrito.

## Cómo citar

Borrás Rocher, F. (2026). *ArbitrIA* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.22269115

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
