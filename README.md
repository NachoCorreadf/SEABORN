# SEABORN
Esta biblioteca se utiliza principalmente para la visualización de datos y está construida sobre Matplotlib
## Tipos de Gráficos en Seaborn
Seaborn ofrece una variedad de gráficos para visualizar datos de forma efectiva. Algunos de los tipos más comunes son:
### Gráficos de Dispersión (scatter plots): Útiles para mostrar la relación entre dos variables numéricas.
~~~~
import seaborn as sns
sns.scatterplot(data=df, x='variable_x', y='variable_y')
~~~~

### Gráficos de Líneas (line plots): Ideales para visualizar tendencias a lo largo del tiempo.
~~~~
sns.lineplot(data=df, x='tiempo', y='valor')
~~~~

### Gráficos de Barras (bar plots): Muestran la relación entre categorías y un valor numérico.
~~~~
sns.barplot(data=df, x='categoría', y='valor')
~~~~

### Histogramas: Para visualizar la distribución de una variable numérica.
~~~~
sns.histplot(data=df, x='variable', bins=30)
~~~~
