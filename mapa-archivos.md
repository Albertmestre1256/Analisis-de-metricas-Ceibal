# Mapa de archivos — Proyecto - Ceibal

Generado el 15/10/2026 (America/Montevideo). Excluye carpetas y archivos ocultos (`.git`, `.ipynb_checkpoints`, etc.).

## Árbol

```
Proyecto - Ceibal/
├── README.md
├── mapa-archivos.md
├── Datasets & Metadatos/                      (fuente cruda: no modificar)
│   ├── Dataset - Docentes/
│   │   ├── datos_docentes_2019.csv
│   │   ├── datos_docentes_2020.csv
│   │   ├── datos_docentes_2021.csv
│   │   ├── datos_docentes_2022.csv
│   │   ├── docentes_datos_abiertos_agesic.csv       (año 2023)
│   │   ├── actividad-de-docentes-2024.csv
│   │   └── actividad-de-docentes-2025.csv
│   ├── Dataset - Estudiantes/
│   │   ├── datos_estudiantes_2019.csv
│   │   ├── datos_estudiantes_2020.csv
│   │   ├── datos_estudiantes_2021.csv
│   │   ├── datos_estudiantes_2022.csv
│   │   ├── estudiantes_datos_abiertos_agesic.csv    (año 2023)
│   │   ├── actividad-de-estudiantes-2024.csv
│   │   └── actividad-de-estudiantes-2025.csv
│   ├── Metadatos - Docentes/
│   │   ├── metadatos_actividad_docente.csv
│   │   └── metadatos_actividad_docente.pdf
│   └── Metadatos - Estudiantes/
│       ├── metadatos_actividad_estudiante.csv
│       └── metadatos_actividad_estudiante.pdf
├── Proyecto/
│   ├── Etapa I - Convertir los datasets en Parquet/
│   │   └── Concatenación de datos.ipynb
│   └── Etapa II - Exploración primaria + Limpieza/
│       ├── EDA - Docentes.ipynb
│       └── EDA - Estudiantes.ipynb
└── Recursos/
    ├── Dataset docentes concatenado/
    │   └── dataset_docentes_consolidado.parquet
    └── Dataset estudiantes concatenado/
        └── dataset_estudiantes_consolidado.parquet
```

## Resumen

- **Total:** 25 archivos en 12 carpetas, incluida la raíz (el conteo incluye `README.md` y este mapa).
- **Por tipo:** 16 `.csv`, 2 `.pdf`, 2 `.parquet`, 3 `.ipynb`, 2 `.md`.
- **Carpetas principales:** `Datasets & Metadatos/` (datos crudos y metadatos, ≈502 MB), `Proyecto/` (un notebook por etapa; la Etapa II tiene uno por dataset), `Recursos/` (Parquet consolidados, ≈60 MB: docentes ≈3,5 MB y estudiantes ≈58,9 MB).

## Notas

- Los CSV de 2019–2022 llevan el patrón `datos_<dataset>_<año>.csv`; los de 2024 y 2025, `actividad-de-<dataset>-<año>.csv`. El de 2023 se llama `*_datos_abiertos_agesic.csv`.
- Los metadatos (CSV y PDF) no indican el año al que corresponden.
- La Etapa II se dividió en dos notebooks: `EDA - Docentes.ipynb` (en curso, 62 celdas) y `EDA - Estudiantes.ipynb` (recién creado: 6 celdas, con importaciones y carga del Parquet). Antes había un único `EDA y limpieza de datos.ipynb`, que ya no está en la carpeta.
- Todavía no existen `docentes_limpio.parquet` ni `estudiantes_limpio.parquet`: son los productos pendientes de la Etapa II.
