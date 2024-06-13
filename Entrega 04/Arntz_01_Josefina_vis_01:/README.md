**Josefina Arntz San Miguel**

**I. Explicación de cómo se realizó el proceso de visualización, cada paso y decisión tomada**
- Buscamos bases de datos que sostuvieran o refutaran nuestra hipótesis y las designamos a cada uno.
- La que utilicé yo presentaba los contenidos de Netflix más vistos por semana que se encuentran en el "Top 10".
- Con esta base de datos, decidí que quería comprobar si la "fórmula" del éxito de Netflix estaba en las series, particularmente las secuelas de ellas.
- Primero limpié la base de datos, dejando solo las series de habla inglesa que han sido el top 1.
- Luego, busqué las series dentro de esa lista que consistían en de una segunda temporada o más (apostando que el máximo sería nueve).
- Así, vi que 21 de las 29 consistían en secuela, por lo que decidí mantener mi primera idea de visualización. 
- Hice un dataframe antes de la visualización que ordenara las semanas, si eran secuela o no, el nombre de la serie, el nombre de la temporada y la cantidad de horas vistas.
- Le pregunté a una persona que sabe de Python si conocía una librería que me ayudara a hacer lo que yo quiero e importé  matplotlib.pyplot.
- Así armé un gráfico que me dijera las veces en que una temporada secuela y no secuela haya sido la top 1 y las horas en que fue vista. 
- Finalmente instalé el programa que me permitía pasar la visualización a html.
**II. Comentar la base de datos (csv) que utilizaron, cómo la procesaron hasta dejarla lista para usar en la visualización que quieren hacer y una explicación de por qué la seleccionaron**
La base de datos trata de los contenidos que Netflix que entran en el top 10 semanal. Es una lista que contiene:
- La fecha de la semana.
- La categoría, es decir, si es una serie, una película, si es de habla inglesa, etc.
- El *weekly rank*, es decir, el número del top 10 en el que se encontraba.
- El nombre del producto
- El nombre de la temporada, en caso de ser una serie.
- La cantidad de horas semanales vista.
- Las semanas acumuladas en que se mantuvo en el top 10. 

**III. Algunos ejemplos sobre preguntas que puede responder su visualización de datos final (o el conjunto de visualizaciones que crearon)**
- ¿Netflix usa como estrategia para tener más visualizaciones las secuelas de series?
- ¿Funciona la estrategia?
- ¿Cuáles son las series más vistas de la plataforma?
- ¿Cuántas personas están viendo las series más vistas de Netflix?

