# Final Project – One Anomaly, Defended

## Team
- Felipe Alonso
- Juan Costa

## Repository
[https://github.com/juancostalarrain-netizen/-iele756-Quilicura-La-Reina-Tiltil](https://github.com/juancostalarrain-netizen/-iele756-Quilicura-La-Reina-Tiltil)

## Video
[AGREGAR LINK AL VIDEO]

---

# Anomaly

Nuestra anomalía consiste en que Tiltil (código 13125) presenta una tasa de egresos hospitalarios (GRD) de **69.79 por 10.000 habitantes**, prácticamente idéntica a su tasa de notificaciones ENO (77.42 por 10k), resultando en un cociente GRD/ENO de 0.9.

Esperábamos un cociente GRD/ENO de entre 7 y 20 (rango observado en el resto de la Región Metropolitana), pero observamos un valor de 0.9 — estructuralmente imposible bajo funcionamiento normal del sistema de salud, ya que los egresos hospitalarios siempre superan ampliamente a las notificaciones de enfermedades de declaración obligatoria.

Las comunas principales involucradas son:
- Tiltil (13125) — la anomalía
- Quilicura (13122) — referencia, cociente GRD/ENO ≈ 8.8
- La Reina (13109) — referencia, cociente GRD/ENO ≈ 7.0

La figura principal se encuentra en:
`figs/headline.png`

El notebook que la genera es:
`notebooks/final_anomaly.ipynb`

---

# Repository Structure

```
your-repo/
  README.md
  requirements.txt
  notebooks/
    tarea0.ipynb                (carry forward, no edits required)
    tarea1.ipynb
    tarea2.ipynb
    tarea3.ipynb
    final_anomaly.ipynb         (NEW)
  data/                         (paths or download script; do
                                 NOT commit large parquet/zip)
  figs/
    headline.png                (the figure used in your video)
    fig1_correlation_heatmap.png
    fig2_scatter_multiples.png
    fig3_ols_diagnostics.png
    fig4_predicted_rate_map.png
    fig5_residual_map.png
    fig6_coefficient_plot.png
```

---

# How to Run

```bash
# 1. Clonar el repositorio
git clone <URL_DEL_REPO>
cd <nombre-repo>

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar el notebook del proyecto final
jupyter notebook notebooks/final_anomaly.ipynb
```

`notebooks/final_anomaly.ipynb` carga la tabla pre-computada `output/tarea3_analytical_table.csv` generada por `notebooks/tarea3.ipynb` y regenera `figs/headline.png` en menos de 1 minuto.

Para regenerar desde cero: ejecutar `notebooks/tarea3.ipynb` primero (~5–10 min), luego `notebooks/final_anomaly.ipynb`.

---

# AI Use Disclosure

Utilizamos **Claude (Anthropic)** como herramienta de asistencia durante el proyecto:

- **Depuración de código**: errores en joins con GeoPandas (proyecciones CRS, merge por nombre normalizado).
- **Redacción del README**: borrador inicial revisado y corregido por ambos integrantes.
- **Estructura de `final_anomaly.ipynb`**: sugerencia de la estructura de secciones; el código y el análisis fueron revisados, ejecutados y validados por el equipo.
- **Identificación de la anomalía**: Claude señaló el patrón del cociente GRD/ENO como eje central del análisis; la interpretación causal y los chequeos de hipótesis alternativas fueron desarrollados por el equipo.
- **Organización del repositorio GitHub**: Claude reorganizó la estructura de carpetas, renombró los notebooks a nombres canónicos (tarea0–tarea3, final_anomaly), movió los archivos a las carpetas correctas (notebooks/, figs/, output/, data/) y realizó el commit y push al repositorio remoto.

Toda afirmación numérica y causal es responsabilidad de Felipe Alonso y Juan Costa.
