# Catálogo de películas · Team Challenge

> Renombrad este fichero a `README.md` y completad las partes entre `<...>`.

**Equipo: 2** Manuel Martín Arillo, Isaac Cuesta Martinez, Luis Gonzalez-Aller Jareño

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones

| Persona | Rol | Notebook / tarea |
|---|---|---|
| Manuel Martín Arillo | 01, 02 y 04 | Crear repo, merge ramas y git, responder preguntas 02_Analisis y 4A |
| Isaac Cuesta Martinez | 02 | Analisis, merge datos y agrupaciones, calidad y QA reproducibilidad |
| Luis Gonzalez-Aller Jareño | 03, 04 | fetch de datos y generación con gemini, gestión de claves |

## Instalación

**Antes de instalar descargar links.csv, movies.csv, ratings.csv y tags.csv adañirlos todos a ./data**  

```bash
git clone https://github.com/mmacode75/TC_01_MOVIES_E2.git
cd TC_01_MOVIES_E2
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp example .env            # y rellenad las claves
```

## Claves necesarias

| Variable | Dónde se obtiene |
|---|---|
| `TMDB_READ_ACCESS_TOKEN` o `TMDB_API_KEY` | themoviedb.org → Settings → API |
| `GEMINI_API_KEY` | aistudio.google.com |

## Ejecución

Ejecutad los notebooks **en este orden** (cada uno genera un CSV en `data/processed/` que usa el siguiente):

1. `01_ingesta_limpieza.ipynb` → `movies_clean.csv`
2. `02_analisis.ipynb`
3. `03_tmdb.ipynb` → `movies10.csv`
4. `04_gemini.ipynb` → `movies10_es.csv`

## Resultados principales

### Conclusiones sobre los datos

- El dataset base por lo general está bastante completo y no se necesita un trabajo especial de limpieza o tratamiento.
- La comunidad de tmdb es bastante activa ya que existen muchas calificaciones para las distintas películas.
- Las categorías y tags son los datos más dispersos ya que no todos están estrechamente relacionados con la película.

### Conclusiones sobre el trabajo realizado

- Hemos aprendido e interiorizado metodología de trabajo en equipo y coordinación a la que no estamos habituados.
- Hemos experimentado la adaptación a servicios cambiantes y en continua actualización de terceros como la api de gemini y tmdb y aprendido a leer documentación de manera eficiente.
