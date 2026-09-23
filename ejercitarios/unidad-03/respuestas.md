# Respuestas — Ejercitario Unidad 03

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · El significado de proceso

**1. Define en tus propias palabras qué es un proceso de software.**

Un proceso de software es un conjunto organizado de actividades y tareas que se realizan para transformar una necesidad o idea del usuario en un producto de software funcional. Permite planificar, desarrollar, probar y entregar un sistema siguiendo una orden establecido.


**2. Explica la diferencia entre proceso, metodología y modelo de proceso, con un ejemplo de cada uno.**

Proceso: Es el conjunto general de actividades que indican qué se debe hacer para desarrollar software.

Ejemplo: Comunicación, planificación, diseño, construcción y entrega.

Metodología: Es la forma específica o conjunto de técnicas utilizadas para realizar el proceso.

Ejemplo: Metodología scrum para organizar un proyecto mediante equipos, reuniones y entregas pequeñas.

Modelo de proceso: Es una representación de cómo se organizan las actividades del proceso.

Ejemplo: Modelo cascada, donde cada fase se realiza una después de otra.


**3. Enumera las cinco actividades genéricas del marco de trabajo de Pressman.**

1. Comunicación.
2. Planeación.
3. Modelado.
4. Construcción.
5. Despliegue.

**4. Menciona dos actividades "de la sombrilla" y explica por qué se dice que "cubren" todo el proceso.**

Dos actividades de la sombrilla son:
- Gestión de riesgos.
- Aseguramiento de calidad.

Se llama así porque se realizan durante todas las etapas del desarrollo del software y acompañan al proceso completo, no solamente una fase específica.

## Tema 2 · Modelos de proceso

**5. Completen el siguiente cuadro indicando en qué situación conviene usar cada modelo de proceso visto en clase.**

| Modelo | ¿Cuándo conviene usarlo? |
|---|---|
| Cascada | Cuando los requisitos están bien definidos desde el inicio y no se esperan muchos cambios.|
| Incremental | Cuando se necesita entregar funcionalidad poco a poco hasta completar el sistema.|
| Evolutivo (prototipos) | Cuando los requisitos no están claros y el cliente necesita visualizar una versión inicial.|
| Evolutivo (espiral) | Cuando el proyecto tiene alto riesgo y se necesita analizar riesgos contantemente.|
| Concurrente | Cuando varias actividades del desarrollo deben realizarse em paralelo. |

**6. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Modelo de proceso | Característica principal |
|---|---|
| A. Cascada | _2_ |
| B. Incremental | _4_ |
| C. Prototipos | _5_ |
| D. Espiral | _1_ |
| E. Concurrente | _3_ |

1. Combina iteración con análisis explícito de riesgo en cada vuelta.
2. Enfoque secuencial y lineal, actividad por actividad.
3. Representa actividades ocurriendo en paralelo, no en secuencia estricta.
4. Entrega el producto en porciones funcionales cada vez más completas.
5. Construye una versión parcial y rápida para validar requisitos poco claros.

**7. Elegí un proyecto de software (hipotético o real) y justificá qué modelo de proceso usarías para desarrollarlo y por qué.**

Proyecto: Aplicación móvil para administrar turnos de una clínica.

Elegiría el modelo incremental, porque permite desarrollar primero las funciones principales (registro de pacientes y turnos) y luego agregar nuevas características. Así el cliente puede utilizar partes del sistema mientras continúa el desarrollo.

## Tema 3 · Iteración de procesos

**8. Explica con tus palabras por qué la mayoría de los procesos modernos son iterativos.**

La mayoría de los procesos modernos son iterativos porque permiten desarrollar un sistema por etapas, realizando mejoras y correcciones en cada ciclo. De esta manera, se pueden detectar errores, incorporar cambios en los requisitos y obtener versiones mejoradas del software sin tener que esperar hasta el final del proyecto.


**9. Menciona una ventaja y una desventaja de trabajar con iteraciones cortas.**

Ventaja: Permiten detectar errores rápidamente y recibir comentarios para mejorar el sistema en poco tiempo.
Desventaja: Pueden generar más trabajo de planificación y adaptación, especialmente cuando los requisitos cambian constantemente

## Tema 4 · Especificación, diseño, implementación, validación y evolución

**10. Describan brevemente qué implica cada una de las cuatro actividades fundamentales del proceso de software, según Sommerville.**

