# Proyecto sprint 10: Decisiones de negocio basadas en datos
Para una tienda online, se toma 3 dataset: Hipotesis, ordenes y visitas.Basado en eso se elegirá la hipotesis prioritaria para realizar la prueba test A/B y analizar si aumenta nuestros ingresos con este cambio.
## Objetivo
* Elegir y poner a prueba la hipotesis correcta.
* Detectar si estos cambio aumenta nuestros ingresos

## Desarrollo
* Apliqué el framework Ice, Rice para elegir la prioridad de hipotesis y realizar la prueba test A/B.
* Compilé y analicé los ingresos y tamaño promedio acumulado de cada grupo.
* Comparé la tasa de conversion en una graficar y resaltar alguna anomalia.
* Realicé la prueba no parametrica para comprobar una diferencia significativa entre ambos grupos.

### Descripción del proyecto
Contexto
Eres analista en una gran tienda online. Junto con el departamento de marketing has recopilado una lista de hipótesis que pueden ayudar a aumentar los ingresos.

Tienes que priorizar estas hipótesis, lanzar un test A/B y analizar los resultados.

Descripción de los datos
Datos utilizados en la primera parte del proyecto '/datasets/hypotheses_us.csv'

* Hypotheses: breves descripciones de las hipótesis.
* Reach: alcance del usuario, en una escala del uno a diez.
* Impact: impacto en los usuarios, en una escala del uno al diez.
* Confidence: confianza en la hipótesis, en una escala del uno al diez.
* Effort: los recursos necesarios para probar una hipótesis, en una escala del uno al diez. Cuanto mayor sea el valor Effort, más recursos requiere la prueba.

Datos utilizados en la segunda parte del proyecto '/datasets/orders_us.csv'

* transactionId: identificador de pedido.
* visitorId: identificador del usuario que realizó el pedido.
* date: fecha del pedido.
* revenue: ingresos del pedido.
* group: el grupo del test A/B al que pertenece el usuario.

/datasets/visits_us.csv
* date: la fecha.
* group: grupo de la prueba A/B.
* visits: el número de visitas en la fecha especificada en el grupo de pruebas A/B especificado.
  
Asegúrate de preprocesar los datos. Es posible que haya errores en los datasets originales; por ejemplo, algunos de los visitantes podrían haber entrado tanto en el grupo A como en el grupo B.
