# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.

Herramienta de IA usada: Gemini

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta              | Todas con el mismo formato (Si/No) |
| --------- | --------------- | ------------------------------------ | ---------------------------------- |
| Zero-shot | 5               | Tabla con comentario y clasificacion | Si                                 |
| One-shot  | 5               | "Comentario" -> Clasificacion        | Si                                 |
| Few-shot  | 5               | "Comentario" -> Clasificacion        | Si                                 |

En zero-shot la IA clasifico correctamente, pero eligio por su cuenta el formato de tabla. En one-shot y few-shot siguio el formato mostrado en los ejemplos, siendo few-shot el mas consistente al mantener exactamente la misma estructura en todas las respuestas.

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ------------------ | ------------------------- | ---------------- |
| Directo     | 318.60             | No                        | Si               |
| Paso a paso | 318.60             | Si                        | Si               |

Ver los pasos permite comprobar de donde sale el resultado y detectar en que parte podria existir un error.
Aunque la respuesta directa fue correcta, el procedimiento paso a paso da mayor seguridad al verificar cada calculo.

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo            | A quien le sirve mas                     |
| -------------- | ------------------------------ | -------------------------------- | ---------------------------------------- |
| A. Sin rol     | Intermedio                     | Si, ejemplos y codigo            | Publico general                          |
| B. Rol docente | Sencillo                       | Si, ejemplos faciles de entender | Estudiantes principiantes                |
| C. Rol senior  | Tecnico                        | Si, ejemplos y codigo Java       | Personas con experiencia en programacion |

El rol cambia la forma en que la IA explica un mismo tema. Con el rol docente la respuesta fue mas sencilla y didactica, mientras que con el rol senior se uso un lenguaje mas tecnico y orientado a programacion.

## Ejercicio 5: Descomposicion

## Ejercicio 5: Descomposicion

- Paso 1: La IA identifico los 5 requisitos principales del sistema de inventario.
- Paso 2: A partir de esos requisitos, propuso las clases necesarias con sus atributos y tipos de datos.
- Paso 3: Genero el codigo Java de la clase Producto con sus atributos, constructor y metodos get y set.
- Paso 4: Reviso el codigo generado y propuso tres mejoras concretas.

Comparacion: Al realizar el pedido de una sola vez, la respuesta fue mas general. En cambio, al dividir la tarea en pasos, el resultado fue mas ordenado y mantuvo una mejor relacion entre los requisitos, el diseno de las clases y el codigo generado.

## Ejercicio 6: Prompt estructurado y autocritica

| Que revisar                                      | Cumple (Si / No) |
| ------------------------------------------------ | ---------------- |
| ¿Tiene las 4 columnas pedidas?                   | Si               |
| ¿Incluye el bloqueo despues de 3 intentos?       | Si               |
| ¿Incluye casos con campos vacios?                | Si               |
| ¿Indica que casos agrego en la autocritica?      | Si               |
| ¿Hay algun caso repetido o que no tenga sentido? | No               |

La autocrítica permitió encontrar casos límite que no estaban en la primera respuesta, como campos vacíos, correo inválido y espacios en la contraseña.
