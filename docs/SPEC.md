# Especificación — CosechaCuenta

Requisitos escritos con el patrón EARS («Cuando…, el sistema deberá…»). Cada uno es verificable con una prueba (ver [PRUEBAS.md](PRUEBAS.md)).

## Alcance de la versión 1.0

Cuaderno digital del pequeño agricultor: parcelas, campañas, costos, jornales, cosecha y costo por quintal. Funciona en un solo dispositivo, sin cuentas de usuario y sin servidor.

## Requisitos funcionales

| ID | Requisito |
|---|---|
| R01 | Cuando el usuario crea una campaña, el sistema deberá asociarla a una parcela y permitir una sola campaña activa por parcela. |
| R02 | Cuando se registra un gasto, el sistema deberá sumarlo al costo acumulado de la campaña. |
| R03 | El sistema deberá calcular el costo por unidad como costo total de la campaña dividido entre la cantidad cosechada. |
| R04 | El sistema deberá calcular la utilidad por hectárea como ingresos menos costos, dividido entre las hectáreas de la parcela. |
| R05 | Cuando llega la fecha prevista de una tarea, el sistema deberá mostrar una notificación local. |
| R06 | Cuando el usuario cierra una campaña, el sistema deberá impedir nuevos gastos y conservar el historial. |
| R07 | Si el dispositivo no tiene señal en el campo, el sistema deberá funcionar completo sin conexión. |
| R08 | Cuando el usuario exporta, el sistema deberá generar un resumen de campaña en PDF y CSV. |

## Requisitos no funcionales

| ID | Requisito |
|---|---|
| N01 | La app deberá abrir en menos de 3 segundos en un teléfono Android de gama baja (2 GB de RAM). |
| N02 | Todos los datos deberán almacenarse en SQLite local y no enviarse a ningún servidor. |
| N03 | La interfaz deberá estar en español con montos en bolivianos (Bs) y fechas dd/mm/aaaa. |
| N04 | Los botones táctiles deberán medir al menos 48 dp. |
| N05 | La app deberá operar completa sin conexión a internet. |
| N06 | El costo de licencias de cualquier dependencia deberá ser cero. |

## Fuera de alcance (v1.0)

- No ofrece pronóstico del clima ni recomendaciones agronómicas.
- Un solo dispositivo por finca en la primera versión.
- Los precios de venta son los que ingresa el usuario.

## Criterios de aceptación globales

1. Un usuario nuevo registra su primer dato útil en menos de 5 minutos.
2. Ningún dato se pierde al cerrar la app de forma abrupta.
3. Los totales coinciden con un cálculo manual en los casos de prueba de [PRUEBAS.md](PRUEBAS.md).