| Actividad | Qué implica |
|---|---|
| Especificación |Define qué debe hacer el sistema y cuáles son sus requisitos y restricciones |
| Diseño e implementación | Consiste en diseñar la estructura del sistema y desarrollar el software que lo hará funcionar.|
| Validación |Comprueba que el sistema cumple con los requisitos y funciona correctamente |
| Evolución | Consiste en modificar y adaptar el software después de su desarrollo para incorporar cambios, mejoras o nuevas necesidades.|

**11. Relaciona estas cuatro actividades con las cinco fases del ciclo del software vistas en la Unidad 1 (análisis, diseño, implementación, pruebas, mantenimiento). ¿En qué se parecen y en qué se diferencian?**

Se corresponden casi directamente: especificación ↔️ análisis, diseño e implementación ↔️ diseño e implementación (aquí se fusionan en una sola actividad), validación ↔️ pruebas, y evolución ↔️ mantenimiento.
¿En qué se parecen?
Ambos modelos describen actividades necesarias para desarrollar y mantener un sistema de software. En los dos se consideran los requisitos, el diseño, la construcción del software, las pruebas y los cambios posteriores.
¿En qué se diferencian?
La principal diferencia es que el modelo de Sommerville agrupa algunas actividades. Por ejemplo, une diseño e implementación en una sola actividad, mientras que el otro ciclo las presenta como fases separadas. Además, Sommerville utiliza evolución para representar los cambios y mejoras que se realizan durante la vida del software.

## Tema 5 · Herramientas y técnicas para modelado de procesos

**12. Menciona dos formas de representar un proceso (no un sistema) y explica brevemente cada una.**

* Diagrama de flujo: representa gráficamente los pasos de un proceso utilizando símbolos y flechas para mostrar el orden en que se realizan las actividades.
* Diagrama de actividad: permite representar las actividades que se realizan en un proceso, mostrando el orden de las acciones y las decisiones que pueden ocurrir durante el mismo.


**13. ¿Qué es un patrón de proceso? Da un ejemplo hipotético de un problema recurrente en un proyecto y su solución.**
Un patrón de proceso es una solución que puede utilizarse para resolver un problema que aparece de manera frecuente durante el desarrollo de un proyecto.

Ejemplo: un problema recurrente puede ser que los requisitos cambien constantemente durante el desarrollo del sistema. Una posible solución sería revisar y aprobar los requisitos con el cliente antes de comenzar cada etapa, y registrar formalmente cualquier cambio que se solicite.


---

## Tema 6 · Ayuda automatizada al proceso

**14. Explica la diferencia entre herramientas Upper-CASE y Lower-CASE.**

Las herramientas Upper CASE (Mayúsculas) se utilizan principalmente en las etapas iniciales del desarrollo, como la planificación, el análisis y el diseño del sistema.

Las herramientas Lower CASE (Minúsculas) se utilizan principalmente en las etapas posteriores, como la programación, las pruebas y el mantenimiento del software.

También existen las herramientas I-CASE, que integran funciones de las herramientas Upper CASE y Lower CASE y pueden utilizarse durante diferentes etapas del ciclo de desarrollo.


**15. Menciona tres herramientas que consideren CASE (de su propia experiencia o investigación) y clasifíquenlas según la categoría a la que pertenecen.**

| Herramienta | Categoría (Upper / Lower / I-CASE) |
|---|---|
|Draw.io	 | Upper CASE|
|Visual Studio Code | Lower CASE|
|Enterprise Architect | I-CASE|

**16. Reflexión final:** de los modelos de proceso vistos en esta unidad, ¿cuál elegirían para un proyecto personal? Justifiquen su elección considerando el tamaño del proyecto, el tiempo disponible y el nivel de certeza sobre los requisitos.

Para un proyecto personal elegiría un modelo iterativo, porque permite desarrollar el sistema por partes y realizar mejoras durante el proceso. Lo utilizaría especialmente para un proyecto de tamaño pequeño o mediano, donde se dispone de un tiempo limitado y los requisitos pueden cambiar a medida que se conoce mejor lo que necesita el usuario.

Por ejemplo, si desarrollara un sistema para controlar el inventario de un pequeño negocio, primero podría crear las funciones principales y luego agregar mejoras según las necesidades que vayan apareciendo.
