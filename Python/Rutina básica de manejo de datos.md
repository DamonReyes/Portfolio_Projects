## Empezando con la rutina basica de manejo de datos
### Skills Tecnicos para este Proyecto:  Python(pandas), Tableau

## Table of contents
1. [pre processing](#introduction)
2. [Visualization](#paragraph1)




###### Empezando con la rutina básica de manejo de datos <a name="introduction"></a>
lo primero que hago es cargar el dataset: revisar de que tipos de datos disponemos y hacer una copia para no trabajar sobre el original como buena practica. Convertimos la columna de fecha en un formato más simple.

![Image 1](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(11).png)

Pasamos [dt] a una nueva columna para entenderla mejor y hacemos un filtro por [Country] y vemos la media de las temperaturas que tenemos.

![Image 2](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(12).png)

Creamos una columna solo con el año para filtros posteriores y cambiamos los nombres para el merge

![Image 3](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(13).png)

Ahora tenemos que pasarle ese formato a todos los datasets con los que queremos el analisis, los importamos y creamos una funciona para pasar el formato de lo que ya hicimos.

![Image 4](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(15).png)

Vemos de nuevo dtypes para confirmar y convertimos los datos para que sean compatibles con el primer dataset, hacemos un merge con todos los datasets ya transformados.

![Image 5](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(16).png)

Borramos las columnas que no necesitamos y eliminamos tambien los datos nulos porque en este caso específico los datos nulos solo van a sesgar el analisis y prefiero que solo trabajemos con datos y países con sus respectivos datos.

![Image 6](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(17).png)

> Ahora que ya terminamos el pre procesamiento y la preparación de los datos lo exportamos en xlxs y vamos a analizarlo en Tableau.

Comenzamos a hacer preguntas para descubrir los insights y lo primero que podemos preguntar es: <a name="paragraph1"></a>

Cuáles son los paises que más Co2 producen?
En qué año los paises desecharon más Co2?
Ver la evolución del Co2 en los últimos años?
Qué temperatura máxima alcanzaron los países con el Co2 como etiqueta?
Qué pais tiene mayor producción de agricultura?
Qué país tiene la mayor tala de árboles y cómo aumenta la temperatura en dicho país?
Entre otros y creamos el dashboard con los insights que encontramos! :D

![Image 7](https://github.com/DamonReyes/Routine_1/blob/main/Screenshots/Screenshot%20(19).png)

Dejo también el link original del dataviz [tabelau_routine1](https://public.tableau.com/profile/damon.reyes#!/vizhome/routine1/Dashboard1)

Y puedes ver todas mis visualizaciones en [tableau_damonreyes](https://public.tableau.com/profile/damon.reyes#!/)

> Damon reyes analista

Linkedin [linkedin damon](https://www.linkedin.com/in/damon-reyes/)
