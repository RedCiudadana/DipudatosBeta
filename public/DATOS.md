# Datos

Los datos que alimentan el sitio provienen de un [Google spreadseet](https://docs.google.com/spreadsheets/d/1haid-rjQqAY62soTzOupd-caDMo--QJBgaWkpimxiM8/pubhtml).

Este spreadhseet se vuelca en archivos JSON estáticos dentro de [`static-files`](static-files)
que están a disposición para consumo.

### Consumo

Se recomienda consumir los archivos a través de [RawGit](https://rawgit.com), un
servicio que devuelve correctamente el `Content-Type` del contenido.

Por ejemplo, en lugar de consumir directamente el archivo [`perfil.json`](static-files/perfil.json),
este se puede consumir por medio de RawGit con [esta URL para desarrollo](https://rawgit.com/RedCiudadana/Dipudatos/gh-pages/static-files/perfil.json)
y [esta URL para producción](https://cdn.rawgit.com/RedCiudadana/Dipudatos/gh-pages/static-files/perfil.json).

### Archivos de datos

Los principales archivos de datos disponibles son:

##### [`perfil.json`](static-files/perfil.json)

Este archivo contiene los datos para el principal concepto a manejar dentro del sitio:
los perfiles de los diputados. Acerca de estos se cuenta, por ejemplo, con la siguiente
información: `id`, `nombre`, `fotoUrl`, `profesion`, `educacion` (con estructura HTML), `fechaNacimiento`
(yyyy-mm-dd), `partidoPostulante` (llave), `partidoActual` (llave), `biografía` (con
estructura HTML), `planTrabajo` (con estructura HTML).

##### [`partido.json`](static-files/partido.json)

Se cuenta también con la información de los partidos existentes dentro del Congreso,
con información tal como `id`, `nombreCompleto`, `email`, `telefono`, `noDeAfilados`.

##### [`comision.json`](static-files/comision.json)

Cuenta con la información de las comisiones existentes en el Congreso,
con información tal como: `id`, `nombreCompleto`, `sede`.

##### [`distrito.json`](static-files/distrito.json)

Cuenta con la información de los distritos existentes en el Congreso,
con información tal como: `id`, `nombreCompleto`.

##### [`diputado-comision.json`](static-files/diputado-comision.json)

Cuenta con la información de la relación entre diputados (perfiles) y comisiones. Cuenta con
los campos: `perfil` (llave) y `comision` (llave).

##### [`sesion.json`](static-files/sesion.json)

Cuenta con la información de los distritos existentes en el Congreso,
con información tal como: `id`, `fecha` y `tipo` (ordinaria o extraordinaria).

##### [`asistencia.json`](static-files/asistencia.json)

Cuenta con la información de la relación entre diputados (perfiles) y sesiones. Cuenta con
los campos: `perfil` (llave) y `sesion` (llave).
