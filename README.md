# planillas_jupyter
Un repositorio de planillas de Jupyter Notebooks para usar en la exploración y análisis de datos.

Cada planilla viene con unas cuantas **cells** con código que se asume vas a terminar escribiendo.
Hasta ahora hay 3 planillas:
* Exploración
* Preparación
* Visualizaciones

Debajo el ejemplo de la planilla de Visualizaciones donde ya tenemos escrito el código para importar `altair` y el esqueleto de 2 gráficos.


# 00 Exploración: [NOMBRE_DEL_PROJECTO]

##### Metas:
1. Identificar características. 
2. Familiarizarse con los detalles de los datos
  - dtypes
  - tamaño del dataset
3. ETC

##### Cambios:
* fecha_del_ultimo_cambio: Descripción del cambio.
* otro cambio: otra descripción.

***
__Preparación__


```python
import pandas as pd
from pathlib import Path
from datetime import datetime
```


```python
# Inicializa rutas hacia los archivos.
fecha_hoy = datetime.today()
archivos_en_bruto = Path("../datos/en_bruto/")
archivos_procesados = Path("../datos/procesados/")
archivo_final = Path("../datos/procesados/") / f"resumen_{fecha_hoy:%b-%d-%Y}.csv"
```


```python
archivo = archivos_en_bruto / 'REEMPLAZA_ESTO_CON_EL_NOMBRE_DE_TU_ARCHIVO'
```


```python
# Leer y describir el conjunto de datos.
datos = pd.read_csv(archivo)

print("-"*25)
print(f"{datos.shape[0]} filas, {datos.shape[1]} columnas.")
print("-"*25)
datos.describe()
print("-"*25)
datos.head()
```

###### En el de visualizaciones tienes `cells` como:
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
