# Respuestas — Ejercitario Unidad 04


## Tema 1 · El proceso de requerimientos

**1. Define en tus propias palabras qué es la ingeniería de requerimientos.**

La ingeniería de requerimientos es el proceso de identificar, analizar, organizar y documentar lo que los usuarios necesitan de un sistema. También permite comprobar que los requisitos estén claros y que el sistema que se desarrolle cumpla con esas necesidades.


**2. Explica la diferencia entre "requerimiento", "especificación de requisitos" e "ingeniería de requisitos", con un ejemplo de cada uno.**

* Requerimiento: es una necesidad o condición que el sistema debe cumplir.
    Ejemplo: El sistema debe permitir registrar nuevos productos.
  
* Especificación de requisitos: es la descripción detallada y organizada de los requisitos que debe cumplir el sistema.
    Ejemplo: Se especifica que para registrar un producto se debe ingresar su nombre, categoría, precio y cantidad disponible.
  
* Ingeniería de requisitos: es el proceso mediante el cual se identifican, analizan, documentan y validan los requisitos del sistema.
    Ejemplo: Entrevistar a la dueña de un minisúper para conocer cómo controla actualmente sus productos y determinar qué funciones debería tener el sistema de inventario.

## Tema 2 · Tipos de requerimientos

**3. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Tipo de requerimiento | Descripción |
|---|---|
| A. Funcional | _2_ |
| B. No funcional | _3_ |
| C. Del dominio | _1_ |

1. Proviene de las reglas o restricciones propias del área o dominio de negocio.
2. Describe una función o servicio concreto que el sistema debe realizar.
3. Restringe cómo debe comportarse el sistema (desempeño, seguridad, usabilidad, etc.).

**4. Completen el siguiente cuadro comparando los requerimientos de usuario y los requerimientos de sistema.**

| Aspecto | Requerimientos de usuario | Requerimientos de sistema |
|---|---|---|
| Audiencia principal | Usuarios y clientes del sistema	| Desarrolladores, diseñadores y equipo técnico|
| Nivel de detalle | General y fácil de comprender| Más detallado y específico|
| Lenguaje utilizado |Lenguaje natural, evitando términos técnicos	 | Lenguaje más técnico y preciso|

**5. Elegí un sistema que conozcas (una app, una plataforma, un sistema de tu universidad o trabajo) y da un ejemplo propio de un requerimiento funcional y uno no funcional para ese mismo sistema.**

Sistema elegido: Sistema de Control de Inventario para un Minisúper

Requerimiento funcional:
El sistema debe permitir registrar un producto indicando su nombre, categoría y cantidad disponible.

Requerimiento no funcional:
El sistema debe tener una interfaz sencilla y fácil de utilizar para que la persona encargada del minisúper pueda realizar las operaciones de inventario sin dificultad.


## Tema 3 · Características de los requerimientos

**6. Completen el siguiente cuadro indicando qué pregunta permite verificar cada característica de un buen requerimiento.**

| Característica | Pregunta que permite verificarla |
|---|---|
| Correcto | ¿El requerimiento refleja realmente una necesidad del usuario o del sistema?|
| No ambiguo |	¿Puede entenderse de una sola manera? |
| Completo | ¿Contiene toda la información necesaria para entender qué debe hacer el sistema? |
| Verificable | ¿Se puede comprobar mediante una prueba o revisión si el requerimiento se cumple? |

**7. Tomá el requerimiento "El sistema debe ser rápido" y reescribilo de forma que cumpla con las características de un buen requerimiento vistas en clase.**

El sistema debe responder a una consulta de búsqueda de pacientes en un tiempo máximo de 2 segundos, considerando una base de datos de hasta 10.000 registros y una carga de hasta 50 usuarios concurrentes.


## Tema 4 · Obtención y análisis de requerimientos

**8. Enumera las cuatro etapas del ciclo de obtención y análisis de requerimientos vistas en clase.**

1. Descubrimiento.
2. Clasificación y organización.
3. Priorización y negociación.
4. Especificación y documentación.

**9. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Técnica de obtención | Situación en que conviene usarla |
|---|---|
| A. Entrevistas | 3___ |
| B. Observación | 1___ |
| C. Talleres / workshops | 2___ |

1. Cuando el usuario no puede verbalizar fácilmente lo que necesita.
2. Cuando hay varios interesados con visiones distintas que negociar.
3. Cuando se quiere profundizar con un interesado en particular.

---

## Tema 5 · Técnicas de especificación de requerimientos

**10. Completen el siguiente cuadro indicando una ventaja y una limitación de cada técnica de especificación de requerimientos.**

| Técnica | Ventaja | Limitación |
|---|---|---|
| Lenguaje natural estructurado | Fácil de entender para usuarios.| Puede presentar ambiguedades.|
| Casos de uso | Describe claramente la interacción usuario-sistema.| Puede ser extenso en sistemas grandes.|
| Historias de usuario | Son simples y útiles en metodología ágiles.| No siempre tienen suficiente detalle técnico.|
| Diagramas (UML) | Facilitan la representación visual.| Requieren conocimiento de la notación.|


