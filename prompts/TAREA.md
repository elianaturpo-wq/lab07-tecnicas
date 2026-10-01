# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para el registro de usuarios de una aplicacion.

## Version 1: prompt basico

```text
Genera casos de prueba para el registro de usuarios de una aplicacion.
```

Tecnica agregada: Ninguna. Se uso un prompt basico y directo.

Por que: Se busco observar como respondia la IA sin darle un rol, contexto ni formato especifico.

Que mejoro o falto: La respuesta fue completa, pero la IA decidio por su cuenta la cantidad de casos, el formato y algunos escenarios. Faltaba indicar con mayor precision el contexto y la forma en que debia presentar los resultados.

## Version 2

```text
Actua como analista de pruebas de software.

Necesito evaluar el registro de usuarios de una aplicacion web que solicita nombre, correo y contrasena.

Genera 6 casos de prueba e incluye casos correctos e incorrectos.

Presenta la respuesta en una tabla con las columnas:
ID, escenario, datos de entrada y resultado esperado.
```

Tecnica agregada: Role prompting y prompt estructurado.

Por que: Se agrego un rol especifico, un contexto claro y un formato definido para orientar mejor la respuesta de la IA.

Que mejoro: La respuesta fue mas ordenada y precisa. Se obtuvieron exactamente 6 casos de prueba, con escenarios validos e invalidos, y todos fueron presentados en la tabla solicitada.

## Version 3: prompt final

```text
<rol>
Actua como analista de pruebas de software especializado en aplicaciones web.
</rol>

<contexto>
Se evaluara el registro de usuarios de una aplicacion web.
El formulario solicita nombre, correo y contrasena.
El correo debe tener un formato valido y no puede estar registrado previamente.
La contrasena debe tener minimo 8 caracteres.
</contexto>

<ejemplo>
ID: CP01
Escenario: Registro con correo invalido
Datos de entrada: nombre = Ana, correo = ana.com, contrasena = Clave123
Resultado esperado: El sistema rechaza el registro y solicita un correo valido.
</ejemplo>

<tarea>
Genera 8 casos de prueba. Incluye casos validos, invalidos y casos limite.
</tarea>

<formato>
Presenta la respuesta en una tabla con las columnas:
ID, escenario, datos de entrada y resultado esperado.
</formato>

<autocritica>
Antes de finalizar, revisa que no existan casos repetidos, que todos tengan las 4 columnas y que se incluyan casos de correo invalido, correo repetido, campos vacios y contrasena menor a 8 caracteres. Corrige cualquier problema antes de mostrar la respuesta final.
</autocritica>
```

Tecnicas agregadas: Role prompting, prompt estructurado, few-shot y autocritica.

Por que: Se agregaron estas tecnicas para dar mayor contexto a la IA, mostrarle un ejemplo del resultado esperado y pedirle que revise su propia respuesta antes de entregarla.

Que mejoro: La respuesta final fue mas completa y controlada. Los casos siguieron el formato solicitado, incluyeron situaciones validas, invalidas y limite, y se cubrieron condiciones especificas como correo invalido, correo repetido, campos vacios y contrasenas menores a 8 caracteres.

## Tecnicas usadas en el prompt final

| Tecnica             | Parte del prompt final                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Role prompting      | "Actua como analista de pruebas de software especializado en aplicaciones web."                                           |
| Prompt estructurado | Se organizo el prompt usando las etiquetas `<rol>`, `<contexto>`, `<ejemplo>`, `<tarea>`, `<formato>` y `<autocritica>`.  |
| Few-shot            | Se incluyo un ejemplo de caso de prueba con ID, escenario, datos de entrada y resultado esperado.                         |
| Autocritica         | Se pidio revisar que no existan casos repetidos, que esten las 4 columnas y que se incluyan los casos limite solicitados. |

## Evaluacion del resultado

| Criterio                                                                      | Cumple (Si / No) |
| ----------------------------------------------------------------------------- | ---------------- |
| ¿La respuesta contiene los 8 casos de prueba solicitados?                     | Si               |
| ¿Todos los casos tienen ID, escenario, datos de entrada y resultado esperado? | Si               |
| ¿Incluye casos validos, invalidos y casos limite?                             | Si               |
| ¿Incluye correo invalido y correo previamente registrado?                     | Si               |
| ¿Incluye campos vacios y contrasena menor a 8 caracteres?                     | Si               |
| ¿Los casos son diferentes y no se repiten?                                    | Si               |

## Por que elegi estas tecnicas

Elegi role prompting, prompt estructurado, few-shot y autocritica porque se adaptan bien a una tarea de casos de prueba. El rol ayudo a orientar la respuesta desde el punto de vista de un analista de software, la estructura permitio definir mejor el contexto y el formato, el ejemplo facilito que la IA mantuviera el tipo de respuesta esperado y la autocritica sirvio para revisar que no faltaran casos importantes ni se repitieran escenarios.
