Mapa vectorial usando datos procesados de BADATA y OSM. </br>
Usado para la base rasterizada de [https://github.com/f-ciampo/transit-map-demo/](https://github.com/f-ciampo/transit-map-demo/).

**veredas-2019.zip** y **parcelas-2019.zip**</br>
Datasets fuente de BA-DATA ([veredas](https://data.buenosaires.gob.ar/dataset/veredas); [parcelas](https://web.archive.org/web/20200709054813/https://data.buenosaires.gob.ar/dataset/parcelas)) </br>
Ambos son de 2019, ya que las primeras no se actualizan desde ese año, y los datos para las segundas empeoraron mucho en calidad a partir de 2020.

**veredasYParcelas.mbtiles** y **veredasYParcelas.pmtiles**</br>
mbtiles y pmtiles con dos capas vectoriales ('parcelas' y 'veredas') con los polígonos de ambas cosas en los niveles de zoom 15 a 18.</br>
Generado con [tippecanoe](https://github.com/mapbox/tippecanoe) y convertido con [pmtiles CLI](https://docs.protomaps.com/pmtiles/cli).</br>
Las veredas adyacentes fueron unidas (el original tiene un polígono de vereda por parcela, en vez de uno solo para toda una manzana).</br>
Como el único objetivo del mapa es visual, para reducir el tamaño se eliminaron los atributos de los polígonos, y los feature-ids son aleatorios (generados por tippecanoe).</br>
Se usó [QGIS](https://qgis.org/) para pre-procesar los datos.

Los [rasters](https://assets.transit.ar/caba-512.pmtiles) se generaron con [TileServer-GL](https://github.com/maptiler/tileserver-gl), usando un estilo creado en [Maputnik](https://github.com/maplibre/maputnik) para superponer las veredas y parcelas sobre datos de OSM.</br>
**TODO**: limpiar el style y publicarlo.
