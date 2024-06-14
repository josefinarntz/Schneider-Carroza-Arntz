### Tomás Schneider

1.	Buscar una base de datos acorde a la temática del trabajo, en la cual haya una relación entre variables que se asocien con el consumo de Netflix a lo largo de los años, ya sea en suscriptores, contenidos, regiones, etc. 
2.	Encontré el siguiente link: https://www.kaggle.com/datasets/mauryansshivam/netflix-ott-revenue-and-subscribers-csv-file 
3.	La abrí en Excel para poder hacer una limpieza de datos, con el fin de quedarme solo con las columnas verticales de la ganancia de streaming en diferentes locaciones del mundo junto con la columna de la fecha. 
4.	Convertí el archivo XLSX a CSV para que fuera leído en Google Colab 
5.	Importe el código:

    import pandas as pd
    #Especifica la ruta al archivo en Google Drive
    file_path = '/content/drive/My Drive/ruta/al/archivo.csv'
    #Carga el archivo CSV
    df = pd.read_csv(file_path)
    #Muestra las primeras filas del DataFrame
    df.head()
    
6.	Me apareció la tabla ordenada, como la deje en Excel. 
7.	Luego puse “generar gráficos” y me aparecieron 4 gráficos interesantes que me sirven para la entrega. 
8.	Los descargué y subí a Github.  

La base de datos escogida nos sirve para poder ver la relación entre la ganancia de streaming en diferentes regiones del mundo en la plataforma Netflix y cómo va aumentando o disminuyendo a medida que pasa el tiempo. 
Algunas preguntas que puede responder la base de datos son: 
a)	¿En qué regiones del mundo se expresó la mayor cantidad de ganancia de streaming de Netflix? 
b)	¿En qué años se puede notar una gran ganancia de streaming de Netflix? 
c)	¿Cuál fue la cantidad de streaming de Netflix que se expresó en los últimos años?
