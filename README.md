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


## Estilos para una Presentación más Profesional
Seaborn permite personalizar los estilos de los gráficos para hacerlos más atractivos y profesionales. Aquí hay algunas maneras de hacerlo:


### Establecer un Estilo General: Puedes cambiar el estilo global de tus gráficos con set_style(). Algunos estilos disponibles son darkgrid, whitegrid, dark, white, y ticks.
~~~~
for i, s in enumerate(["dark", "white", "ticks", "whitegrid", "darkgrid"]):
    sns.set_style(s);
    fig = plt.figure(figsize = (6, 2))
    fig.suptitle(s)
    sns.boxplot(x = "day", y = "tip", data = tips);
~~~~
![image](https://github.com/user-attachments/assets/e90699d4-9317-470d-a20f-b9b10a894e9d)

### Personalizar Paletas de Colores: Utiliza set_palette() para cambiar la paleta de colores de tus gráficos.
~~~~
my_palette = ["#D4E09B", "#9AC2C9", "#9CB380", "#C2C5BB"]
sns.catplot(x = "tip", y = "day", data = tips, kind = "box", palette = my_palette);
~~~~
![image](https://github.com/user-attachments/assets/14ae1493-7ac6-4082-be52-71ec388e7c3c)

### Ajustar el Tamaño de las Figuras: Puedes ajustar el tamaño de las figuras con plt.figure(figsize=(ancho, alto)).
~~~~
import matplotlib.pyplot as plt
fig, ax = plt.subplots(figsize = (9, 3))
sns.barplot(x="sex", y="survived", hue="class", data=titanic, ax = ax);
~~~~
![image](https://github.com/user-attachments/assets/7937b989-ea27-4820-b47f-1150e49ba2f7)

### Agregar Títulos y Etiquetas: Asegúrate de añadir títulos y etiquetas descriptivas a tus ejes.
~~~~
import seaborn as sns
df = sns.load_dataset("tips")

sns.scatterplot(x = "total_bill",
                y = "tip", data = df).set_title("Título")

# Equivalente a:            
ax = sns.scatterplot(x = "total_bill",
                y = "tip", data = df)
              
ax.set_title("Título")  
~~~~
![image](https://github.com/user-attachments/assets/1d907c34-645c-4bd8-a417-714bc1228f03)

### Guardar Gráficos: Puedes guardar tus gráficos en diferentes formatos utilizando plt.savefig().
~~~~
plt.savefig('grafico.png', dpi=300)
~~~~
