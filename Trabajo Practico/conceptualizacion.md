[← Volver al inicio](index.md)

# Entrega 1 · Conceptualización

> *Punto de partida: entender el problema y encuadrar el proyecto.*

---

## 1. Presentación del proyecto

**Nombre del sistema:** Sistema de Control de Inventario para un Minisúper

**Integrantes del grupo:**

| Nombre | Rol |
|---|---|
| Javier Caceres | Análisis de requisitos y documentación. |
| Iliana Flecha | Modelado y diseño del sistema.|
| Vivian Obregon | Levantamiento de información y comunicación con el cliente. |
| Hanna Salas | Investigación tecnológica y gestión del proyecto. | 

**Usuario / cliente real:** 
El sistema será desarrollado para un minisúper administrado por la madre de una integrante del grupo.
Actualmente, el negocio realiza el control de sus productos de manera manual y las ventas se realizan directamente en el establecimiento. No cuenta con una computadora ni con un sistema informático destinado al control de inventario.
La propietaria será la principal cliente del proyecto y proporcionará información sobre la forma en que actualmente administra los productos y las necesidades que presenta el negocio.

## 2. Definición del problema
Actualmente, el minisúper realiza el control de sus productos de forma manual y no dispone de una herramienta informática destinada a gestionar el inventario.
Esta situación dificulta mantener la información de los productos organizada y conocer de manera rápida la cantidad disponible de cada artículo. También puede dificultar la identificación de productos que necesitan ser repuestos.
La falta de un sistema de control de inventario hace necesario realizar una gestión manual de la información, lo que puede generar dificultades para mantener actualizado el stock y llevar un seguimiento organizado de los productos disponibles.
Por este motivo, se plantea el desarrollo de un sistema que permita organizar y facilitar el control del inventario del minisúper.

## 3. Propósito y objetivos
**Objetivo general:**
Diseñar un sistema de control de inventario para un minisúper que permita gestionar de manera organizada la información de los productos, controlar sus existencias y facilitar la identificación de productos que necesitan reposición.

**Objetivos específicos:**
1. Registrar y mantener actualizada la información de los productos, incluyendo sus datos principales y cantidad disponible.
2. Controlar las entradas y salidas de productos para mantener actualizado el stock del minisúper.
3. Facilitar la consulta del inventario, permitiendo identificar los productos disponibles y aquellos que se encuentren por debajo del stock mínimo establecido.


## 4. Alcance del proyecto


El sistema estará orientado al control y administración del inventario del minisúper.

4.1 Funcionalidades incluidas

La primera versión del sistema permitirá:

* Registrar productos.
* Modificar los datos de los productos.
* Desactivar productos que ya no se comercialicen.
* Consultar y buscar productos.
* Registrar la cantidad disponible de cada producto.
* Registrar entradas de productos.
* Registrar salidas de productos.
* Actualizar las cantidades disponibles.
* Establecer un nivel mínimo de stock.
* Identificar productos con bajo stock.
* Consultar el estado actual del inventario.

4.2 Fuera del alcance

Para mantener un alcance realista, la primera versión no incluirá:

* Registro y gestión de ventas.
* Compras en línea.
* Servicio de delivery.
* Pagos electrónicos.
* Facturación electrónica.
* Gestión de múltiples sucursales.
* Aplicación móvil.
* Integración automática con proveedores.
* Control contable del negocio.

Estas funcionalidades podrían considerarse en futuras versiones del sistema, pero no forman parte del alcance inicial del proyecto.

---

## 5. Interesados (stakeholders)
5.1 Propietaria del minisúper

Es la principal interesada y cliente del sistema. Se encarga de la administración general del negocio.

Interés: disponer de una herramienta que facilite el control y organización del inventario.


5.2 Personal encargado de la atención

Son las personas que colaboran en la atención del minisúper y pueden necesitar consultar o actualizar información relacionada con los productos.

Interés: acceder de manera sencilla a la información del inventario y mantener actualizadas las cantidades disponibles.


5.3 Administrador del sistema

Será el usuario encargado de administrar la información principal del sistema.

Interés: registrar, modificar y controlar los productos y el inventario.


5.4 Clientes del minisúper

Son las personas que adquieren los productos disponibles en el establecimiento.

Interés: encontrar los productos disponibles y recibir una atención más organizada.

---

## 6. Justificación / viabilidad
6.1 Justificación

El proyecto surge a partir de una necesidad real de un minisúper que actualmente realiza el control de sus productos de manera manual.

La implementación de un sistema de control de inventario permitirá organizar la información de los productos y facilitar el seguimiento de las cantidades disponibles. Esto puede ayudar a la propietaria a conocer con mayor facilidad el estado de su inventario y detectar productos que necesitan reposición.

Además, al tratarse de un negocio real, el grupo podrá obtener información directamente de la cliente y validar que la propuesta responda a sus necesidades.


6.2 Viabilidad técnica

El proyecto es técnicamente viable, ya que puede desarrollarse utilizando herramientas y tecnologías disponibles para el grupo.

