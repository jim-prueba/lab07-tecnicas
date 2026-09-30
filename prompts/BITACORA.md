# Bitácora de técnicas avanzadas

Laboratorio 07: Técnicas Avanzadas de Prompting.
Herramienta de IA usada: Gemini

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta                                             | Todas con el mismo formato (Sí/No) |
| --------- | --------------- | ------------------------------------------------------------------- | ---------------------------------- |
| Zero-shot | 5               | Libre, incluyó viñetas, introducciones y explicaciones adicionales. | No                                 |
| One-shot  | 5               | Más ordenado, pero aún varió en el uso de símbolos.                 | No                                 |
| Few-shot  | 5               | Estricto y limpio, exactamente línea por línea como los ejemplos.   | Sí                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA | Muestra los pasos (Sí/No) | Correcta (Sí/No) |
| ----------- | ------------------ | ------------------------- | ---------------- |
| Directo     | S/ 318.60          | No                        | Sí               |
| Paso a paso | S/ 318.60          | Sí                        | Sí               |

_¿Por qué es útil ver el razonamiento aunque la respuesta directa haya sido correcta?_

Es útil porque permite ver el proceso lógico de la IA y detectar si el resultado correcto fue una simple coincidencia o si realmente siguió las reglas que se le fueron dadas.

## Ejercicio 4: Role prompting

| Versión        | Vocabulario (sencillo/técnico) | Usa ejemplos o código | A quién le sirve más                           |
| -------------- | ------------------------------ | --------------------- | ---------------------------------------------- |
| A. Sin rol     | General y estándar             | Ejemplo básico        | Publico general                                |
| B. Rol docente | Muy sencillo y amigable        | Cajas con etiquetas   | Estudiantes principiantes                      |
| C. Rol senior  | Técnico y avanzado             | Código fuente (Java)  | Desarrolladores o compañeros de equipo técnico |

## Ejercicio 5: Descomposición

- **Paso 1 (Requisitos):** Entregó una lista estructurada con los 5 requisitos: Gestión de productos, control de stock, registro, alertas de inventario y reportes basicos.
- **Paso 2 (Diseño):** Diseñó las clases `Producto`, `Inventario` y `Movimiento` detallando tipos de datos `String`, `int` y `double` para cada atributo.
- **Paso 3 (Código):** Generó la clase `Producto.java`, con encapsulamiento, constructor y métodos `getters/setters`.
- **Paso 4 (Mejoras):** Propuso añadir validaciones en los `setters`, implementar la interfaz para sobreescribir el método `toString()`.

## Ejercicio 6: Prompt estructurado y autocrítica

| Qué revisar                                      | Cumple (Sí/No) |
| ------------------------------------------------ | -------------- |
| ¿Tiene las 4 columnas pedidas?                   | Sí             |
| ¿Incluye el bloqueo después de 3 intentos?       | Sí             |
| ¿Incluye casos con campos vacíos?                | Sí             |
| ¿Indica qué casos agregó en la autocrítica?      | Sí             |
| ¿Hay algún caso repetido o que no tenga sentido? | No             |

### Bloque de código del prompt estructurado:

```text
<rol>Actúa como analista de pruebas de software.</rol>
<contexto>Login web con correo y contraseña. La cuenta se bloquea después de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso qué puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>
```
