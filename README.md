# Datos públicos de TD10 Programación

Repositorio independiente de datos sintéticos y material abierto para clases de Python. La fuente activa de la semana 8 se controla desde un panel local del docente y se publica en GitHub mediante commits.

## Fuente activa

- `datos/registros.json`: atenciones ficticias con `codigo`, `fecha`, `sede`, `hospital`, `paciente_id`, `paciente_nombre`, `paciente_cedula`, `grupo_edad`, `diagnostico`, `canal`, `estado` y una lista `medicamentos`.
- `datos/equivalencias.json`: reglas para reunir variantes bajo una clave común. Tanto las claves como los valores están en minúsculas; el programa estudiantil aplica `strip().casefold()` antes de consultarlas.

La clase comienza con dos registros. El docente puede ampliar la fuente a 3, 10, 20, 50 y 100, agregar o editar registros y publicar cada cambio. La URL permanece estable; el historial Git permite revisar cada versión. El estudiantado solo lee los JSON públicos y vuelve a ejecutar su programa para observar el cambio.

URLs de lectura mediante la API de contenidos de GitHub:

```text
https://api.github.com/repos/amenaactppp/td10-datos-publicos/contents/datos/registros.json?ref=main
https://api.github.com/repos/amenaactppp/td10-datos-publicos/contents/datos/equivalencias.json?ref=main
```

La solicitud usa `Accept: application/vnd.github.raw+json` para recibir JSON directamente. El programa de clase incluye la lectura por API y copias locales de respaldo. La fuente pública no requiere credenciales de estudiante. Evite consultas continuas: basta con ejecutar de nuevo después de una publicación.

Los códigos y nombres de paciente son inventados. `paciente_cedula` usa el prefijo `FIC-` y seis dígitos, un formato deliberadamente distinto de una cédula real. Un mismo paciente conserva nombre y cédula cuando aparece en varias atenciones; esto permite distinguir registros de pacientes distintos. Los nombres de medicamentos son datos de práctica para lectura de JSON, ciclos y diccionarios contadores. Su coincidencia con un diagnóstico no representa una prescripción ni una recomendación médica.

## Organización futura

- `datos/`: conjuntos sintéticos versionados y documentados.
- `materiales/`: guías públicas que se decida compartir.
- `fuentes/`: documentación de origen y permisos de datos externos.

Una actividad futura puede estudiar web scraping. Antes de incorporar una fuente externa, se documentarán su origen, licencia, condiciones de uso y método de obtención.

## Licencia

El código y la documentación de este repositorio se distribuyen bajo MIT. Los datos sintéticos de clase se ofrecen bajo CC0 1.0. Las fuentes externas conservarán sus propios términos.
