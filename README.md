# Análisis del Impacto de la Actividad Industrial Automotriz en la Concentración de Contaminantes Atmosféricos PM2.5, PM10 y O₃ en Saltillo
### Con datos históricos del periodo 2019–2022

> Investigación académica — Seminario de Investigación · Universidad Autónoma de Coahuila

---

## Descripción

Este repositorio contiene el código y la documentación de una investigación que analiza si existe una correlación estadísticamente significativa entre la actividad industrial del clúster automotriz de Saltillo (medida en horas-hombre trabajadas, subsector 336 EMIM-INEGI) y la concentración de contaminantes atmosféricos PM2.5, PM10 y O₃ registrados por la estación Finanzas del SINAICA.

Se aplicó el coeficiente de correlación de Pearson y regresión lineal simple con Python. Los resultados muestran correlaciones débiles y estadísticamente no significativas para el período analizado.

---

## Estructura del repositorio

```
/
├── analisis_calidad_aire.ipynb   # Script principal de análisis en Python
├── README.md                     # Este archivo
├── .gitignore                    # Archivos excluidos del repositorio
└── docs/                         # Documentación de la investigación (tesina)
```

---

## ⚠️ Datos — Descarga manual requerida

Los archivos de datos **no están incluidos** en este repositorio porque pertenecen a instituciones públicas del gobierno mexicano y deben descargarse directamente desde sus fuentes oficiales. Son de acceso público y gratuito.

Debes descargar los archivos y colocarlos en la misma carpeta que el notebook antes de ejecutarlo.

---

### Fuente 1 — SINAICA (Calidad del Aire)

**Institución:** Instituto Nacional de Ecología y Cambio Climático (INECC) · SEMARNAT  
**URL:** https://sinaica.inecc.gob.mx/data.php?tipo=V

**Pasos para descargar:**
1. Entra al enlace anterior
2. Selecciona **Estación: Finanzas** (Saltillo, Coahuila)
3. Selecciona los parámetros: **PM2.5, PM10, O3**
4. Selecciona el rango de fechas: **noviembre 2019 – agosto 2022**
5. Descarga el archivo en formato `.xlsx`
6. Guárdalo en la carpeta del proyecto

---

### Fuente 2 — EMIM (Actividad Industrial)

**Institución:** Instituto Nacional de Estadística y Geografía (INEGI)  
**URL:** https://www.inegi.org.mx/programas/emim/2013/#datos_abiertos

**Pasos para descargar:**
1. Entra al enlace anterior
2. Descarga la serie mensual de la **Encuesta Mensual de la Industria Manufacturera (EMIM)**
3. El archivo contiene la variable **HH\_T1** (Horas-Hombre Trabajadas)
4. Filtra por **Subsector 336** (Fabricación de equipo de transporte) y **Coahuila de Zaragoza**
5. Guárdalo en la carpeta del proyecto

---

## Cómo ejecutar

1. Clona este repositorio:
```bash
git clone https://github.com/TU_USUARIO/TU_REPOSITORIO.git
cd TU_REPOSITORIO
```

2. Descarga los archivos de datos siguiendo las instrucciones anteriores

3. Abre el notebook:
```bash
jupyter notebook analisis_calidad_aire.ipynb
```

4. Ejecuta las celdas en orden — el notebook instala las dependencias necesarias automáticamente

---

## Metodología

| Elemento | Detalle |
|---|---|
| Tipo de investigación | Correlacional, no experimental, longitudinal |
| Periodo de análisis | Noviembre 2019 – Agosto 2022 |
| Criterio de cobertura | Meses con al menos 75% de datos válidos |
| Muestra | 19 meses-estación |
| Variable independiente | Horas-Hombre Trabajadas (HH\_T1), Subsector 336, Coahuila |
| Variables dependientes | PM2.5, PM10, O₃ (µg/m³) — Estación Finanzas, Saltillo |
| Análisis estadístico | Coeficiente de Pearson r, p-valor, Regresión lineal R² |
| Escala de interpretación | Débil < 0.4 · Moderada 0.4–0.7 · Fuerte ≥ 0.7 |

---

## Resultados principales

| Correlación | r | p-valor | Intensidad | Significativa |
|---|---|---|---|---|
| Horas vs PM2.5 | 0.099 | 0.686 | Débil | No |
| Horas vs PM10 | 0.278 | 0.249 | Débil | No |
| Horas vs O₃ | 0.364 | 0.127 | Débil | No |

La hipótesis H1 (r > 0.70, p < 0.05) no fue confirmada. El aporte principal es el protocolo metodológico replicable para cruzar datos SINAICA + EMIM en cualquier ciudad industrial de México.

---

## Licencia

El código de este repositorio se distribuye bajo licencia **MIT**. Los datos utilizados pertenecen a sus respectivas instituciones públicas (INECC-SEMARNAT e INEGI) y están sujetos a sus propias condiciones de uso.

---

*Universidad Autónoma de Coahuila · Seminario de Investigación · 2024–2025*
