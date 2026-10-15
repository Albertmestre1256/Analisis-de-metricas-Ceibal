# Análisis de métricas Ceibal — Datos Abiertos

Proyecto de análisis exploratorio de los datos de actividad educativa publicados por [Plan Ceibal](https://www.ceibal.edu.uy/) en el [Catálogo de Datos Abiertos del Estado uruguayo](https://catalogodatos.gub.uy/dataset/?tags=Ceibal).

El objetivo es doble: aprender ciencia de datos mediante la práctica sobre datos reales, y construir un portfolio demostrable de análisis aplicado al contexto educativo uruguayo.

---

## Fuente de datos

Los datasets fueron descargados del Catálogo de Datos Abiertos de Uruguay (AGESIC / Plan Ceibal). Corresponden a registros de actividad de **docentes y estudiantes** del sistema educativo público en plataformas digitales de Ceibal durante los años lectivos **2019–2025**.

- **Licencia:** Datos abiertos del Estado uruguayo. Ver documentación oficial en cada dataset.
- **Unidad de observación:** en docentes (verificado), una fila por docente, año lectivo y subsistema (DGEIP, DGES o DGETP): un mismo docente puede aparecer varias veces en un año, una por subsistema. En estudiantes todavía no se verificó.

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
| `docentes_datos_abiertos_agesic.csv` | 2023 (nombre distinto al resto de los años) |

### Actividad estudiantil

| Archivo | Período |
|---|---|
| `datos_estudiantes_2019.csv` | 2019 |
| `datos_estudiantes_2020.csv` | 2020 |
| `datos_estudiantes_2021.csv` | 2021 |
| `datos_estudiantes_2022.csv` | 2022 |
| `actividad-de-estudiantes-2024.csv` | 2024 |
| `actividad-de-estudiantes-2025.csv` | 2025 |
| `estudiantes_datos_abiertos_agesic.csv` | 2023 (nombre distinto al resto de los años) |

> Los archivos originales se conservan sin modificaciones en `Datasets & Metadatos/`. Todo procesamiento opera sobre copias o sobre los archivos consolidados en `Recursos/`.

---

## Variables principales

### Dataset docentes

| Variable | Tipo | Descripción |
|---|---|---|
| `Id persona` | String | Identificador pseudoanónimo por persona; en docentes el mismo ID se repite entre años |
| `Sexo` | String | Sexo de nacimiento administrativo (Femenino / Masculino / Sin Dato) |
| `Rol` | String | Siempre "Docente" |
| `Departamento` | String | Departamento del centro educativo (19 departamentos y el valor "Sin Dato") |
| `Subsistema` | String | DGEIP / DGES / DGETP |
| `Año lectivo` | Numérico | Año lectivo reportado |
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
│   └── Etapa II - Exploración primaria + Limpieza/
│       ├── EDA - Docentes.ipynb
│       └── EDA - Estudiantes.ipynb
├── Recursos/
│   ├── Dataset docentes concatenado/
│   │   └── dataset_docentes_consolidado.parquet
│   └── Dataset estudiantes concatenado/
│       └── dataset_estudiantes_consolidado.parquet
├── mapa-archivos.md                 # Árbol de archivos del proyecto
└── README.md
```

---

## Etapas del proyecto

| # | Etapa | Notebook / Entregable | Estado |
|---|---|---|---|
| 1 | Descarga y consolidación de datos | `Concatenación de datos.ipynb` | ✅ Completo |
| 2–3 | Exploración primaria y limpieza | `EDA - Docentes.ipynb`, `EDA - Estudiantes.ipynb` | 🔄 En curso (docentes avanzado; estudiantes recién iniciado) |
| 4 | Estadística descriptiva | `03_estadistica_descriptiva.ipynb` | ⬜ Pendiente |
| 5 | Estadística inferencial | `04_estadistica_inferencial.ipynb` | ⬜ Pendiente |
| 6 | Machine Learning (opcional) | `05_machine_learning.ipynb` | ⬜ Opcional |
| 7 | Análisis en R | `06_analisis_R.Rmd` | ⬜ Pendiente |
| 8 | Dashboard en Power BI | `dashboard_ceibal.pbix` | ⬜ Pendiente |
| 9 | Artículo académico | `articulo_ceibal.pdf` | ⬜ Pendiente |
| 10 | Comunicación del proyecto | README + portfolio | ⬜ Pendiente |

---

## Hallazgos de la etapa de limpieza (docentes, en curso)

- **Espacios al final de las categorías.** En el archivo de 2025, `Sexo`, `Subsistema` y `Departamento` traen espacios sobrantes; Python los cuenta como valores distintos. Se limpiaron con `.str.strip()`.
- **Cobertura.** Cada archivo contiene un único año lectivo, el de su nombre: 2019–2025 sin huecos.
- **Unidad de observación.** 74.929 docentes en 379.153 filas. La combinación `Id persona` + `Año lectivo` se repite en 39.031 filas; la hipótesis "una fila por docente y año" se descartó y "una fila por docente, año y subsistema" resistió la prueba (una sola excepción, ID 199850 en 2024). Para contar personas se usa `nunique`, no filas.
- **Faltantes escondidos como texto.** `isna()` da 0, pero `Sexo` tiene 480 filas "Sin Dato" (465 docentes) y `Departamento` 39 (39 docentes). En `Sexo` se completaron 67 filas desde otras filas del mismo docente (62 docentes, todos con un único sexo registrado) y se conservan 413 filas (403 docentes) como "Sin Dato", que se excluyen solo en los análisis por sexo; borrarlas habría eliminado 403 docentes. En `Departamento` la decisión sigue pendiente: el valor cambia entre años para un mismo docente, así que no se puede completar desde otras filas sin más análisis.
- **Supuestos sin verificar.** Se unificaron las columnas de comentarios y acciones de CREA de 2019–2024 con las de 2025 asumiendo que miden lo mismo; los metadatos disponibles solo cubren 2019–2022.

---

## Stack tecnológico

- **Python** (pandas, pyarrow, matplotlib, seaborn, scipy) — Jupyter Lab
- **R** — análisis estadístico complementario
- **Power BI** — visualización e informes interactivos

---

## Nota sobre los datos

Los datos corresponden a métricas de actividad en plataformas digitales (CREA, Matific, PAM, Biblioteca País) y no incluyen calificaciones, asistencia ni información que permita identificar a personas individuales. La variable `Contexto` (quintil de vulnerabilidad) está disponible únicamente para centros de DGEIP.

La cobertura es 2019–2025, sin años faltantes: cada archivo corresponde a un único año lectivo (el de 2023 es el archivo `*_datos_abiertos_agesic.csv`). Los archivos de 2023, 2024 y 2025 tienen nomenclatura diferente a la de 2019–2022, y en docentes las columnas de comentarios y acciones de CREA cambian de nombre en 2025; la compatibilidad de variables se resuelve en la etapa de exploración y limpieza.

---

*Proyecto en desarrollo — Albert Mestre · Montevideo, Uruguay · 2026*
