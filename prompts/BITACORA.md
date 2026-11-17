
# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: ChatGPT

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 | Tabla con comentarios y sentimientos | Si |
| One-shot | 5 | Lista numerada con flechas y emojis | Si |
| Few-shot | 5 | Comentario seguido de flecha y clasificacion | Si |

## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Respuesta directa | S/ 318.60 | No | Si |
| Respuesta paso a paso | S/ 318.60 | Si | Si |

Mostrar los calculos paso a paso me permite entender como se obtuvo el resultado y comprobar que no haya errores.
Aunque la respuesta directa fue correcta, la segunda explicacion me dio mas confianza porque pude verificar cada operacion.

## Ejercicio 4: Role prompting

| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | Sencillo, con terminos basicos | Si, ejemplos y codigo Java | Estudiantes principiantes |
| B. Rol docente | Sencillo y didactico | Si, ejemplos cotidianos y codigo Java explicado | Estudiantes que nunca han programado |
| C. Rol senior | Tecnico y profesional | Si, codigo Java y ejemplos de sistemas reales | Desarrolladores con conocimientos de programacion |
## Ejercicio 5: Descomposicion

**Paso 1: Requisitos del sistema**

ChatGPT identifico cinco requisitos: registro de productos, gestion de productos, control de stock, registro de ventas y alertas de stock bajo.

**Paso 2: Diseno de clases**

ChatGPT propuso seis clases: Producto, Inventario, Venta, DetalleVenta, GestorVentas y AlertaStock. Tambien indico sus atributos y tipos de datos.

**Paso 3: Codigo Java**

ChatGPT genero la clase Producto.java con seis atributos privados, un constructor y sus respectivos getters y setters.

**Paso 4: Revision y mejoras**

ChatGPT propuso validar los atributos, crear metodos para aumentar y disminuir el stock y agregar un metodo para detectar stock bajo.

**Comparacion con el pedido completo**

Cuando pedi todo de una vez, ChatGPT genero directamente un proyecto llamado TiendaTec con Java Swing. En cambio, al dividir la tarea en cuatro pasos, pude revisar primero los requisitos, despues el diseno de clases, luego el codigo y finalmente sus posibles mejoras. Considero que la descomposicion me permitio tener mayor control sobre el desarrollo.


## Ejercicio 6: Prompt estructurado y autocritica

| Criterio de evaluacion | Si/No | Observacion |
|-----------------------|-------|-------------|
| Tiene las 4 columnas solicitadas | Si | Incluye ID, escenario, datos de entrada y resultado esperado. |
| Considera el bloqueo despues de 3 intentos | Si | El caso CP-05 comprueba esta regla. |
| Incluye pruebas con campos vacios | Si | Aparecen los casos CP-04, CP-09 y CP-10. |
| Indica los casos agregados en la autocritica | Si | Identifica 6 casos nuevos, del CP-07 al CP-12. |
| Hay casos repetidos o poco claros | Si | Algunos casos de campos vacios se parecen y CP-08 no muestra espacios en el dato de entrada. |

### Prompt estructurado utilizado

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>
```

### Prompt de autocritica utilizado

```text
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```