## Tema 6 · Especificaciones formales

**11. ¿Qué es una especificación formal y en qué tipo de sistemas se justifica su uso? Da un ejemplo hipotético de un sistema donde la usarías.**

Es una descripción de los requerimientos utilizando una notación matemática con reglas definidas, evitando interpretaciones diferentes.

Se utiliza principalmente en sistemas críticos donde un error puede causar consecuencias graves, como sistemas médicos o de control industrial.

Ejemplo: Sistema de control de un avión.

## Tema 7 · Prototipado de los requerimientos

**12. Explica la diferencia entre un prototipo desechable y un prototipo evolutivo, con un ejemplo de un proyecto donde usarías cada uno.**

_Respuesta:_Prototipo desechable (throwaway): se construye rápido y barato solo para explorar o validar una idea (por ejemplo, la interfaz de usuario o un requisito ambiguo), y luego se descarta; el sistema final se construye desde cero. Ejemplo: hacer una maqueta en papel o en Figma de la pantalla de login de una app para validar con el cliente si le gusta el flujo, sin usar ese código para el producto real.
	•	Prototipo evolutivo: se construye con calidad suficiente para ir mejorándolo iterativamente hasta convertirse en el sistema final; no se descarta, se refina. Ejemplo: un MVP (producto mínimo viable) de una app de e-commerce que se lanza a usuarios reales y se va ampliando con nuevas funcionalidades en cada sprint hasta llegar al producto completo.

---

## Tema 8 · Técnicas de construcción rápida

**13. Menciona dos técnicas de construcción rápida de prototipos vistas en clase y explica brevemente en qué consiste cada una.**

_Respuesta:_Programación visual / drag-and-drop: herramientas donde se arman pantallas e interacciones arrastrando componentes (botones, formularios, etc.) sin escribir mucho código, ideal para mostrar rápido cómo se vería la interfaz (ej. Figma, Adobe XD, o generadores de UI).
	•	Reutilización de componentes existentes: se arma el prototipo combinando bibliotecas, frameworks o módulos ya hechos (por ejemplo, componentes de Bootstrap o Material UI) en lugar de programar todo desde cero, lo que acelera mucho la construcción.

---

## Tema 9 · Validación de requerimientos

**14. Completen el siguiente cuadro relacionando cada técnica de validación con el tipo de problema que detecta mejor.**

| Técnica de validación | Qué tipo de problema detecta mejor |
|---|---|
| Revisiones de requisitos | Detectan errores, contradicciones, información incompleta o requisitos ambiguos. |
| Prototipado | Permite detectar problemas de comprensión, diseño o necesidades que el usuario no había expresado claramente. |
| Generación de casos de prueba | Permite comprobar si los requisitos pueden ser comprobados y si el sistema cumple con lo solicitado. |


## Tema 10 · Administración de requerimientos

**15. Explica con tus palabras qué es la trazabilidad de requerimientos y por qué es importante en un proyecto real.**

La trazabilidad de requerimientos es la posibilidad de seguir un requerimiento durante todo el proyecto, desde que se identifica hasta que se desarrolla y se prueba. Es importante porque permite saber qué parte del sistema corresponde a cada requerimiento y verificar que ninguno quede sin implementar. También ayuda a controlar los cambios que se hagan durante el proyecto.

## Tema 11 · Medición de requerimientos

**16. Menciona dos métricas que se pueden aplicar a los requerimientos de un proyecto y qué información le aporta cada una al equipo.**

**Dos métricas que se pueden utilizar son:**

**Cantidad de requisitos:** permite conocer cuántos requisitos tiene el proyecto y controlar si el alcance está aumentando demasiado.
**Porcentaje de requisitos cumplidos:** permite saber qué cantidad de requisitos ya fueron implementados y cuáles todavía están pendientes.

**17. Reflexión final:** pensá en un proyecto de software (hipotético o real). Describí qué técnica de obtención, qué técnica de especificación y qué técnica de validación usarías para sus requerimientos, y justificá tu elección considerando el tipo de proyecto y de usuarios.

Para un sistema de control de inventario de un minisúper, utilizaría entrevistas como técnica de obtención, porque permitirían hablar directamente con la persona encargada y conocer cómo trabaja actualmente y qué necesita.
Para especificar los requerimientos utilizaría casos de uso, porque permiten representar de forma clara las acciones que puede realizar el usuario, como registrar productos, modificar cantidades o consultar el inventario.
Para validar los requerimientos utilizaría prototipado, porque permitiría mostrar al encargado cómo funcionaría el sistema antes de desarrollarlo completamente y comprobar si las pantallas y funciones son realmente las que necesita.
