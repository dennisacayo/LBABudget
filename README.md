# Presupuesto · La Banda de la Abuela

Aplicación web (una página) para crear presupuestos de precios: rellenas el
formulario, ves la vista previa y generas el PDF desde el navegador. Funciona
en escritorio y móvil; no necesita servidor.

## Archivos
- `index.html` — la app (formulario + vista previa + botones).
- `assets/` — foto e logo.
- `fonts/` — tipografías.
- `vendor/` — librería `html2pdf.bundle.min.js` (genera el PDF en el navegador).

## Publicar en GitHub Pages
1. Sube estos archivos a un repo (con `index.html` en la raíz).
2. **Settings → Pages → Deploy from a branch → main → / (root)** y guarda.
3. En ~1 min tendrás la URL (`https://USUARIO.github.io/REPO/`). Ese es el enlace.

## Cómo se usa
1. Abre el enlace (en cualquier navegador, también móvil).
2. Rellena el formulario; la vista previa se actualiza al escribir.
3. **Descargar PDF** (recomendado, sobre todo en móvil): genera el archivo A4
   con margen 0 directamente, sin pasar por el motor de impresión (que en móvil
   mete márgenes que no se pueden quitar).
4. **Imprimir** (alternativa en escritorio): "Guardar como PDF", tamaño **A4**,
   márgenes **Ninguno**. Da un PDF con texto seleccionable.

### Tarifas (lo importante)
Escribe **una línea por opción** con el formato:
```
duración, músicos, precio
```
igual que por WhatsApp. Ejemplo:
```
2 horas, 4 músicos, 990 €
2 horas, 5 músicos, 1.090 €
3 horas, 4 músicos, 1.290 €
3 horas, 5 músicos, 1.390 €
3 horas, 6 músicos, 1.490 €
```
Se **agrupan solas por duración**, así que puedes poner 2, 3 y 4 horas seguidas.

### Otros campos
- **Amplificación (opcional):** apartado para el sonido y luces con su precio
  (concepto + precio). Si dejas ambos vacíos, no aparece en el presupuesto.
- **Todo incluido:** un concepto por línea (instrumentos, sonido, luces…).
- **Dirigido a:** opcional; si lo rellenas, aparece bajo el título.
- **Nota de IVA:** al pie sale fijo que los precios son sin IVA y que, si se
  requiere factura, se aplica un 21%.
- **Contacto:** nombre, teléfono y correo. Vienen con los datos actuales por
  defecto; cámbialos si hace falta. "Limpiar" vuelve a poner los de por defecto.

## Personalizar
- **Foto:** sustituye `assets/cover.jpg` (mismo nombre). Para que pese poco:
  JPEG calidad ~80.
- **Color de marca:** variable `--red` en `:root` dentro de `index.html`.
- **Enlace de reserva / textos fijos** (intro, "Reserva tu fecha"): en `index.html`.

> Los datos se guardan en el navegador (localStorage), no se envían a ningún sitio.
> Tras subir cambios al repo, recarga forzada (Ctrl/Cmd+Shift+R).
