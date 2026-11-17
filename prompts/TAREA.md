
# Tarea: Mi prompt avanzado

## Tarea elegida

Mi tarea elegida consiste en crear un programa de registro de notas de estudiantes utilizando Java.

El programa debe permitir ingresar el nombre de un estudiante y tres notas entre 0 y 20, calcular su promedio y determinar si esta aprobado o desaprobado. Tambien debe validar los datos ingresados para evitar errores.

Elegí esta tarea porque esta relacionada con lo que estoy aprendiendo en Desarrollo de Software y me permite comparar como mejora el codigo cuando utilizo diferentes tecnicas de prompting.


## Version 1: prompt basico

### Prompt utilizado

```text
Crea un programa en Java para registrar las notas de estudiantes.
```

### Resultado obtenido

ChatGPT genero un programa llamado RegistroNotas.java que permite registrar estudiantes, ingresar tres notas entre 0 y 20, calcular el promedio y mostrar si el estudiante esta APROBADO o DESAPROBADO.

Tambien incluyo validaciones para evitar notas incorrectas y un ciclo para registrar varios estudiantes.

### Mi observacion

Aunque utilice un prompt muy sencillo, ChatGPT genero un programa bastante completo. Sin embargo, yo no habia indicado la cantidad de notas, la escala de calificacion ni el promedio minimo para aprobar. Por eso, considero importante escribir instrucciones mas precisas para controlar mejor el resultado.

## Version 2

### Prompt utilizado

```text
Actua como profesor de programacion Java para estudiantes principiantes.

Necesito desarrollar un programa de consola para registrar notas de estudiantes.

Requisitos:
1. Solicitar el nombre del estudiante.
2. Pedir exactamente 3 notas entre 0 y 20.
3. Calcular el promedio con 2 decimales.
4. Mostrar APROBADO si el promedio es mayor o igual a 11 y DESAPROBADO si es menor.
5. Validar las notas incorrectas o fuera del rango permitido.

Formato de respuesta:
- Codigo Java completo en una clase llamada RegistroNotas.
- Explicacion sencilla de las partes principales.
- Un ejemplo de ejecucion con el estudiante Carlos y las notas 15, 12 y 14.
```

### Tecnicas agregadas

- Role prompting: asigne a ChatGPT el papel de profesor de programacion Java para principiantes.
- Prompt estructurado: especifique los requisitos del programa y el formato esperado de la respuesta.

### Resultado obtenido

ChatGPT genero la clase RegistroNotas con un programa de consola que solicita el nombre del estudiante, registra tres notas validas, calcula el promedio con dos decimales y determina si esta APROBADO o DESAPROBADO.

Tambien incluyo una explicacion sencilla de las partes del codigo y un ejemplo con Carlos y las notas 15, 12 y 14, cuyo promedio es 13.67.

### Mi observacion

En esta segunda version mejore el prompt porque indique exactamente lo que necesitaba. A diferencia de la primera version, pude controlar los requisitos y el formato de la respuesta. Tambien observe que el rol de profesor ayudo a que la explicacion fuera mas sencilla de entender.

## Version 3: prompt final

### Prompt final utilizado

```text
<rol>
Actua como desarrollador Java senior y profesor de programacion para estudiantes principiantes.
</rol>

<contexto>
Soy estudiante de Desarrollo de Software y necesito crear un programa de consola en Java llamado RegistroNotas.
</contexto>

<tarea>
Desarrolla un programa que cumpla estos requisitos:
1. Solicitar el nombre del estudiante.
2. Pedir exactamente tres notas entre 0 y 20.
3. Validar entradas no numericas, valores negativos y notas mayores que 20.
4. Calcular el promedio y mostrarlo con dos decimales.
5. Mostrar APROBADO si el promedio es mayor o igual a 11; de lo contrario, DESAPROBADO.
6. Utilizar codigo sencillo, bien organizado y con comentarios.
</tarea>

<ejemplos>
Ejemplo 1:
Nombre: Carlos
Notas: 15, 12, 14
Promedio: 13.67
Estado: APROBADO

Ejemplo 2:
Nombre: Ana
Notas: 8, 10, 9
Promedio: 9.00
Estado: DESAPROBADO
</ejemplos>

<formato>
Presenta la respuesta en este orden:
1. Codigo Java completo de RegistroNotas.java.
2. Explicacion sencilla del funcionamiento.
3. Ejemplo de ejecucion con Carlos.
4. Comprobacion breve de los requisitos.
5. Tres posibles mejoras del programa.
</formato>

<autocritica>
Antes de entregar la respuesta, revisa si el codigo cumple todos los requisitos, si las validaciones son correctas y si los ejemplos coinciden con los calculos. Corrige los errores que encuentres e indica cualquier limitacion que no hayas podido comprobar.
</autocritica>
```

