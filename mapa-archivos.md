# Mapa de archivos — Proyecto - Ceibal

Generado: 20/10/2026 (carpeta conectada `Proyecto - Ceibal/`, sin carpetas ocultas ni `.git`).

## Árbol

```
Proyecto - Ceibal/
├── Datasets & Metadatos/
│   ├── Dataset - Docentes/
│   │   ├── actividad-de-docentes-2024.csv (3.1 MB)
│   │   ├── actividad-de-docentes-2025.csv (8.8 MB)
│   │   ├── datos_docentes_2019.csv (2.8 MB)
│   │   ├── datos_docentes_2020.csv (2.9 MB)
│   │   ├── datos_docentes_2021.csv (3.0 MB)
│   │   ├── datos_docentes_2022.csv (3.0 MB)
│   │   └── docentes_datos_abiertos_agesic.csv (3.3 MB)
│   ├── Dataset - Estudiantes/
│   │   ├── actividad-de-estudiantes-2024.csv (66.5 MB)
│   │   ├── actividad-de-estudiantes-2025.csv (62.1 MB)
│   │   ├── datos_estudiantes_2019.csv (69.3 MB)
│   │   ├── datos_estudiantes_2020.csv (71.2 MB)
│   │   ├── datos_estudiantes_2021.csv (71.2 MB)
│   │   ├── datos_estudiantes_2022.csv (68.8 MB)
│   │   └── estudiantes_datos_abiertos_agesic.csv (65.7 MB)
│   ├── Metadatos - Docentes/
│   │   ├── metadatos_actividad_docente.csv (5 KB)
│   │   └── metadatos_actividad_docente.pdf (53 KB)
│   └── Metadatos - Estudiantes/
│       ├── metadatos_actividad_estudiante.csv (11 KB)
│       └── metadatos_actividad_estudiante.pdf (63 KB)
├── Proyecto/
│   ├── Etapa I - Convertir los datasets en Parquet/
│   │   └── Concatenación de datos.ipynb (10 KB)
│   └── Etapa II - Exploración primaria + Limpieza/
│       ├── EDA - Docentes.ipynb (284 KB)
│       └── EDA - Estudiantes.ipynb (2 KB)
├── Recursos/
│   ├── Dataset docentes concatenado/
│   │   └── dataset_docentes_consolidado.parquet (3.3 MB)
│   ├── Dataset docentes limpio/
│   │   └── docentes_limpio.parquet (3.2 MB)
│   ├── Dataset estudiantes concatenado/
│   │   └── dataset_estudiantes_consolidado.parquet (56.1 MB)
│   └── Dataset estudiantes limpio/
├── mapa-archivos.md (3 KB)
└── README.md (13 KB)
```

## Resumen

Archivos: 26.

- .csv: 16
- .ipynb: 3
- .parquet: 3
- .md: 2
- .pdf: 2

Carpetas principales: `Datasets & Metadatos/` (fuente cruda, no modificar), `Proyecto/` (notebooks por etapa), `Recursos/` (Parquet consolidados y limpios).

## Notas

- `Recursos/Dataset estudiantes limpio/` está vacía en esta carpeta.
- En `Proyecto/Etapa II…/` no hay módulos auxiliares: el notebook de docentes importa `utilidades_eda.py` y no lo encuentra en esta carpeta.
