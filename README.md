# Preguntas sobre `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN` y `FULL OUTER JOIN`

## 1. ¿Por qué usaste `LEFT JOIN` para la Consulta 1 y no `INNER JOIN`? ¿Qué se perdería si usaras `INNER JOIN`?

- *INNER descarta las filas sin coincidencia, así que escondería justo los productos sin ventas que buscabas. Es como preguntar quién faltó y que te den la lista de los que vinieron.*

---

## 2. ¿Por qué usaste `RIGHT JOIN` para la Consulta 2? ¿Qué tabla está a la izquierda y cuál a la derecha en tu consulta?

- *Productos a la izquierda, ventas a la derecha. Se usa `RIGHT JOIN` para preservar toda la tabla `Ventas` y detectar la venta huérfana.*

---

## 3. ¿Qué representan los valores `NULL` en cada resultado?

### Consulta 1

**¿Qué significa que `venta_id` sea `NULL`?**

- *Un `NULL` significa que el producto nunca se vendió.*

### Consulta 2

**¿Qué significa que `producto_id` de `Productos` sea `NULL`?**

- *Un `NULL` significa que existe una venta de un producto inexistente en el catálogo.*

---

## 4. ¿Cuándo usarías `FULL OUTER JOIN` en un caso real de negocio?

- *Lo utilizaría para detectar problemas de integridad en ambos lados al mismo tiempo. Con `FULL OUTER JOIN`, en una sola consulta puedo ver los dos tipos de error.*
