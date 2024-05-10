### El **proceso** para llegar a la base de datos utilizada fue el siguiente: 

1.	Primero encontré la base de datos en Keggle https://www.kaggle.com/datasets/prasertk/netflix-subscription-price-in-different-countries que muestra por país la cantidad de contenido que tiene la plataforma, cuántas son series y cuántas son películas. También incluye el precio por suscripción dependiendo del país y el tipo de plan que tengan (del año 2021). 
2.	Luego la descargué en formato cvs y la abrí en Excel para poder mirarla claramente. Ahí me di cuenta que lo que quería hacer me funcionaba mejor en Google Colab porque no me manejo en Excel.
3.	La base originalmente tenía el código del país, lo que yo eliminé con el siguiente código 

      df = df.drop('Country_code', axis=1)
      # Mostrar el DataFrame resultante
      print(df)


4.	Con esa columna eliminada se me ocurrió que podría agregar otra columna para poder agrupar los países cuando profundicemos en nuestra investigación. Ahí cuestioné con ChatGPT cómo podía hacer eso y me dijo que primero tenía que usar la función del diccionario para que cada país se asocie a un continente.
5.	De forma manual anoté cada país con su continente de la siguiente forma

 
 diccionario_continentes = {
    
     'United Kingdom': 'Europa',
     'United States': 'América del Norte',
     'Argentina': 'América del Sur',
     'Uruguay': 'América Sur',
     'Venezuela': 'América del Sur',
     'Paraguay': 'América del Sur',
     'Peru': 'América del Sur',
     'Chile': 'América del Sur',
     'Colombia': 'América del Sur',
     'Bolivia': 'América del Sur',
     'Brazil': 'América del Sur',
     'Ecuador': 'América del Sur',
     'Australia': 'Oceanía',
     'New Zealand': 'Oceanía',
     'Austria': 'Europa',
     'Belgium': 'Europa',
     'Bulgaria': 'Europa',
     'Croatia': 'Europa',
     'Czechia': 'Europa',
     'Denmark': 'Europa',
     'Estonia': 'Europa',
     'Finland': 'Europa',
     'France': 'Europa',
     'Germany': 'Europa',
     'Gibraltar': 'Europa',
     'Greece': 'Europa',
     'Canada': 'América del Norte',
     'Guatemala': 'América Central',
     'Mexico': 'América Central',
     'Honduras': 'América Central',
     'Costa Rica': 'América Central',
     'Hong Kong': 'Asia',
     'India': 'Asia',
     'Israel': 'Asia',
     'Japan': 'Asia',
     'Malaysia': 'Asia',
     'Philippines': 'Asia',
     'Singapore': 'Asia',
     'South Korea': 'Asia',
     'Taiwan': 'Asia',
     'Turkey': 'Asia',
     'Thailand': 'Asia',
     'Hungary': 'Europa',
     'Italy': 'Europa',
     'Latvia': 'Europa',
     'Liechtenstein': 'Europa',
     'Lithuania': 'Europa',
     'Moldova': 'Europa',
     'Monaco': 'Europa',
     'Netherlands': 'Europa',
     'Norway': 'Europa',
     'Poland': 'Europa',
     'Portugal': 'Europa',
     'Romania': 'Europa',
     'Russia': 'Europa',
     'San Marino': 'Europa',
     'Slovakia': 'Europa',
     'Spain': 'Europa',
     'Sweden': 'Europa',
     'Switzerland': 'Europa',
     'Ukraine': 'Europa',
     'South Africa': 'África',
     'Ireland': 'Europa',
     'Iceland': 'Europa',
     'Indonesia': 'Asia',


6.	En ese mismo código agregue el resto del código que me sugirió ChatGPT para poder agregar una columna que tenga como nombre Continente y como ya están asociados los nombres de los países, cada continente quedó correctamente posicionado.

      # Crear una nueva columna 'Continente' basada en el diccionario de   continentes
      df['Continente'] = df['Country'].map(diccionario_continentes)

      # Ordenar los países por continente
      df = df.sort_values(by='Continente')
      
      # Mostrar el DataFrame resultante
 
 7.	Por último, me desesperé porque no sabía cómo pasar mi trabajo de Google Colab para que quede en formato cvs o formato Excel, por lo que tuve que pedirle ayuda a amigas que se manejen con el computador. Ahí me comentaron que era cosa de que ingrese un código en el mismo bloc que estaba trabajando y podía descargarlo. El código es el siguiente:

8.	Ahí debería haber puesto el nombre de mi base que en este caso era df, pero igual me funcionó usando ese código. 
9.	De ahí descargué mi base en el formato que quería y pude subirla. 


### Fuentes utilizadas:
https://www.kaggle.com/datasets/prasertk/netflix-subscription-price-in-different-countries
https://www.comparitech.com/blog/vpn-privacy/countries-netflix-cost/

### Preguntas que se pueden responder:
- ¿En qué país hay una biblioteca más amplia de contenido?
- ¿Cuáles son los países que tienen un costo más caro por suscripción?
- ¿Hay una relación entre el precio y la cantidad de contenido?