El sistema puede utilizar una base de datos relacional para almacenar la información de los productos y sus movimientos de inventario.


6.3 Viabilidad operativa

El sistema estará diseñado considerando las actividades habituales del minisúper y procurando que su utilización sea sencilla para las personas encargadas del negocio.

La propietaria podrá participar durante el análisis para validar las necesidades y el funcionamiento esperado del sistema.


6.4 Viabilidad económica

El proyecto es económicamente viable debido a que puede desarrollarse utilizando herramientas de software gratuitas o de bajo costo.

La implementación podrá realizarse inicialmente utilizando los recursos tecnológicos disponibles y, posteriormente, analizar la necesidad de adquirir un equipo destinado exclusivamente al sistema.

---

## 7. Visión general de la solución

[Descripción breve, en lenguaje llano y sin detalle técnico, de cómo el grupo imagina que el sistema resolverá el problema planteado.]

---Se propone desarrollar un sistema informático que permita centralizar y organizar la información relacionada con el inventario del minisúper.
El sistema permitirá registrar los productos, consultar sus datos, controlar las cantidades disponibles y registrar los movimientos de entrada y salida de productos.
Además, permitirá establecer niveles mínimos de stock para identificar aquellos productos cuya cantidad disponible sea baja y requiera reposición.
La solución estará orientada principalmente a la propietaria y a las personas autorizadas para utilizar el sistema, buscando que puedan gestionar el inventario de manera sencilla y organizada.
En esta etapa se presenta una visión general de la solución. Los detalles técnicos y modelos específicos serán desarrollados en las siguientes entregas

## 8. Glosario de términos

| Término | Definición |
|---|---|
| [Producto] | [Artículo disponible en el minisúper para su comercialización] |
| [Inventario] | [Conjunto de productos disponibles y registrados en el minisúper.] |
| [Stock] | [Cantidad disponible de un determinado producto] |
| [Entrada] | [Registro de productos que ingresan al inventario, por ejemplo, debido a una reposición.] |
| [Salida] | [Registro de productos que disminuyen la cantidad disponible del inventario.] |
| [Stock mínimo] | [Cantidad mínima establecida para un producto antes de considerarlo con bajo stock.] |
| [Bajo stock] | [Estado de un producto cuya cantidad disponible se encuentra por debajo del nivel mínimo establecido] |
| [Reposición] | [Proceso mediante el cual se incorporan nuevos productos al inventario para aumentar su disponibilidad] |
| [Usuario] | [Persona autorizada para acceder y utilizar el sistema] |
| [Administrador] | [Usuario encargado de gestionar la información y las operaciones principales del sistema] |
---

## 9. Riesgos iniciales

| Riesgo | Impacto | Estrategia de mitigación |
|---|---|---|
| Información insuficiente sobre el funcionamiento del negocio. | Al comienzo del proyecto puede no conocerse completamente la forma en que la propietaria controla actualmente los productos. | Realizar entrevistas y consultas con la propietaria para conocer el proceso actual y validar los requisitos. |
| Cambios en los requisitos. | Durante el desarrollo del proyecto pueden surgir nuevas necesidades o modificaciones solicitadas por el cliente. | Establecer un alcance inicial y registrar los cambios para evaluar su incorporación al proyecto. |
| Falta de tiempo. | El proyecto debe desarrollarse dentro del periodo establecido por la asignatura. | Mantener un alcance limitado y priorizar las funciones principales del control de inventario. |
| Dificultades en la adopción del sistema. | Al tratarse de un negocio que actualmente trabaja de forma manual, puede existir cierta dificultad inicial para adaptarse a una herramienta informática. | Diseñar una interfaz sencilla y considerar las necesidades y conocimientos tecnológicos de las personas que utilizarán el sistema. |
| Falta de equipamiento. | Actualmente el minisuper no dispone de una computadora destinada al control del inventario. | Considerar durante el diseño las alternativas de equipamientos necesarias para utilizar el sistema y seleccionar una solución que no requiera infraestructura excesivamente costosa. |

---

## 10. Selección tecnológica preliminar
La selección tecnológica es preliminar y podrá ser ajustada durante las etapas de análisis y diseño.
| Componente | Elección | Justificación breve |
|---|---|---|
| Lenguaje de programación | Java | Se propone Java debido a que permite desarrollar aplicaciones utilizando programación orientada a objetos y facilita la organización del sistema mediante clases y componentes. |
| Framework | Spring Boot | Se propone utilizar Spring Boot para facilitar el desarrollo de la aplicación y permitir una estructura organizada para sus diferentes componentes. |
| Base de datos | MySQL | Se propone utilizar MySQL para almacenar la información de los productos, las cantidades disponibles y los movimientos de inventario. |

---

Herramientas complementarias:

Github: Para almacenar y gestionar el proyecto.

Github Pages: Para publicar las entregas del trabajo.

Draw.io: Para elaborar los diagramas del sistema.

Figma: Para realizar los prototipos de las interfaces.

---

[← Volver al inicio](index.md) · [Siguiente: Análisis →](analisis.md)
