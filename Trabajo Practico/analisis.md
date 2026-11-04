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
| RF-01 | [El sistema debe permitir...] | Alta |
| RF-02 | [El sistema debe permitir...] | Alta |
| RF-03 | [El sistema debe permitir...] | Media |
| RF-04 | [El sistema debe permitir...] | Baja |

---

## 2. Requisitos no funcionales

| ID | Requisito | Categoría |
|---|---|---|
| RNF-01 | [ej. El sistema debe responder en menos de 2s] | Rendimiento |
| RNF-02 | [ej. Las contraseñas deben almacenarse cifradas] | Seguridad |
| RNF-03 | [ej. La interfaz debe ser utilizable sin capacitación previa] | Usabilidad |

---

## 3. Modelo de casos de uso

**Diagrama de casos de uso:**

`[Insertar imagen: diagramas/casos-de-uso.png]`

**Especificación de casos de uso principales:**

### CU-01 · [Nombre del caso de uso]

- **Actor(es):** [actor principal / secundarios]
- **Precondición:** [qué debe cumplirse antes]
- **Flujo principal:**
  1. [Paso 1]
  2. [Paso 2]
  3. [Paso 3]
- **Flujos alternativos:** [qué pasa si algo falla o se desvía]
- **Postcondición:** [estado del sistema al finalizar]

*(Repetir esta estructura para cada caso de uso principal.)*

---

## 4. Modelo de dominio

**Diagrama de clases conceptual:**

`[Insertar imagen: diagramas/modelo-dominio.png]`

[Breve descripción de las entidades principales del negocio y cómo se relacionan entre sí, sin detalles de implementación.]

---

## 5. Diagramas de comportamiento

**Diagrama de secuencia / actividad — [Nombre del flujo principal]:**

`[Insertar imagen: diagramas/secuencia-flujo-principal.png]`

[Breve explicación del flujo representado.]

---

## 6. Prototipo de interfaz (mockups)

**Pantalla — [Nombre de la pantalla]:**

`[Insertar imagen: diagramas/mockup-pantalla1.png]`

[Breve descripción de la interacción que ilustra este mockup.]

*(Repetir para cada pantalla principal.)*

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
