# Plan de pruebas — CosechaCuenta

## Automáticas (Jest)

La lógica de cálculo vive en `src/lib/` y se prueba sin interfaz.

- [ ] Una sola campaña activa por parcela.
- [ ] Costo por unidad con cosecha en qq, arroba y kg.
- [ ] Utilidad con ventas parciales.
- [ ] Notificación de tarea sin conexión.
- [ ] Exportación de una campaña con más de 100 gastos.

## Manuales en teléfono real

- [ ] Instalación del APK en Android 10 o superior.
- [ ] Uso completo en modo avión.
- [ ] Cierre abrupto de la app y reapertura sin pérdida de datos.
- [ ] Exportación y apertura del archivo en otra app.

## Comandos

```bash
npm test
npx tsc --noEmit
```
