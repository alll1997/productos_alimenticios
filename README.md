# Productos Alimenticios

### Desafio
En una empresa emergente que vende productos alimenticios. Investigar el comportamiento del usuario para la aplicación de la empresa.
Estudiar el embudo de ventas y descubrir cómo los usuarios y las usuarias llegan a la etapa de compra. 
¿Cuántos usuarios o usuarias realmente llegan a esta etapa? ¿Cuántos se atascan en etapas anteriores? ¿Qué etapas en particular?


Observar los resultados de un test A/A/B. Al equipo de diseño le gustaría cambiar las fuentes de toda la aplicación, pero la gerencia teme que los usuarios y las usuarias piensen que el nuevo diseño es intimidante. Por ello, se decide tomar una decisión basada en los resultados de un test A/A/B.

Los usuarios se dividen en tres grupos: dos grupos de control obtienen las fuentes antiguas y un grupo de prueba obtiene las nuevas. Descubrir qué conjunto de fuentes produce mejores resultados.

Crear dos grupos A tiene ciertas ventajas. Establecer el principio de que solo confiaremos en la exactitud de nuestras pruebas cuando los dos grupos de control sean similares. Si hay diferencias significativas entre los grupos A, esto puede ayudar a descubrir factores que pueden estar distorsionando los resultados. La comparación de grupos de control también nos dice cuánto tiempo y datos necesitaremos cuando realicemos más tests.

Utilizar el mismo dataset para el análisis general y para el análisis A/A/B. El equipo de análisis estudia la calidad de una aplicación utilizando datos generales, sin prestar atención a si los usuarios y las usuarias participan en experimentos

**SKILLS: Preprocesamiento de datos - Análisis exploratorio - Análisis estadistico - Análisis de negocio - Explicación de datos**

### Contenido
1.  Abrir el archivo de datos y leer la información general
2.  Preparar los datos para el análisis
  -  Cambiar el nombre de las columnas
  -  Comprobar tipos de datos, duplicados y valores ausentes.
  -  Agrega una columna de fecha y hora y una columna separada para las fechas
3.  Estudiar y comprobar los datos
  -  ¿Cuántos eventos hay en los registros?
  -  ¿Cuántos usuarios y usuarias hay en los registros?
  -  ¿Cuál es el promedio de eventos por usuario?
  -  ¿Qué periodo de tiempo cubren los datos? ¿Qué periodo representan realmente los datos?
  -  ¿Perdiste muchos eventos y usuarios al excluir los datos más antiguos?
  -  Asegúrate de tener usuarios y usuarias de los tres grupos experimentales.
4.  Estudiar el embudo de eventos
  -  Observa qué eventos hay en los registros y su frecuencia de suceso. Ordénalos por frecuencia.
  -  Encuentra la cantidad de usuarios y usuarias que realizaron cada una de estas acciones. Ordena los eventos por el número de usuarios y usuarias. Calcula la proporción de usuarios y usuarias que realizaron la acción al menos una vez.
  -  ¿En qué orden crees que ocurrieron las acciones? ¿Todas son parte de una sola secuencia? No es necesario tenerlas en cuenta al calcular el embudo.
  -  Utiliza el embudo de eventos para encontrar la proporción de usuarios y usuarias que pasan de una etapa a la siguiente. (Por ejemplo, para la secuencia de eventos A → B → C, calcula la proporción de usuarios en la etapa B a la cantidad de usuarios en la etapa A y la proporción de usuarios en la etapa C a la cantidad en la etapa B).
  -  ¿En qué etapa pierden más usuarios y usuarias?
  -  ¿Qué porcentaje de usuarios y usuarias hace todo el viaje desde su primer evento hasta el pago?
5.  Estudiar los resultados del experimento
  -  ¿Cuántos usuarios y usuarias hay en cada grupo?
  -  Tenemos dos grupos de control en el test A/A, donde comprobamos nuestros mecanismos y cálculos. Observa si hay una diferencia estadísticamente significativa entre las muestras 246 y 247.
  -  Selecciona el evento más popular. En cada uno de los grupos de control, encuentra la cantidad de usuarios y usuarias que realizaron esta acción. Encuentra su proporción. Comprueba si la diferencia entre los grupos es estadísticamente significativa. Repite el procedimiento para todos los demás eventos (ahorrarás tiempo si creas una función especial para esta prueba). ¿Puedes confirmar que los grupos se dividieron correctamente?
  -  Haz lo mismo para el grupo con fuentes alteradas. Compara los resultados con los de cada uno de los grupos de control para cada evento de forma aislada. Compara los resultados con los resultados combinados de los grupos de control. ¿Qué conclusiones puedes sacar del experimento?
  -  ¿Qué nivel de significación has establecido para probar las hipótesis estadísticas mencionadas anteriormente? Calcula cuántas pruebas de hipótesis estadísticas has realizado. Con un nivel de significancia estadística de 0.1, uno de cada 10 resultados podría ser falso. ¿Cuál debería ser el nivel de significación? Si deseas cambiarlo, vuelve a ejecutar los pasos anteriores y comprueba tus conclusiones.
6.  Conclusión

Para visualizar del analisis, mirarlos en el [Notebook](https://github.com/alll1997/portafolio/blob/main/Productos%20Alimenticios/codigo%20de%20analisis.ipynb)
<img src="https://github.com/alll1997/portafolio/blob/main/Productos%20Alimenticios/image.png" width=1000/>

## Conclusiones
- Los eventos presentes en el análisis estaban presente en una cadena donde 'MainScreenAppear' se presenta como el evento más popular y el primer paso de los eventos, 'PaymentScreenSuccessful', 'CartScreenAppear' y 'OffersScreenAppear'; por aparte se encuentra el evento 'Tutorial'; pese que el análisis inicio el '25 de Julio del 2019 04:43:36', pero se estabilizó el  '01 de Agosto del 2019 00:07:28', a su vez el promedio de eventos por usuarios es de 32.28.
- La perdida del principio al final de la secuencia de evento fue de un 47.7% en las 4 etapas, teniendo un 48.13% de conversión.
- En el A|A|B test, en las 12 pruebas realizadas con la prueba Mann-Whitney y Z-test de proporciones, mantienen los resultados en las desviaciones estándar y no se puede rechazar la significancia estadística de la diferencia entre los grupos de comparación  ya sea que el valor alpha sea el valor estándar (0.05) o difiera en un 0.012.
- Las varianzas de los dos grupos son iguales y no se puede rechazar la significancia estadística de la diferencia entre los grupos de comparación, ya sea que el valor alpha sea el valor estándar (0.05) o difiera (0.1 o 0.09).
- Con el preprocesamiento y las pruebas realizadas de evidencia que los datos no están distorsionados para la análisis de las variaciones y el impacto a generar en la empresa
