---
title: "Análisis"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 2 · Análisis

> *Qué debe hacer el sistema, desde la perspectiva del negocio y del usuario.*

---

## 1. Requisitos funcionales

| ID | Requisito | Prioridad |
|---|---|---|
| RF-01 | El sistema debe permitir registrar productos con código, nombre, categoría, unidad de medida y stock mínimo. | Alta |
| RF-02 | El sistema debe permitir modificar los datos de un producto existente, incluido su stock mínimo.  | Alta |
| RF-03 | El sistema debe permitir desactivar productos que ya no se comercialicen, sin eliminarlos del historial. | Media |
| RF-04 | El sistema debe permitir consultar y buscar productos por nombre, código o categoría. | Alta |
| RF-05 | El sistema debe permitir registrar entradas de productos (reposición) indicando producto, cantidad y fecha. | Alta |
| RF-06 | El sistema debe permitir registrar salidas de productos indicando producto, cantidad y motivo (venta, merma o vencimiento, ajuste). | Alta |
| RF-07 | El sistema debe actualizar automáticamente la cantidad disponible de un producto al registrar una entrada o una salida. | Alta |
| RF-08 | El sistema debe identificar y listar los productos cuya cantidad disponible esté por debajo de su stock mínimo.. | Alta |
| RF-09 | El sistema debe permitir consultar el estado actual del inventario (producto, cantidad disponible y estado). | Alta |
| RF-10 | El sistema debe permitir consultar el historial de movimientos (entradas y salidas) por producto y por rango de fechas. | Media |
| RF-11 | El sistema debe requerir inicio de sesión y limitar las funciones según el rol del usuario (Administrador o Encargado).  | Alta |
| RF-12 | El sistema debe permitir al administrador gestionar los usuarios autorizados (crear, desactivar y asignar rol). | Media |

---

## 2. Requisitos no funcionales

| ID | Requisito | Categoría |
|---|---|---|
| RNF-01 | Las consultas y el registro de movimientos deben responder en menos de 2 segundos con hasta 5.000 productos. | Rendimiento |
| RNF-02 | Las contraseñas deben almacenarse cifradas (hash con sal) y las funciones deben protegerse según el rol.  | Seguridad |
| RNF-03 | La interfaz debe poder usarse sin capacitación previa extensa: un movimiento debe poder registrarse en no más de 3 pasos.  | Usabilidad |
| RNF-04 | El sistema debe ser accesible desde un navegador web común, sin instalar software adicional en equipo.| Portabilidad |
| RNF-05 | Un movimiento y la actualización del stock deben guardarse en conjunto (transacción) para evitar inconsistencias. | Integridad |
| RNF-06 | El sistema debe permitir realizar copias de seguridad de la base de datos. | Disponibilidad |
| RNF-07 | El sistema debe funcionar con recursos modestos (un solo equipo), dado que el negocio no cuenta con infraestructura propia. | Eficiencia de costos |
| RNF-08 |  El código y la base de datos deben estar organizados para poder incorporar luego nuevas funciones (por ejemplo, ventas). | Mantenibilidad |

---

## 3. Modelo de casos de uso

**Diagrama de casos de uso:
https://ibb.co/zTdGxFc9

**Especificación de casos de uso principales:**

### CU-01 · [StockMiniSuper.html]

- **Actor(es):** [Administrador y Encargado]
- **Precondición:** [El usuario debe estar registrado y activo en el sistema]
- **Flujo principal:**
  1. [El usuario ingresa su nombre de usuario y constraseña]
  2. [El sistema recibe y valida las credenciales.]
  3. [El sistema identifica el rol asignado al usuario]
  4. [El sistema muestra el menú principal e las opciones permitidas para ese rol.]
- **Flujos alternativos:** [Si las credenciales son incorrectas, el sistema informa el error y permite volver a intentarlo. Si el usuario está desactivado, el sistema deniega el acceso]
- **Postcondición:** [El usuario queda autenticado y puede utilizar las funciones autorizadas según su rol.]

*(Repetir esta estructura para cada caso de uso principal.)*
CU-01 · Iniciar sesión