### Resultado obtenido

ChatGPT genero un programa Java que permite ingresar el nombre de un estudiante, registrar tres notas validas, calcular el promedio y determinar si esta APROBADO o DESAPROBADO.

Incluyo ejemplos con Carlos y Ana, una explicacion del codigo, una comprobacion de los requisitos y tres propuestas de mejora.

### Mi observacion

En esta tercera version combine cuatro tecnicas de prompting para obtener una respuesta mas precisa y organizada. Los ejemplos ayudaron a definir los resultados esperados y la autocritica permitio identificar limitaciones del programa. Sin embargo, el codigo todavia necesita compilarse y probarse para comprobar su funcionamiento real.

## Tecnicas usadas en el prompt final

| Tecnica | Parte del prompt donde la utilice | Como ayudo al resultado |
|---------|-----------------------------------|-------------------------|
| Role prompting | Etiqueta <rol> | Permitio obtener una explicacion de Java adaptada a estudiantes principiantes. |
| Prompt estructurado | Etiquetas <contexto>, <tarea> y <formato> | Organizo los requisitos y establecio el orden de la respuesta. |
| Few-shot | Etiqueta <ejemplos> con Carlos y Ana | Mostro ejemplos de los promedios y resultados esperados. |
| Autocritica | Etiqueta <autocritica> | Solicito revisar los requisitos, las validaciones y los calculos antes de responder. |

## Evaluacion del resultado

| Criterio de evaluacion | Si/No | Observacion |
|-----------------------|-------|-------------|
| Genera el codigo completo de RegistroNotas.java | Si | Incluye la clase principal y el codigo Java solicitado. |
| Solicita el nombre y exactamente tres notas | Si | Utiliza Scanner y un ciclo for para registrar las tres notas. |
| Valida notas incorrectas o fuera de rango | Si | Utiliza try-catch y condiciones para rechazar datos invalidos. |
| Calcula correctamente los promedios de los ejemplos | Si | Carlos obtiene 13.67 y Ana obtiene 9.00. |
| Incluye explicacion, comprobacion y mejoras | Si | Presenta las secciones solicitadas y tres mejoras posibles. |
| El codigo fue compilado y ejecutado realmente | No | ChatGPT indico que reviso la logica, pero no ejecuto el programa. |

## Por que elegi estas tecnicas

Elegí estas cuatro técnicas porque considero que se complementan y me ayudan a obtener mejores resultados al trabajar con inteligencia artificial.

Utilicé Role Prompting para que ChatGPT explicara el código como un profesor de Java, utilizando un lenguaje fácil de entender. El Prompt estructurado me permitió indicar exactamente qué debía hacer el programa y cómo quería recibir la respuesta.

También utilicé Few-shot porque los ejemplos de Carlos y Ana ayudaron a mostrar los resultados que esperaba obtener. Finalmente, incorporé la autocrítica para que ChatGPT revisara sus respuestas e identificara posibles errores o limitaciones.

Preferí estas técnicas porque mi objetivo era generar un programa pequeño con requisitos claros. La descomposición habría sido más útil para un proyecto grande con varias clases, mientras que el razonamiento paso a paso habría sido más importante si el problema se centrara en cálculos complejos.

Con esta actividad aprendí que un prompt más detallado no garantiza que el código funcione perfectamente, pero sí permite controlar mejor las instrucciones y obtener respuestas más organizadas.
