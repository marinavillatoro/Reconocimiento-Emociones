# Reconocimiento-Emociones
Reconocimiento emociones en habla mediante técnicas de aprendizaje automático

Se lleva a cabo un clasificador que reconoce emociones en la voz, en concreto: asco, felicidad, ira, miedo, sorpresa y tristeza.
Las características usadas son energía, cruces por cero y los primeros 12 MFCC, estas se extraen para cada trama de la señal. Luego se agrupan varias tramas, formando un segmento y se calcula la media y desviación de las características de las tramas del segmento. Por último, se calcula la media de todas las medias y desviaciones de los segmentos. Resultando un vector de 28 características para cada señal de audio.

El conjunto de muestras de características se dividen para la fase de entrenamiento y para la fase de pruebas. Luego se normalizan con StandardScaler(). 

Se evaluan los algoritmos Support Vector Machine, Gradient Boosting y Random Forest para ver con cual se optiene mejor tasa de reconocimiento.

Una vez creado el clasificador, se introducen varias bases de datos distintas a la usada en la fase de entrenamiento: CREMA-D, RAVDESS y EmoMatchSpanishDB
