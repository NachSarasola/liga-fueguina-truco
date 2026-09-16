# Liga Fueguina de Truco — tabla de posiciones

Una sola página (`index.html`) que muestra la tabla de posiciones de la liga con
tres vistas —Ushuaia, Río Grande y Provincial— y un panel de administración para
cargar los resultados. No necesita servidor, base de datos ni cuentas.

Demo en vivo: https://claude.ai/code/artifact/1d98de2a-d51c-4ffa-a67b-b64dfe7bc5ab

---

## 1. Publicarla

Subí `index.html` a cualquier hosting estático gratis. Tiene que quedar como
`index.html` en la raíz del sitio.

- **Netlify Drop** — https://app.netlify.com/drop — arrastrás el archivo y listo.
- **GitHub Pages** — subís `index.html` a un repo y activás Pages.
- **Cloudflare Pages**, **Vercel**, o el hosting que ya tengas.

Pasás ese link a los jugadores. Eso es todo lo que ven ellos.

## 2. Entrar al panel

`https://tu-sitio/#admin` — o el enlace **Panel** abajo de la tabla.

Contraseña inicial: **`truco2026`**

**Cambiala antes de entregar la página.** Panel → sección *Contraseña*. La nueva
contraseña se aplica cuando descargás y volvés a subir la página (paso 3).

> Aclaración de seguridad: la contraseña frena a un curioso, pero cualquiera que
> descargue el HTML puede leer su rastro. Para una liga alcanza; no la uses para
> nada sensible.

## 3. Cargar una fecha y publicarla

Cada sábado se juega una fecha: un mini torneo eliminatorio por sede. Lo único
que cargás es **qué le pasó a cada pareja** — el resultado ya trae los puntos
fijos de esa ronda.

1. Entrás al panel, sección *Resultado de la fecha*.
2. Elegís la sede.
3. Para cada pareja, elegís su resultado de hoy: Campeón, Subcampeón,
   Semifinalista, Cuartofinalista, Eliminado en 16avos, Eliminado en 32avos, o
   dejás "Sin cambios" si no jugó. Los puntos entre paréntesis se suman al
   acumulado de temporada — no lo reemplazan.
4. Botón **Aplicar resultados de esta fecha**.
5. Repetís para las otras dos sedes.
6. Actualizás el número de *Fecha* en la sección *Liga*.
7. Botón **Descargar página**.
8. Subís el `index.html` descargado a tu hosting, reemplazando el anterior.

Los cambios recién se ven cuando subís el archivo nuevo. Mientras tanto quedan
como *borrador* en tu navegador (botón **Guardar borrador**).

Los puntos por cada resultado (100 al campeón, 70 al subcampeón, etc.) se
cambian en *Liga → Puntos por resultado de fecha*, antes de aplicar la fecha.

## 4. Parejas

Sección *Parejas*: editás jugador 1 y jugador 2 de cada pareja, agregás o
quitás. El campo *Nombre o club* es opcional; si lo dejás vacío, la pareja se
muestra por los apellidos.

Para cargar las 32 de una: *Parejas → Importar lista*, una por línea con el
formato `Jugador 1; Jugador 2; nombre opcional`.

## 5. Datos de ejemplo

La página viene con 32 parejas y resultados ficticios, marcados con *"datos de
ejemplo"*. Cuando cargues los reales, destildá esa marca en *Liga → Mostrar la
marca "datos de ejemplo"*. Al importar la lista de parejas se saca sola.

## 6. Copia de seguridad

*Panel → Copia de seguridad*: **Exportar JSON** guarda todos los datos en un
archivo; **Importar JSON** los restaura. Conviene exportar de vez en cuando.

## Tabla y reglas

Columnas: `# · Pareja · FJ · Tít · Pts`. FJ es fechas jugadas, Tít es fechas
ganadas (campeonatos). Orden: puntos de temporada → fechas ganadas → finales
alcanzadas → semifinales alcanzadas → nombre.
