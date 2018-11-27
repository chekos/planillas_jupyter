# planillas_jupyter
Un repositorio de planillas de Jupyter Notebooks para usar en la exploración y análisis de datos.

Cada planilla viene con unas cuantas **cells** con código que se asume vas a terminar escribiendo.
Hasta ahora hay 3 planillas:
* Exploración
* Preparación
* Visualizaciones

Debajo el ejemplo de la planilla de Visualizaciones donde ya tenemos escrito el código para importar `altair` y el esqueleto de 2 gráficos.


# 02 Visualizaciones: [NOMBRE_DEL_PROYECTO]

Gráficos por hacer:
1. <br>
2. <br>
3. <br>

***
__Preparación__


```python
import altair as alt
import pandas as pd
from IPython.core.interactiveshell import InteractiveShell

# Esto te permite exhibir más de un OUTPUT por cell
InteractiveShell.ast_node_interactivity = "all"
```


```python
archivo = "../data/NOMBRE_DEL_DATASET.csv"
```


```python
df = pd.read_csv(archivo)

df.head()
```


```python
titulo_1 = "Título del Gráfico"

grafico_1 = alt.Chart(df).mark_bar().encode(
    x = alt.X(),
    y = alt.Y(),
    color = alt.Color()
).properties(
    height = 400,
    width = 600,
    title = f"{titulo_1}"
)

grafico_1
```


```python
titulo_2 = "Título del 2do Gráfico"

grafico_2 = alt.Chart(df).mark_line().encode(
    x = alt.X(),
    y = alt.Y(),
    color = alt.Color()
).properties(
    height = 400,
    width = 600,
    title = f"{titulo_2}"
)
```
