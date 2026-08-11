# Casos de devolución — borrador

Extraídos de datos reales de gestión (tablero interno), con nombres inventados y sin ningún otro dato que permita identificar al cliente real. Los montos son reales; la institución y la aseguradora original se generalizan a su categoría ("banco", "casa comercial", "aseguradora original") para no dar pistas de la fuente real de los datos.

**Ojo:** el monto del crédito y las cuotas los leí de una captura de pantalla — antes de publicar, verifica que estas cifras coincidan con el tablero real. Con la segunda captura (más clara) corregí un error: había invertido cuotas pagadas con cuotas pendientes en la primera pasada. Con el dato que diste (menos cuotas pagadas = mayor devolución) los números ahora sí son consistentes entre casos.

Dos estados posibles a mostrar:
- **En proceso / firmado**: el cliente ya aceptó su devolución, está en trámite de pago.
- **Terminado**: el cliente ya recibió el pago.

Recomiendo mostrar ambos tipos en el sitio — "en proceso" también transmite movimiento actual, no solo casos cerrados.

**Formato confirmado:** tarjetas individuales para el sitio (sección de casos) + versión carrusel para redes, reutilizando el mismo contenido.

---

### Caso 1 — Rosa Elena Muñoz Paredes (nombre inventado)
- Institución: banco
- Estado: firmado, en trámite de pago
- Crédito original: $4.644.172 (56 cuotas totales)
- Saldo del crédito: $2.134.337
- Cuotas pendientes: 18 (de 56)
- Devolución calculada: $32.275
- Seguro nuevo: $8.836 (antes tenía un costo operativo de $1.613 asociado)
- Abono al cliente: $11.836

### Caso 2 — Sergio Andrés Villagra Cortés (nombre inventado)
- Institución: banco
- Estado: firmado, en trámite de pago
- Cuotas pendientes: 51
- Saldo del crédito: *no confirmado — en la captura se ve algo como $115.357.104, pero es un número inusualmente alto comparado con el resto de los casos; puede ser error de lectura. Confírmalo antes de publicarlo.*
- Devolución calculada: $5.095.190
- Seguro nuevo: $2.347.402
- Abono al cliente: $2.473.140
- *Este es el caso de mayor monto del listado — bueno para generar impacto/curiosidad si se destaca. Con 51 cuotas pendientes, es justamente un crédito recién iniciado, coherente con tener la mayor devolución.*

### Caso 3 — Camila Fernanda Reyes Muñoz (nombre inventado)
- Institución: casa comercial
- Estado: firmado, en trámite de pago
- Saldo del crédito: $7.956.552
- Cuotas pendientes: 53
- Devolución calculada: $443.872
- Seguro nuevo: $215.066
- Abono al cliente: $186.631

### Caso 4 — Pedro Pablo Gutiérrez Soto (nombre inventado)
- Institución: financiera
- Estado: firmado, en trámite de pago
- Saldo del crédito: $5.927.117
- Cuotas pendientes: 43
- Devolución calculada: $237.439
- Seguro nuevo: $147.822
- Abono al cliente: $32.515

### Caso 5 — Loreto Andrea Salinas Bravo (nombre inventado)
- Institución: banco
- Estado: **terminado, dinero ya pagado al cliente**
- Saldo del crédito: $34.757.820
- Cuotas pendientes: 50
- Devolución calculada: $1.232.319
- Seguro nuevo: $693.419
- Abono al cliente: $457.319

### Caso 6 — Manuel Ignacio Poblete Vega (nombre inventado)
- Institución: casa comercial
- Estado: **terminado, dinero ya pagado al cliente**
- Saldo del crédito: $5.884.462
- Cuotas pendientes: 18
- Devolución calculada: $139.722
- Seguro nuevo: $40.546
- Abono al cliente: $82.203

---

## Pendiente de definir con Danny
- No tengo plazos de proceso (cuántos días tomó cada caso) — si querés incluir ese dato hay que agregarlo a mano, no lo voy a inventar.
- Verifica las cifras de saldo/cuotas marcadas arriba contra el tablero real antes de publicar (lectura de captura de pantalla, riesgo de error en números largos).
- En el Caso 2 (Sergio) el saldo del crédito no quedó confirmado — el sitio (`casos.html`) por ahora solo muestra las cuotas pendientes para ese caso, sin saldo, hasta que lo confirmes.
