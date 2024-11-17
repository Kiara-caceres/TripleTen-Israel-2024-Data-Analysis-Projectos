# Proyecto integrado 2: Prueba A/A/B
Para este proyecto se toma el dataset general de una empresa de venta de alimentos donde se refleja el comportamiento de cada usuario que entra en una etapa o pagina a otra.
## objectivo
Comprobar si habría un impacto en el comportamiento de los usuarios al cambiar toda la fuenta de la aplicación
## Desarrollo
En el dataset se muestra 3 grupos para el analisis de un test A/A/B y tomar la mejor decisión:
* Realicé una comparativa de proporción de usuario en cada evento(embudo de venta) para cada grupo y analizar la retención en cada etapa.
* Analizé la diferencia estadística de los grupos de control para verificar la exactitud de las muestras tomando en cuenta la conversion a comprador. 
*  Utilicé la prueba de hipótesis Ttest_ind para analizar la diferencia significativa para las diferentes comparaciones entre el grupo de control y el grupo de prueba.

## SKILLS para este proyecto 
<div align='center'>
<img width="68" alt="Procesamiento de datos" src="https://github.com/user-attachments/assets/4b6c58b1-0bc3-434c-9b57-3511dcb04749">
<img width="68" alt="Analisis exploratorio" src="https://github.com/user-attachments/assets/22486eb0-e5a6-4095-9067-c435ffc839ec">
<img width="68" alt="Analisis estadistico" src="https://github.com/user-attachments/assets/54044c92-a726-408c-84dc-8b71f25475e5">
</div>

* Analisis de negocio
* Explicacion de datos


### Descripción del proyecto
Trabajas en una empresa emergente que vende productos alimenticios. Debes investigar el comportamiento del usuario para la aplicación de la empresa.

Primero, estudia el embudo de ventas. Descubre cómo los usuarios y las usuarias llegan a la etapa de compra. ¿Cuántos usuarios o usuarias realmente llegan a esta etapa? ¿Cuántos se atascan en etapas anteriores? ¿Qué etapas en particular?

Luego, observa los resultados de un test A/A/B. (Sigue leyendo para obtener más información sobre los test A/A/B). Al equipo de diseño le gustaría cambiar las fuentes de toda la aplicación, pero la gerencia teme que los usuarios y las usuarias piensen que el nuevo diseño es intimidante. Por ello, deciden tomar una decisión basada en los resultados de un test A/A/B.

Los usuarios se dividen en tres grupos: dos grupos de control obtienen las fuentes antiguas y un grupo de prueba obtiene las nuevas. Descubre qué conjunto de fuentes produce mejores resultados.

Crear dos grupos A tiene ciertas ventajas. Podemos establecer el principio de que solo confiaremos en la exactitud de nuestras pruebas cuando los dos grupos de control sean similares. Si hay diferencias significativas entre los grupos A, esto puede ayudarnos a descubrir factores que pueden estar distorsionando los resultados. La comparación de grupos de control también nos dice cuánto tiempo y datos necesitaremos cuando realicemos más tests.

Utilizarás el mismo dataset para el análisis general y para el análisis A/A/B. En proyectos reales, los experimentos se llevan a cabo constantemente. El equipo de análisis estudia la calidad de una aplicación utilizando datos generales, sin prestar atención a si los usuarios y las usuarias participan en experimentos.

Descripción de los datos
Cada entrada de registro es una acción de usuario o un evento.

EventName: nombre del evento.
DeviceIDHash: identificador de usuario unívoco.
EventTimestamp: hora del evento.
ExpId: número de experimento: 246 y 247 son los grupos de control, 248 es el grupo de prueba.
