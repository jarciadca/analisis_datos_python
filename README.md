# Análisis de Datos con Python 📊



Proyecto de análisis de datos usando Python, pandas, SQL y visualizaciones. Trabajo sobre keywords de Google Ads y análisis de competencia.



## 📋 Descripción



Este proyecto contiene un cuaderno Jupyter (`data\_analisys\_python.ipynb`) donde se realiza:



- Limpieza y exploración de datos de keywords

- Análisis de competencia (LOW / MEDIUM / HIGH)

- Distribución de `Competition (indexed value)`

- Consultas SQL sobre DataFrames con pandasql / duckdb

- Visualizaciones con matplotlib y seaborn



---



# 🗂️ Estructura del proyecto



```

EJEMPLO1\_PYTHON/

├── .gitignore

├── README.md

├── requirements.txt

├── data\_analisys\_python.ipynb

├── data/

│   └── keywords.csv

└── .venv/

```



## ⚙️ Requisitos



- Python 3.10+

- Git (opcional, para clonar)

- VS Code o Jupyter Notebook/Lab



---



## 🚀 Instalación



### 1. Clonar el repositorio



```bash

git clone https://github.com/jarciadca/analisis\_datos\_python.git

cd analisis\_datos\_python

```



### 2. Crear y activar el entorno virtual



Windows (PowerShell):



```powershell

python -m venv .venv

.\\.venv\\Scripts\\Activate.ps1

```



macOS / Linux:



```bash

python3 -m venv .venv

source .venv/bin/activate

```



### 3. Instalar dependencias



```bash

python -m pip install --upgrade pip

python -m pip install -r requirements.txt

```



### 4. Registrar el kernel de Jupyter (opcional)



```bash

python -m ipykernel install --user --name=ejemplo1 --display-name "Python (EJEMPLO1)"

```



## ▶️ Uso



Abre el notebook:



```bash

jupyter notebook data\_analisys\_python.ipynb

```



O en VS Code: abre el `.ipynb` y selecciona el kernel `.venv` (arriba a la derecha).



> ⚠️ Importante: cada vez que abras el notebook, ejecuta \*\*Run All\*\* desde la primera celda. Jupyter no conserva las variables al cerrar o reiniciar el kernel.



---



## 🧰 Stack de librerías



| Librería | Uso |

|---|---|

| pandas | Manipulación de datos |

| numpy | Cálculos numéricos |

| matplotlib | Gráficos base |

| seaborn | Visualizaciones estadísticas |

| pandasql | SQL sobre DataFrames |

| duckdb | Alternativa moderna y rápida a pandasql |

| jupyter | Entorno interactivo |



## 📊 Ejemplos de análisis



### Limpieza de datos



```python

df = df.dropna(subset=\['Top of page bid (low range)'])

```



### Histograma por categoría



```python

ax = df.plot.hist(

&#x20;   column=\["Competition (indexed value)"],

&#x20;   by='Competition',

&#x20;   bins=10,

&#x20;   figsize=(8, 12)

)

```



### Consulta SQL sobre el DataFrame



```python

from pandasql import sqldf

pysqldf = lambda q: sqldf(q, globals())



q = """

SELECT Keyword, avg\_monthly\_searches, three\_month\_change, yoy\_change

FROM df

"""

df\_export = pysqldf(q)

```



## 🤝 Contribuir



1. Haz fork del repo.

2. Crea una rama: `git checkout -b feature/nueva-funcionalidad`

3. Commit: `git commit -m "Añadida nueva funcionalidad"`

4. Push: `git push origin feature/nueva-funcionalidad`

5. Abre un Pull Request.



## 📄 Licencia



Este proyecto está bajo la licencia MIT. Ver `LICENSE` para más detalles.



## 👤 Autor



**jarciadca**



- GitHub: [@jarciadca](https://github.com/jarciadca)



## 🙏 Agradecimientos



- Documentación de [pandas](https://pandas.pydata.org/)

- [DuckDB](https://duckdb.org/) por consultas SQL rápidas

- Comunidad de [Stack Overflow](https://stackoverflow.com/)

