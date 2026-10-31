# Datos públicos de TD10 Programación

Repositorio independiente para publicar **datos sintéticos y material abierto**
que se consulta desde las clases de Python. La primera fuente corresponde a
la semana 8, «El informe que cambió».

## Fuente disponible

`datos/registros.json` contiene registros ficticios con `codigo` y una lista de
`medicamentos`. No hay nombres, cédulas ni datos de pacientes reales. Los
nombres sirven para practicar lectura de JSON, ciclos y conteos; las cifras
representan menciones en los registros, no indicaciones médicas.

URL de lectura mediante la API de contenidos de GitHub:

```text
https://api.github.com/repos/amenaactppp/td10-datos-publicos/contents/datos/registros.json?ref=main
```

Para recibir el contenido del archivo como JSON sin decodificar Base64, enviar
la cabecera `Accept: application/vnd.github.raw+json`. El programa de clase
incluye esta lectura y una copia local de respaldo. No requiere token para
este repositorio público.

## Organización futura

- `datos/`: conjuntos sintéticos versionados y documentados.
- `materiales/`: guías públicas que se decida compartir más adelante.
- `fuentes/`: documentación de origen y permisos de cualquier dato externo.

Una actividad futura puede estudiar **web scraping**, pero este repositorio no
incluye extractores ni datos de terceros. Antes de incorporar una fuente real,
se documentarán su origen, licencia, condiciones de uso y método de obtención.

## Actualización de la fuente

La semana 8 usa dos escenas. El docente prepara la segunda versión por fuera de
este repositorio; durante la clase actualiza `datos/registros.json` mediante un
commit. La URL permanece igual, y el historial Git muestra la diferencia.

## Licencia

El código y la documentación creados para este repositorio se distribuyen bajo
MIT. Los datos sintéticos creados para la clase pueden reutilizarse bajo CC0
1.0. Las futuras fuentes externas deberán conservar sus propios términos.
