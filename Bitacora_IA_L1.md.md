
**Nombre:** Sebastian Bedoya
**Equipo / especie:** Tuhuy
**Asistente usado:** (Claude, versión: Sonnet 5.5/Gemini, versión: Neón).

Una entrada por cada uso. La última columna es la que vale: cómo lo comprobaron.

| #   | Qué pedí (el texto exacto)                                                                                    | Qué salió (un fragmento)                                                                    | Qué acepté, corregí o rechacé, y por qué                                                                                                      | Cómo lo comprobé                                                                                                 |
| --- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| 1   | Le pedí a Claude que me explicara los códigos de la sesión 1 desde la parte 5 y qué códigos tenia que cambiar | me dio leer_numero y columna y los códigos de la secció                                     | Acepté el código y lo pegué en las celdas con # TU CÓDIGO AQUÍ.                                                                               | Ejecuté las celdas en orden y las pruebas no dieron error.                                                       |
| 2   | le mande la foto del error nameError de la seccion 2 y le pedi ayuda                                          | me dio las ocho funciones juntas (es_primo, rectangulos etc.) para la celda "Peguen aqui".  | Habia pegado el codigo en las celdas de pruebas, no en la de arriba. Lo moví, agregue el "import matplotlip.pyplot as plt" y ejecuté en orden | Corrí la celda de pruebas y salió "✔ Herramientas listas. Especie de base 6".                                    |
| 3   | Le pedí que me explicara por qué en base 6 se pasa del 5 al 10.                                               | Me explicó que no se salta nada: el seis se escribe 10 ("un grupo de seis y cero sueltos"). | Acepté la explicación porque ya la había deducido yo con 1, 2, 3, 4, 5, 10, 11, 12.                                                           | Comparé la tabla con mi propio conteo.                                                                           |
| 4   | Le pedí el código del conteo, las secciones del mensaje y ensamblar.                                          | Me dio codificar_conteo, un ejemplo de secciones 2 y 3 y ensamblar.                         | Acepté el ejemplo como mi mensaje. Al pegar, quedó una copia suelta del código y la IA me dijo que borrara toda la celda y pegara de nuevo.   | Ejecuté y salió el dibujo del mensaje (323 bits, 17 × 19).                                                       |
| 5   | Le pedí el código de las funciones del canal (ruido, paridad, repetición, votar).                             | Me dio los cuerpos de las funciones.                                                        | Tres de ellas quedaron con líneas rojas por el sangrado. Pegué las funciones completas, no solo el cuerpo.                                    | Ejecuté la celda y la de "medir" dio los resultados (972 con error, 966 detectadas, 904 de 1000 con repetición). |
| 6   | Me ayudó a ordenar P5.                                                                                        | La IA dijo 10 bits dañados al enviarlo 3 veces.                                             | Rechacé el 10 y mantuve 9, porque yo seguí la regla de multiplicar por 3: 3 × 3 = 9.                                                          | Hice la cuenta: 323 × 0,01 ≈ 3 y 3 × 3 = 9.                                                                      |
| 7   | Le dije a la IA que P4 y P5 no las había respondido en Obsidian.                                              | La IA había dicho que sí las había respondido allí.                                         | Corregí a la IA: lo de Obsidian era el Momento 1 de la sesión 1, no de la sesión 2.                                                           | Lo comprobé con mi propia memoria de lo que había hecho.                                                         |

## Experimento estrella (sesión 1)

Le di al asistente los 1 679 bits sin decirle qué eran y le pedí que los descifrara.

- **Lo que respondió**: El asistente respondió que en 1679 bits fue el mensaje que se envió en 1974 por una transmisión de radio al espacio era un mensaje en forma de rectángulo para que ordenarán 23 * 73 1679 era un número semiprimo por lo tanto el mensaje iba ordenado de 23 filas y 73 columnas
- **¿Descifró o reconoció?** ¿Cómo lo sé? ¿Qué prueba propongo para distinguirlo? Claramente lo descifró y reconoció de que se trataba explícitamente de ese mensaje en la prueba que propuso para distinguirlo fue eso la descomposición del número como era números de mi primo entonces su descomposición eran entre los dos números primos en este caso el 23 y el 73 los cuales iban a armar una imagen por medio de una cuadrícula coloreada donde se iba a mostrar una imagen

## Contraprueba (sesión 2)

Le di el mensaje de la especie ______ (que no está en internet) y le pedí que lo tradujera.

- Ancho que dedujimos: 19 columnas, porque el mensaje tiene 1311 bits (3 × 19 × 23); al quitar la repetición quedan 437 bits (19 × 23), y con 19 columnas las figuras se ven alineadas, mientras que con 23 se ve como ruido.
- Base que dedujimos: 8, porque el conteo de arriba va 1, 2, 3, 4, 5, 6, 7 y luego vuelve a empezar con 10, 11, 12. El último dígito es el 7, y 7 + 1 = 8. Cada dígito usa 3 bits, que da justo 8 valores (0 a 7).
- Protección que creemos que usaron: repetición, porque 422 de 437 grupos de tres bits eran iguales (000 o 111), y al votar queda el mensaje de 437 bits.

## Conclusión (cinco líneas)

Gemini no inventó una traducción del mensaje: dijo que no podía darla con seguridad y propuso dibujarlo probando anchos. Reconoció la forma del mensaje pero no entendió la protección ni el significado. Claude se equivocó varias veces: me contradijo en lo que ya había respondido y me sugirió una razón que no era la correcta, y lo detecté yo mismo comprobando. Aprendí que el asistente puede ayudarme a avanzar, pero lo que dice hay que probarlo con código o con una cuenta. Voy a desconfiar de él cuando me dé una respuesta muy segura que no pueda comprobar.