# SEABORN
Esta biblioteca se utiliza principalmente para la visualización de datos y está construida sobre Matplotlib
## Tipos de Gráficos en Seaborn
Seaborn ofrece una variedad de gráficos para visualizar datos de forma efectiva. Algunos de los tipos más comunes son:
### Gráficos de Dispersión (scatter plots): Útiles para mostrar la relación entre dos variables numéricas.
~~~~
iris = sns.load_dataset("iris")
sns.relplot(x = "sepal_length", y = "sepal_width", data = iris);
~~~~
![image](https://github.com/user-attachments/assets/d80a3dbf-a1ba-40d9-9dd6-8d7b04580e0f)


### Gráficos de Líneas (line plots): Ideales para visualizar tendencias a lo largo del tiempo.
~~~~
df = pd.DataFrame({
    "x": range(100),
    "y": np.random.randn(100).cumsum()
})
sns.relplot(x = "x", y = "y", data = df, kind = "line");
~~~~
![image](https://github.com/user-attachments/assets/ed631764-694e-46af-a1a1-89bab332370a)


### Gráficos de Barras (bar plots): Muestran la relación entre categorías y un valor numérico.
~~~~
titanic = sns.load_dataset("titanic")
sns.catplot(x = "sex", y = "survived", kind = "bar", data = titanic);
~~~~
![image](https://github.com/user-attachments/assets/81af22c4-1ff1-4115-b2bb-95c43ceb6fca)



### Histogramas: Para visualizar la distribución de una variable numérica.
~~~~
y = np.random.normal(size = 100)
sns.distplot(y, kde = False);
~~~~
![image](https://github.com/user-attachments/assets/e1f11947-40d4-4820-9587-ce4e30162013)
