
<h1 align='center'>
 <b>PROYECTO INDIVIDUAL Nº2 - Alfonso Justo</b>
</h1>

# <h1 align="center">**`Telecomunicaciones`**</h1>

¡Bienvenidos al último proyecto individual de la etapa de labs! En esta ocasión, deberán hacer un trabajo situándose en el rol de un ***Data Analyst***.
<p align='center'>
<img src = 'https://newses.cgtn.com/n/BfJIA-CAA-HAA/BceGDAA.jpg' height = 200>
<p>


## **Descripción del problema -contexto y rol a desarrollar-**


### **Contexto**

Las telecomunicaciones se refieren a la transmisión de información a través de medios electrónicos, como la telefonía, la televisión, la radio y, más recientemente, el internet. Estos medios de comunicación permiten la transmisión de información entre personas, organizaciones y dispositivos a largas distancias.

El internet, por su parte, es una red global de computadoras interconectadas que permite el intercambio de información en tiempo real. Desde su creación, ha tenido un impacto significativo en la vida de las personas, transformando la manera en que nos comunicamos, trabajamos, aprendemos y nos entretenemos.

La industria de las telecomunicaciones ha jugado un papel vital en nuestra sociedad, facilitando la información a escala internacional y permitiendo la comunicación continua incluso en medio de una pandemia mundial. La transferencia de datos y comunicación se realiza en su mayoría a través de internet, líneas telefónicas fijas, telefonía móvil, y en casi cualquier lugar del mundo. 

En comparación con la media mundial, Argentina está a la vanguardia en el desarrollo de las telecomunicaciones, teniendo para el 2020 un total de [62,12 millones de conexiones](https://www.datosmundial.com/america/argentina/telecomunicacion.php).
<br>
<br>

# <h1 align="center">**`Desarrollo`**</h1>
<br>
Fuente de Datos:

[DatosAbiertos](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/)

<br>

## **ETL (Extract, Transform, Load) y EDA (Exploratory Data Analysis)**
<br>
A pesar que dentro de las instrucciones no se tiene la consigna de realizar un ETL, fue necesario realizarlo, ya que al tener que obtener la información directamente de la fuente que contiene los datos y al tener tantos datasets, las transformaciones fueron completamente necesarias.
<br>
Como sabemos, al mandar el proyecto al repositorio, el tamaño que deben tener es un aspecto que debemos cuidar, entonces es por eso que se tomaron desiciones con respecto a los datasets que se tenian a disposición.
<br><br>

*Extracción*<br><br>
Para hacer esta primera parte con la que obtenemos los datasets podríamos hacerlo de dos formas, primero puede ser mediante la API que tiene la página proporcionada y la segunda era de forma manual, lo que se hizo en este caso fue hacerlo de forma manual, se dejó para el final la extracción mediante la primera forma, esto para ahorrar tiempo.
<br><br>

*Transformaciones*<br><br>
Una de las transformaciones más relevantes fue la de unificar los datasets que contenian datos por Trimestre o por Provincia, con esto me refiero a que se tenian dos grupos (por llamarlos de una forma), uno mostraba la información por trismestre y otro que igualmente los mostraba de esa forma pero a diferencia del otro, este incluida las Provincias de Argentica, lo que provocaba que el dataset creciera y no se pudiera comparar entre ambos sin hacer algunas transformaciones en el formato del archivo.
<br><br>

*Carga*<br><br>
Al final de las transformaciones necesarias se guardaron todos los dataframes resultantes de las transformaciones, esto para tener una referencia más clara del resultado del trabajo, si bien tenemos el dataset original con la transformación, por practicidad (como se mencionó antes del tamaño de los datasets) para no tener problemas futuros.
<br><br>

### **EDA**<br><br>
La realización del EDA como la vez pasada es una de las etapas que más me gustan (el ETL igual, me es interesante, me ayuda a darme una idea de como hacer el EDA), porque es la interpretación final de los datos antes de pasar a realizar alguna otra cosa, es por eso la importancia de hacerlo de una buena forma, iniciando desde el ETL para tener claros cuales serán los *insigths* que podemos ver a simple vista.<br>
No se describió en el proyecto anterior pero la forma en la que me gusta hacer estos pasos es con notas, por ejemplo, uno de los datasets contenia información de los ingresos, lo que me llevó a pensar en que podría hacer un dashboard que mostrara el incremento de los mismos con el paso del tiempo, y para no olvidarlo tomé notas de eso que me di cuenta "a simple vista" como dije antes, para poder enformarme un poco más en eso.<br>
Me resulta interesante hacerlo de esa forma porque sin problemas de que se me olvide o que pueda pasarlo por alto, tengo ya algo con que trabajar después del ETL.<br>
Este es un ejemplo de lo que se hizo.

```python
#Realizamos un gráfico
sns.barplot(x = int_ingresos['Año'], y = int_ingresos['Ingresos (miles de pesos)'])
```
### Resultado
<br>
<p align='center'>
<img src = 'src/plot ingresos.png' height = 500>
<p>
<br>
Dashboards como ese son los que se observarán en los archivos incluidos en el repositorio.<br>
<br><br>

## **DASHBOARDS**
<br>

Parte del trabajo que se debe realizar es hacer dashboards que puedan mostrar la información de manera clara, entendible y porqué no, bonita. Es por eso que usando **PowerBI** se realizaron algunos que aparte de mostrar la información de las gráficas, nos ayudarán a realizar y ver algunos KPI.
<br><br>
(IMAGENES OBTENIDAS DE POWERBI)

<br><br>

## **ANÁLISIS**
<br>

Esta parte me resultó extraña que la pusieran por separado, puesto que dentro del EDA pude realizarlo, es decir, no se realizó de forma separada, si no que dentro de los procesos que se vieron antes se fueron realizando algunas conclusiones, se pusieron algunos comentarios y observaciones con respecto a la información presentada y esto lo podrán corroborar en los archivos **Jupyter** en donde se presentan el ETL y el EDA.<br>
No indagaré mucho al respecto, pero si puedo comentar que el realizar un análisis mientras se está trabajando con los datos, su estructura, sus formatos, tipos de datos, relaciones, etc. Es para mi indispensable ir haciendo conclusiones, ir a la par realiando algunas observaciones con respecto a los datos vistos, ya se mencionó antes como se van obteniedo algunas conclusiones y conforme se avanza se pueden ver algunas otras interesantes ya con el acomodo necesario.
<br><br><br>

## **KPI's**
<br>
