# Mapa de archivos — Proyecto - Ceibal

Generado: 20/10/2026. No incluye carpetas ni archivos ocultos (`.git`, `.ipynb_checkpoints`, `.gitignore`).

## Árbol

- Proyecto - Ceibal/
  - Datasets & Metadatos/
    - Dataset - Docentes/
      - actividad-de-docentes-2024.csv
      - actividad-de-docentes-2025.csv
      - datos_docentes_2019.csv
      - datos_docentes_2020.csv
      - datos_docentes_2021.csv
      - datos_docentes_2022.csv
      - docentes_datos_abiertos_agesic.csv
    - Dataset - Estudiantes/
      - actividad-de-estudiantes-2024.csv
      - actividad-de-estudiantes-2025.csv
      - datos_estudiantes_2019.csv
      - datos_estudiantes_2020.csv
      - datos_estudiantes_2021.csv
      - datos_estudiantes_2022.csv
      - estudiantes_datos_abiertos_agesic.csv
    - Metadatos - Docentes/
      - metadatos_actividad_docente.csv
      - metadatos_actividad_docente.pdf
    - Metadatos - Estudiantes/
      - metadatos_actividad_estudiante.csv
      - metadatos_actividad_estudiante.pdf
  - Proyecto/
    - Etapa I - Convertir los datasets en Parquet/
      - Concatenación de datos.ipynb
    - Etapa II - Exploración primaria + Limpieza/
      - EDA - Docentes.ipynb
      - EDA - Estudiantes.ipynb
  - README.md
  - Recursos/
    - Dataset docentes concatenado/
      - dataset_docentes_consolidado.parquet
    - Dataset docentes limpio/
      - docentes_limpio.manifest.json
      - docentes_limpio.parquet
    - Dataset estudiantes concatenado/
      - dataset_estudiantes_consolidado.parquet
    - Dataset estudiantes limpio/  *(vacía)*
  - mapa-archivos.md

## Resumen

- Archivos: 27
- `.csv`: 16
- `.ipynb`: 3
- `.parquet`: 3
- `.pdf`: 2
- `.md`: 2
- `.json`: 1

**Carpetas principales:** `Datasets & Metadatos/` (CSV originales y metadatos, no se modifican), `Proyecto/` (notebooks por etapa) y `Recursos/` (Parquet consolidados y limpios).

**Notas:** `Recursos/Dataset estudiantes limpio/` está vacía porque el EDA de estudiantes recién empieza. Ya no existe `Recursos/EDA/`: el notebook de docentes no genera archivos ahí. Junto a `docentes_limpio.parquet` está su manifest, que genera la exportación del notebook.
