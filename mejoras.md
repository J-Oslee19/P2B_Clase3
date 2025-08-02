# Archivo de Mejoras – Simulador de Negocio de Comida Rápida
**Autor_1:** Jeferson Oslee Cermeño Pineda  
**Autor_2:** Elder Ezequiel Perez y Perez
**Fecha:** [02/08/2025]  
**Total de mejoras implementadas:** 6

---

## Mejora #1:
**Ubicación:** InventarioService.java  
**Descripción del cambio:** Se agregó una verificación antes de registrar productos, para evitar que se agreguen productos con nombres duplicados (ignorando mayúsculas/minúsculas).  
**Justificación:** Garantiza la integridad del inventario y evita confusión en ventas por productos repetidos con diferente ID.

---

## Mejora #2:
**Ubicación:** Pedido.java y DatabaseManager.java  
**Descripción del cambio:** Se agregó el campo `fecha` de tipo `LocalDateTime` en la clase `Pedido`, y se modificó la tabla `pedidos` para incluir un campo `fecha_hora` en la base de datos.  
**Justificación:** Permite registrar la fecha y hora exactas en que se realiza un pedido, útil para trazabilidad y reportes por fecha.

---

## Mejora #5:
**Ubicación:** Producto.java  
**Descripción del cambio:** Se reforzó la validación en el método `reducirStock` y en el `setStock` para evitar que el stock llegue a valores negativos.  
**Justificación:** Previene errores de lógica y asegura el control del inventario evitando inconsistencias.

---

## Mejora #6:
**Ubicación:** Producto.java y InventarioService.java  
**Descripción del cambio:** Se validó que el precio sea mayor a cero en el constructor y en el setter. También se validó que la cantidad ingresada al vender sea positiva.  
**Justificación:** Protege el sistema de valores incorrectos que podrían causar errores de cálculo o permitir manipulaciones no deseadas.

---

## Mejora #7:
**Ubicación:** Main.java  
**Descripción del cambio:** Se agregó una nueva opción al menú para mostrar un resumen de inventario con el nombre, precio y stock actual de cada producto.  
**Justificación:** Mejora la experiencia del usuario permitiendo consultar rápidamente el estado del inventario desde el menú principal.

---

## Mejora #8:
**Ubicación:** Main.java e InventarioService.java  
**Descripción del cambio:** Se implementó una opción en el menú para eliminar productos por ID, solicitando confirmación previa antes de proceder.  
**Justificación:** Evita eliminaciones accidentales y mejora la seguridad y control del inventario por parte del usuario.

---

