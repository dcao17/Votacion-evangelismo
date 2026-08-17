# Votación de evangelismo

Aplicación web (una sola página HTML) para votar en equipo a dónde ir cada día
dentro del plan de evangelismo. Cada persona escribe su nombre y vota por uno
de los lugares programados para el mes; el lugar con más votos se destaca
como "el ganador del día", con confeti y todo.

## Uso

Abre `index.html` en el navegador. No requiere backend ni build: es HTML,
CSS y JavaScript puro en un solo archivo.

> **Nota:** el archivo usa `window.storage` para guardar los votos, una API
> disponible dentro del entorno de artefactos de Claude. Si vas a publicar
> este sitio de forma independiente (por ejemplo con GitHub Pages), necesitas
> reemplazar esa parte por tu propio backend o por almacenamiento en el
> navegador (`localStorage`) para que los votos se guarden.

## Estructura

- `index.html` — toda la aplicación (marcado, estilos y lógica).

## Personalizar los lugares

La lista de lugares vive en el arreglo `PLACES` dentro de `index.html`.
Cada elemento tiene:

- `mes` — bajo qué mes agrupar el lugar en la interfaz.
- `nombre` — nombre del lugar.
- `objetivo` — a qué se dedica la visita.
- `horario` — franja horaria sugerida.
- `cat` — categoría (`parque`, `ancianos`, `hospital` o `ninos`), usada para
  el ícono y la ilustración del ganador.
