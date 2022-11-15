---
layout: post
title: "Importancia del Número de Muestras en los Modelos Estadísticos"
date: 2021-09-03
author: Gerardo Marx
categories: society projects statistics articles
---

![](/assets/standard_normal.png)

# Modelos Estadísticos

Los **modelos estadísticos** juegan un papel muy importante en la estimación del comportamiento de diferentes fenómenos en la naturaleza; uno muy recurrente actualmente son el número de casos de infección en una pandemia.

Sin embargo, los **modelos estadísticos** dependen de una correcta alimentación de datos y el número de datos. Uno de los modelos más básicos en la estadística es el denominado *Maximum Likelihood Estimator* (MLE). Este estimador, a grandes rasgos, depende de dos parámetros principalmente: la media $$\mu$$ y la desviación estándar $$\sigma$$.

# La Media y Desviación Estándar

Los parámetros, la media y la desviación estándar, son los elementos que describen principalmente al modelo MLE. Sin embargo, estos dos parámetros depende en gran medida del números de muestras $$ n $$ que se tomara representar al fenómeno bajo estudio. De hecho, teóricamente estos parámetros tienden a un valor práctico con forme $$ n $$ tiende a infinito; en la práctica a un número grande de muestras.

Precisamente es en este punto donde la mayoría de los modelos tienen un sesgo. Pensemos en una encuesta de videojuegos que solo considera personas de la tercera edad, esto implicaría que el enfoque de la encuesta tendría un sesgo en cuanto a la aleatoriedad de los las muestras. Por otro laso, piensa que sí se considera un rango amplio de edades; entre 10 a 50 años. No obstante, solo se encuestan 10 personas. Estas 10 personas no representan el **universo** de la gente que juega videojuegos. 

# Importancia del número de muestras en un modelo

De aquí se deriva entonces que un modelo estadístico depende mucho de la forma en que se recolectan los datos (muestreo) y el número de datos que se recolecta. Algo similar, con un enfoque en materiales, se estudio en el trabajo de investigación denominado "A Sample Size Statistical Analysis and Its Impact on Decarburization Measurements Metrics", publicado en la revista JOM de la revista Springer puede ser consultado en la siguiente liga: [artículo completo](https://link.springer.com/epdf/10.1007/s11837-021-04697-9?sharing_token=bjxCrGusENyfai0hRN0rzve4RwlQNchNByi7wbcMAY46q5t_39YoiHFwMeAGCGLOe4_awl_y9rRPQNdCOdChhvE0RPMQyA8fH979Lr1YLRM-LBT5RHMueHxisW7rCfrwIxRPT-sQQdhWulWBJPbpUhIC_Z8n6yGU_pXTvp5zP8Y%3D). 

A manera de conclusión, es importante considerar los efectos que los parámetros de la media y desviación estándar, sufren por el número de muestras y los métodos que recolección de datos. Es decir, es importante observar la dependencia de los parámetros en función que cuántas y a quienes encuestas.


