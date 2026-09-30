# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba y criterios de aceptación para **Registro de Usuarios con verificación de contraseña segura**.

## Versión 1: Prompt básico

```text
Dame casos de prueba para un registro de usuarios que pide contraseña segura.
```

- **Resultado:** Entregó una lista desordenada de ideas generales sin una estructura técnica.

## Versión 2: Aplicando Roles y Estructura (Técnicas 1 y 2)

```text
<rol>Actúa como Ingeniero de QA Automation Senior.</rol>
<contexto>Formulario de registro de usuarios. Requisitos de contraseña: mínimo 8 caracteres, una mayúscula, un número y un carácter especial.</contexto>
<tarea>Diseña los casos de prueba esenciales para este módulo.</tarea>
```

- **Resultado:** Al añadir el ROL y las etiquetas del Prompt estructurado, el lenguaje se volvió técnico y se enfocó en la lógica de las validaciones de seguridad de la contraseña.

## Versión 3: Prompt final (Combinando 4 técnicas avanzadas)

```text
<rol>Actúa como Ingeniero de QA Automation Senior experto en ciberseguridad.</rol>
<contexto>Módulo de registro de usuarios. Requisitos de la contraseña: mínimo 8 caracteres, incluir al menos 1 mayúscula, 1 número y 1 carácter especial.</contexto>
<tarea>Analiza la lógica del componente y genera casos de prueba siguiendo una metodología de partición de equivalencia. Donde pienses paso a paso en los ataque y fallos comunes.</tarea>
<ejemplos>
ID: C24S01 | Escenario: Registro exitoso | Contraseña: "Contr@s3ña" | Resultado: Usuario creado correctamente
ID: C24S02 | Escenario: Longitud insuficiente | Contraseña: "C0m@" | Resultado: Mensaje de error de longitud
</ejemplos>
<formato>Tabla Markdown con columnas: ID, Escenario, Entrada de Datos, Resultado Esperado.</formato>
```

## Técnicas usadas en el prompt final

| Parte del Prompt | Técnica Aplicada     | Objetivo                                                                                   |
| ---------------- | -------------------- | ------------------------------------------------------------------------------------------ |
| `<rol>`          | **Role prompting**   | Define el enfoque técnico al nivel esperado.                                               |
| `<ejemplos>`     | **Few-shot**         | Fuerza a la IA a seguir estrictamente el formato de la tabla sin salirse de la estructura. |
| `<tarea>`        | **Chain of Thought** | Obliga a la IA a analizar condiciones lógicas antes de listar los casos.                   |

## Evaluación del resultado

| Qué revisar                                      | Cumple (Sí/No) |
| ------------------------------------------------ | -------------- |
| ¿El prompt final combina al menos 3 técnicas?    | Sí             |
| ¿Asigna un rol específico y un formato definido? | Sí             |
| ¿Utiliza bloques estructurados?                  | Sí             |

## Por qué elegí estas técnicas

Elegí **Role prompting** y **Few-shot** porque el formato estandarizado de los reportes puedan ser automatizados o importados. La combinación de **Chain of Thought** y **Prompt estructurado** nos llega a garantizar que la IA no pase por alto los casos negativos y mantenga una separación clara entre reglas y formato.
