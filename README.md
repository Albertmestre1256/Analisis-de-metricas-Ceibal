# Análisis de métricas Ceibal — Datos Abiertos

Proyecto de análisis exploratorio de los datos de actividad educativa publicados por [Plan Ceibal](https://www.ceibal.edu.uy/) en el [Catálogo de Datos Abiertos del Estado uruguayo](https://catalogodatos.gub.uy/dataset/?tags=Ceibal).

El objetivo es doble: aprender ciencia de datos mediante la práctica sobre datos reales, y construir un portfolio demostrable de análisis aplicado al contexto educativo uruguayo.

---

## Fuente de datos

Los datasets fueron descargados del Catálogo de Datos Abiertos de Uruguay (AGESIC / Plan Ceibal). Corresponden a registros de actividad de **docentes y estudiantes** del sistema educativo público en plataformas digitales de Ceibal durante los años lectivos **2019–2025**.

- **Licencia:** Datos abiertos del Estado uruguayo. Ver documentación oficial en cada dataset.
- **Unidad de observación:** una persona (docente o estudiante) en un año lectivo, reportada por un subsistema educativo (DGEIP, DGES o DGETP).

---

## Datasets disponibles

### Actividad docente

| Archivo | Período |
|---|---|
| `datos_docentes_2019.csv` | 2019 |
| `datos_docentes_2020.csv` | 2020 |
| `datos_docentes_2021.csv` | 2021 |
| `datos_docentes_2022.csv` | 2022 |
| `actividad-de-docentes-2024.csv` | 2024 |
| `actividad-de-docentes-2025.csv` | 2025 |
| `docentes_datos_abiertos_agesic.csv` | Histórico AGESIC |

### Actividad estudiantil

| Archivo | Período |
|---|---|
| `datos_estudiantes_2019.csv` | 2019 |
| `datos_estudiantes_2020.csv` | 2020 |
| `datos_estudiantes_2021.csv` | 2021 |
| `datos_estudiantes_2022.csv` | 2022 |
| `actividad-de-estudiantes-2024.csv` | 2024 |
| `actividad-de-estudiantes-2025.csv` | 2025 |
| `estudiantes_datos_abiertos_agesic.csv` | Histórico AGESIC |

> Los archivos originales se conservan sin modificaciones en `Datasets & Metadatos/`. Todo procesamiento opera sobre copias o sobre los archivos consolidados en `Recursos/`.

---

## Variables principales

### Dataset docentes

| Variable | Tipo | Descripción |
|---|---|---|
| `Id persona` | String | Identificador único por persona (estable entre años) |
| `Sexo` | String | Sexo de nacimiento administrativo (Femenino / Masculino / Sin Dato) |
| `Rol` | String | Siempre "Docente" |
| `Departamento` | String | Departamento del centro educativo (19 departamentos) |
| `Subsistema` | String | DGEIP / DGES / DGETP |
| `Año lectivo` | String | Año lectivo reportado |
| `Cantidad de días ingreso a CREA` | Numérico | Días distintos con actividad en la plataforma CREA |
| `Cantidad de Comentarios posteados en CREA` | Numérico | Total de comentarios en cursos, foros y tareas |
| `Cantidad de Acciones totales en CREA` | Numérico | Total de acciones en CREA (excluye creación de usuario y visitas a recursos) |
| `Cantidad de días de ingreso a Biblioteca` | Numérico | Días con actividad en Biblioteca País |
| `Cantidad de prestamos en Biblioteca` | Numérico | Total de recursos prestados en Biblioteca País |

### Dataset estudiantes (variables adicionales)

| Variable | Tipo | Descripción |
|---|---|---|
| `Ciclo` | String | Ciclo educativo (Inicial, Primaria, Ciclo Básico, Bachillerato, etc.) |
| `Grado` | String | Grado dentro del ciclo |
| `Zona` | String | Urbana / Rural / Sin Dato (solo DGEIP) |
| `Contexto` | String | Quintil de vulnerabilidad del centro (Quintil 1 = más vulnerable; solo DGEIP) |
| `Cantidad de entregas de tareas en CREA` | Numérico | Total de tareas enviadas (assessment + assignment) |
| `Cantidad de días de ingreso a Matific` | Numérico | Días con actividad en Matific (matemáticas; DGEIP, Niv. 5 hasta 6° grado) |
| `Cantidad de episodios finalizados en Matific` | Numérico | Total de episodios completados en Matific |
| `Cantidad de días de ingreso a PAM` | Numérico | Días con actividad en PAM (matemáticas; 3° Primaria a Media; descontinuada en 2022) |
| `Cantidad de actividades finalizadas en PAM` | Numérico | Total de actividades completadas en PAM |

> La columna `Id persona` es pseudoanónima. No permite identificar personas individuales.

---

## Estructura del repositorio

```
├── Datasets & Metadatos/
│   ├── Dataset - Docentes/          # CSVs originales — no modificar
│   ├── Dataset - Estudiantes/       # CSVs originales — no modificar
│   ├── Metadatos - Docentes/        # Diccionario de variables (CSV + PDF)
│   └── Metadatos - Estudiantes/     # Diccionario de variables (CSV + PDF)
├── Proyecto/
│   ├── Etapa I - Convertir los datasets en Parquet/
│   │   └── Concatenación de datos.ipynb
│   └── (etapas siguientes se agregarán aquí)
├── Recursos/
│   ├── Dataset docentes concatenado/
│   │   └── dataset_docentes_consolidado.parquet
│   └── Dataset estudiantes concatenado/
│       └── dataset_estudiantes_consolidado.parquet
└── README.md
```

---

## Etapas del proyecto

| # | Etapa | Notebook / Entregable | Estado |
|---|---|---|---|
| 1 | Descarga y consolidación de datos | `01_concatenacion.ipynb` | ✅ Completo |
| 2–3 | Exploración primaria y limpieza | `02_exploracion_y_limpieza.ipynb` | ⬜ Pendiente |
| 4 | Estadística descriptiva | `03_estadistica_descriptiva.ipynb` | ⬜ Pendiente |
| 5 | Estadística inferencial | `04_estadistica_inferencial.ipynb` | ⬜ Pendiente |
| 6 | Machine Learning (opcional) | `05_machine_learning.ipynb` | ⬜ Opcional |
| 7 | Análisis en R | `06_analisis_R.Rmd` | ⬜ Pendiente |
| 8 | Dashboard en Power BI | `dashboard_ceibal.pbix` | ⬜ Pendiente |
| 9 | Artículo académico | `articulo_ceibal.pdf` | ⬜ Pendiente |
| 10 | Comunicación del proyecto | README + portfolio | ⬜ Pendiente |

---

## Stack tecnológico

- **Python** (pandas, pyarrow, matplotlib, seaborn, scipy) — Jupyter Lab
- **R** — análisis estadístico complementario
- **Power BI** — visualización e informes interactivos

---

## Nota sobre los datos

Los datos corresponden a métricas de actividad en plataformas digitales (CREA, Matific, PAM, Biblioteca País) y no incluyen calificaciones, asistencia ni información que permita identificar a personas individuales. La variable `Contexto` (quintil de vulnerabilidad) está disponible únicamente para centros de DGEIP.

La cobertura es 2019–2025, con una discontinuidad en 2023 en los datasets descargados. Los años 2024 y 2025 provienen de archivos con nomenclatura diferente a los años anteriores; la compatibilidad de variables se verificará en la etapa de exploración y limpieza.

---

*Proyecto en desarrollo — Albert Mestre · Montevideo, Uruguay · 2026*
