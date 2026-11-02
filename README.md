# Free Market en vivo

Ofertas del Free Market que va leyendo MSCE (MapleStory Market Scanner), en tiempo real.

La página lee una tabla de Supabase con la clave publicable, que solo permite leer. MSCE sube las ofertas con su propia clave de escritura, que no está en este repositorio.

Se publica con GitHub Pages: Settings → Pages → Deploy from a branch → `main`, carpeta `/ (root)`.

## Qué muestra

- Filtros por tipo de equipo (armas, armadura, accesorios y cada tipo), clase y rango de nivel, además de la búsqueda por ítem, jugador o tienda.
- Cada columna de las tablas se ordena con un clic en su encabezado (nivel, precio, ofertas, vendidos...).
- La página de cada ítem pide su historial completo a la base y dibuja la curva de precio: mediana y mínimo en venta por hora o por día, cada copia vista y las ventas en verde, con rangos de 24 h, 7 días, 30 días y todo.
- `catalog.json` trae el tipo, nivel y clase de cada equipo (del catálogo del juego de MSCE).
- Una venta (fila gris) que se vio en varias visitas cuenta una sola vez (jugador, ítem, precio, cantidad y posición).
- Los precios absurdos (más de 20 veces la mediana) se dejan fuera de los promedios y de la curva solo en consumibles y otros ítems sin estadísticas; el equipo nunca se recorta, porque con mejoras perfectas puede valer 100 veces más.
- Pestaña "Ofertas baratas": ofertas de las últimas 24 h con 20% o más de descuento contra la mediana de la última semana. En consumibles la referencia son ofertas y ventas; en equipo, solo ventas reales (8 o más), porque su precio depende de las estadísticas.
- "Cambio 24 h" en "Precios por ítem": mediana de las últimas 24 h contra las 24 h anteriores (hace falta al menos 3 precios en cada ventana).
- Pestaña "Más vendidos": ventas (filas grises, una vez cada una) por ítem con cantidad de ventas, unidades, mesos movidos, su porcentaje del total y la mediana de venta; se ordena por cualquier columna.
- Pestaña "Salud de los datos": filas cargadas, horas cubiertas, ventas sin repetir, porcentaje de equipo con estadísticas completas (en venta y vendido), filas sin mundo, sala o canal, y filas y jugadores por canal y por versión de MSCE.

- El enlace guarda la pestaña y la búsqueda (`#tab=prices&q=Gaia`), así se puede compartir un filtro.

- Alertas de precio: cada alerta guarda un ítem y un precio máximo por unidad en tu navegador, y la página lista las ofertas que la cumplen.