Actor(es): Administrador y Encargado.
Precondición: El usuario debe estar registrado y activo.
Flujo principal:
El usuario ingresa su nombre de usuario y contraseña.
El sistema valida las credenciales.
El sistema identifica el rol del usuario y muestra el menú correspondiente.
Flujos alternativos: Si las credenciales son incorrectas, informa el error y permite reintentar. Si el usuario está desactivado, deniega el acceso.
Postcondición: El usuario queda autenticado con los permisos correspondientes a su rol.

CU-02 · Registrar producto
Actor(es): Administrador.
Precondición: El Administrador inició sesión.
Flujo principal:
El Administrador selecciona “Nuevo producto”.
Ingresa código, nombre, categoría, unidad de medida, stock mínimo y cantidad inicial.
El sistema valida los datos y comprueba que el código sea único.
El sistema guarda el producto como activo.
El sistema confirma el registro.
Flujos alternativos: Si el código ya existe, informa el problema. Si faltan datos o hay cantidades negativas, solicita corregirlos y no guarda el producto.
Postcondición: El producto queda registrado, activo y con su stock inicial.

CU-06 · Registrar entrada
Actor(es): Administrador y Encargado.
Precondición: Sesión iniciada; el producto existe y está activo.
Flujo principal:
El usuario selecciona “Registrar entrada”.
Busca y selecciona el producto.
Ingresa la cantidad recibida y una observación opcional.
El sistema valida que la cantidad sea mayor que cero.
El sistema registra fecha, usuario, producto y cantidad.
El sistema suma la cantidad al stock y muestra el nuevo total.
Flujos alternativos: Si la cantidad es cero o negativa, solicita corregirla. Si el producto está desactivado, rechaza el movimiento.
Postcondición: El stock aumenta y la entrada queda guardada en el historial.

CU-07 · Registrar salida
Actor(es): Administrador y Encargado.
Precondición: Sesión iniciada; el producto existe y está activo.
Flujo principal:
El usuario selecciona “Registrar salida”.
Busca y selecciona el producto.
Ingresa la cantidad y el motivo: venta, merma o vencimiento, o ajuste.
El sistema valida que la cantidad sea mayor que cero y no supere el stock disponible.
El sistema registra el movimiento con fecha, usuario, producto, cantidad y motivo.
El sistema resta la cantidad al stock.
El sistema muestra el nuevo stock y alerta si queda por debajo del mínimo.
Flujos alternativos: Si la cantidad supera el stock, rechaza la salida e informa la existencia actual. Si la cantidad no es válida, solicita corregirla. Si falta el motivo, solicita seleccionarlo. Si el producto está desactivado, no permite el movimiento.
Postcondición: El stock disminuye y la salida queda en el historial; se muestra una alerta si corresponde.

CU-08 · Consultar productos con bajo stock
Actor(es): Administrador y Encargado.
Precondición: El usuario inició sesión.
Flujo principal:
El usuario selecciona “Bajo stock”.
El sistema compara el stock disponible de cada producto activo con su stock mínimo.
El sistema muestra los productos por debajo del mínimo, indicando cantidad actual, mínimo y diferencia.
Flujos alternativos: Si ningún producto está por debajo del mínimo, informa que el inventario está al día.
Postcondición: El usuario identifica los productos que necesitan reposición.

## 4. Modelo de dominio

**Diagrama de clases conceptual:**

https://ibb.co/zTdGxFc9


[Breve descripción de las entidades principales del negocio y cómo se relacionan entre sí, sin detalles de implementación.]

El Producto es la entidad principal del sistema, ya que representa los artículos que forman parte del inventario del minisúper. Cada producto pertenece a una Categoría y posee una cantidad disponible y un stock mínimo establecido.
Los cambios en el inventario se registran mediante la entidad *Movimiento, que puede representar una Entrada o una Salida de productos. Las entradas aumentan las existencias, mientras que las salidas las disminuyen según el motivo correspondiente.
Cada movimiento es registrado por un Usuario, quien tiene asignado un Rol (Administrador o Encargado). El rol determina las funciones y permisos que puede realizar dentro del sistema.
De esta manera, las entidades se relacionan para mantener un control organizado de los productos, las existencias y el historial de movimientos del inventario.
---

