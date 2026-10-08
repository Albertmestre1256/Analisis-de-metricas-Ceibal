# Mapa de archivos — Proyecto Ceibal
_Actualizado: 2026-10-08_

## Árbol completo

```
Proyecto - Ceibal/
├── Datasets & Metadatos/
│   ├── Dataset - Docentes/
│   │   ├── actividad-de-docentes-2024.csv
│   │   ├── actividad-de-docentes-2025.csv
│   │   ├── datos_docentes_2019.csv
│   │   ├── datos_docentes_2020.csv
│   │   ├── datos_docentes_2021.csv
│   │   ├── datos_docentes_2022.csv
│   │   └── docentes_datos_abiertos_agesic.csv
│   ├── Dataset - Estudiantes/
│   │   ├── actividad-de-estudiantes-2024.csv
│   │   ├── actividad-de-estudiantes-2025.csv
│   │   ├── datos_estudiantes_2019.csv
│   │   ├── datos_estudiantes_2020.csv
│   │   ├── datos_estudiantes_2021.csv
│   │   ├── datos_estudiantes_2022.csv
│   │   └── estudiantes_datos_abiertos_agesic.csv
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
│       └── Untitled.ipynb
├── Recursos/
│   ├── Dataset docentes concatenado/
│   │   └── dataset_docentes_consolidado.parquet
│   └── Dataset estudiantes concatenado/
│       └── dataset_estudiantes_consolidado.parquet
├── mapa-archivos.md
└── README.md
```

## Resumen por tipo

| Tipo | Archivos |
|---|---|
| Datos (.csv) | 16 |
| Notebooks (.ipynb) | 2 |
| Documentos (.md) | 2 |
| Datos (.parquet) | 2 |
| Metadatos (.pdf) | 2 |
| **Total** | **24** |

Se omiten carpetas y archivos ocultos (`.git`, `.gitignore`, `.ipynb_checkpoints`).

## Notas

- Datos crudos en `Datasets & Metadatos/` — conservar sin modificar.
- Datos procesados (Parquet consolidados) en `Recursos/`.
- Trabajo activo en `Proyecto/Etapa I` (completa) y `Etapa II`.
- El notebook de Etapa II aún no tiene nombre definitivo (`Untitled.ipynb`).
