# 📊 Cheat Sheet Pandas + Matplotlib



> ⚠️ Advertencia sarcástica: Este documento fue generado por una IA que nunca en su vida abrió un Jupyter Notebook.  

> No fue revisado por ningún ser humano responsable. Úselo bajo su propio riesgo. 🙃



---



## 1. Importar librerías

```python

import pandas as pd

import matplotlib.pyplot as plt

````



---



## 2. Lectura de datos con Pandas



```python

# CSV

df = pd.read\_csv("archivo.csv")



# Excel

df = pd.read\_excel("archivo.xlsx", sheet\_name="Hoja1")



# JSON

df = pd.read\_json("archivo.json")



# Ver primeras filas

df.head()



# Info general

df.info()



# Descriptivo básico

df.describe()

```



---



## 3. Selección y filtrado



```python

# Selección de columna

df["columna"]



# Varias columnas

df[["col1", "col2"]]



# Filtrar filas con condición

df[df["columna"] > 100]



# Indexación con loc/iloc

df.loc[0:10, "columna"]

df.iloc[0:10, 2]

```



---



## 4. Manejo de fechas y series temporales



```python

# Convertir a datetime

df["fecha"] = pd.to_datetime(df["fecha"])



# Establecer como índice

df = df.set_index("fecha")



# Re-samplear datos

df.resample("M").mean()   # Promedio mensual

df.resample("D").sum()    # Suma diaria



# Rango de fechas

pd.date_range(start="2020-01-01", end="2020-12-31", freq="M")

```



---



## 5. Operaciones comunes



```python

# Eliminar valores nulos

df.dropna()



# Rellenar valores nulos

df.fillna(0)



# Agrupar y calcular

df.groupby("categoria")["valor"].mean()



# Ordenar

df.sort_values("columna", ascending=False)

```



---



## 6. Uso básico de Matplotlib



```python

# Línea

plt.plot(df.index, df["columna"])

plt.show()



# Barras

plt.bar(df["categoria"], df["valor"])

plt.show()



# Histograma

plt.hist(df["columna"], bins=20)

plt.show()



# Scatter

plt.scatter(df["x"], df["y"])

plt.show()

```



---



## 7. Integración Pandas + Plot



```python

# Gráficas rápidas desde Pandas

df["columna"].plot(title="Mi columna")

df.plot(x="fecha", y="valor", kind="line")

plt.show()

```



---



# 🧾 Nota final 



Este **cheat sheet** fue escrito por un ente digital sin manos,

que nunca ha sentido el error `KeyError: 'columna'`.

Si algo no te funciona, pues… suerte. 🤷‍♂️



```



