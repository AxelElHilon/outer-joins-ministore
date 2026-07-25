# Preguntas sobre INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN

- **1. ¿Por qué usaste LEFT JOIN para la Consulta 1 y no INNER JOIN? ¿Qué se perdería si usaras INNER JOIN?**
 - *INNER descarta las filas sin coincidencia, así que escondería justo los productos sin ventas que buscabas. Lo de "preguntar quién faltó y que te den la lista de los que vinieron".*

- **2. ¿Por qué usaste RIGHT JOIN para la Consulta 2? ¿Qué tabla está a la izquierda y cuál a la derecha en tu consulta?**
 - *Productos a la izquierda, ventas a la derecha, RIGHT para preservar ventas entera y cazar la huérfana.*

- **3. ¿Qué representan los valores NULL en cada resultado? Explicá con un ejemplo concreto de los datos qué significa que venta_id sea NULL en la Consulta 1 y que producto_id de productos sea NULL en la Consulta 2.** 
 - *En la Consulta 1 NULL es = a producto que nunca se vendió. En la segunda Consulta, el NULL es una venta de un producto inexistente en el catálogo.*

- **4. ¿Cuándo usarías FULL OUTER JOIN en un caso real de negocio?**
 - *Lo utilizaria para detectar problemas de integridad en ambos lados a la vez. Con FULL OUTER JOIN en una sola consulta puedo ver los dos tipos de error.*
