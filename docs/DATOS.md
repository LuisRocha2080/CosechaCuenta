# Modelo de datos — CosechaCuenta

Base SQLite local (`expo-sqlite`). Fechas en formato ISO `AAAA-MM-DD`; montos en bolivianos con dos decimales (guardados como enteros en centavos).

## `parcelas`

Columnas: id, nombre, hectareas, ubicacion, cultivo_actual

## `campanas`

Columnas: id, parcela_id, cultivo, fecha_siembra, fecha_cosecha, estado

## `gastos_campana`

Columnas: id, campana_id, categoria, monto, fecha, nota

## `cosechas`

Columnas: id, campana_id, fecha, cantidad, unidad, precio_unitario, comprador

## `tareas`

Columnas: id, campana_id, descripcion, fecha_prevista, hecha

## Reglas generales

- Cada tabla tiene `id` entero autoincremental.
- Los borrados con historial son **lógicos** (campo `activo`) para no romper reportes.
- Cambios de esquema mediante migraciones numeradas en `src/db/migraciones/`.