## 5. Diagramas de comportamiento

**Registrar salida CU-07:**

https://drive.google.com/file/d/1-yo7c5Dkn185auy4iR5a2mEY62gRTj8-/view?usp=drivesdk

El flujo muestra que el sistema valida contra el stock antes de guardar, y que el movimiento y la actualización del stock se guardan juntos.

---

## 6. Prototipo de interfaz (mockups)

**Prototipos de las pantallas principales del sistema (Minisúper la Candelaria) Los prototipos de alta fidelidad en Figma se presentan en la Entrega 3:**

**Pantalla - Inicio de sesión**

(https://drive.google.com/file/d/1UFgL355JhnZDMwFOiXMElk17j8pfwTC4/view?usp=drivesdk)

El usuario ingresa su nombre de usuario y contraseña; el sistema muestra el menú principal según su rol (Administrador o Encargado).

**Pantalla — Inventario actual (CU-05 y CU-09):**

https://drive.google.com/file/d/17sLUJLF0lNNEZqm5ot2ywrOMlY0Usz0E/view?usp=drivesdk

Permite buscar productos por nombre, código o categoría y ver de un vistazo su stock, su mínimo y su estado. Los productos con bajo stock se resaltan en rojo. Desde esta pantalla se accede a registrar entradas y salidas.

**Pantalla — Registrar salida (CU-07):**

https://drive.google.com/file/d/1X9aYZMo-wzGgiQGIfiyqOpweQmZwKM0O/view?usp=drivesdk

Permite registrar una salida eligiendo el producto, la cantidad y el motivo (venta, merma o vencimiento, ajuste). El panel lateral muestra el stock actual, el mínimo y el stock resultante, y advierte si el producto quedará por debajo del mínimo.

**Pantalla - Productos con bajo stock (CU-08):**
 
https://drive.google.com/file/d/1UFgL355JhnZDMwFOiXMElk17j8pfwTC4/view?usp=drivesdk

Lista los productos por debajo del stock mínimo, con la cantidad que falta para llegar al mínimo, y permite pasar de directamente a registrar una entrada de reposición.

---

## 7. Reglas del negocio

| ID | Regla |
|---|---|
| RN-01 | El código de un producto es único. |
| RN-02 | La cantidad de un movimiento debe ser mayor que cero. |
| RN-03 | Una salida no puede superar la cantidad disponible: el stock nunca puede quedar negativo. |
| RN-04 | Toda salida debe tener un motivo (venta, merma o vencimiento, ajuste). |
| RN-05 | Un producto está en bajo stock cuando su cantidad disponible es menor que su stock mínimo. |
| RN-06 | Un producto desactivado no admite nuevos movimientos, pero conserva su historial. |
| RN-07 | Los movimientos no se modifican ni se eliminan; los errores se corrigen con un movimiento de ajuste. |
| RN-08 | Cada movimiento registra la fecha, el usuario y el producto afectado. |
| RN-09 | Solo el Administrador puede registrar, modificar o desactivar productos y gestionar usuarios. |
| RN-10 | El Encargado puede consultar el inventario y registrar entradas y salidas. |

---

## 8. Matriz de trazabilidad

| Requisito | Caso(s) de uso relacionado(s) |
|---|---|
| RF-01 | CU-02 | RN-01, RN-09 |
| RF-02 | CU-03 | RN-09 |
| RF-03 | CU-04 | RN-06, RN-09 |
| RF-04 | CU-05 | — |
| RF-05 | CU-06 | RN-02, RN-06, RN-08 |
| RF-06 | CU-07 | RN-02, RN-03, RN-04, RN-06, RN-08 |
| RF-07 | CU-06, CU-07 | RN-03, RN-07 |
| RF-08 | CU-08 | RN-05 |
| RF-09 | CU-09 | RN-05 |
| RF-10 | CU-10 | RN-07, RN-08 |
| RF-11 | CU-01 | RN-09, RN-10 |
| RF-12 | CU-11 | RN-09 |
| RF-03 | CU-01 |

---

[← Anterior: Conceptualización](conceptualizacion.md) · [Siguiente: Diseño →](diseno.md)
