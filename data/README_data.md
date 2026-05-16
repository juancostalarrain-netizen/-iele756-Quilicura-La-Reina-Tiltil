# Datos del Proyecto

Los archivos de datos originales **no están incluidos en el repositorio** por tamaño.

## Fuentes

| Dataset | Archivo | Fuente |
|---|---|---|
| Censo 2024 | `viv_hog_per_censo2024/*.parquet` | INE – microdatos censo |
| ENO 2007–2022 | `20241218_base_eno_final.csv` | MINSAL |
| GRD 2019–2024 | `GRD_PUBLICO_XXXX.zip` | MINSAL/Fonasa |
| Shapefile comunas | `Comunas/comunas.shp` | INE |

## Para reproducir

Con los archivos en `output/` (incluidos en el repo) alcanza para ejecutar `notebooks/final_anomaly.ipynb`.

Para regenerar desde cero, se necesitan los archivos de `shared/` (CSVs procesados por cada equipo de la clase) y los datos crudos anteriores.
