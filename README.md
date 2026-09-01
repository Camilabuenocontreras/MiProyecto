# Sonrisa Imperial

Landing page de una clínica dental. Tiene un solo objetivo: que la persona agende una hora.

**Sitio publicado:** https://camilabuenocontreras.github.io/MiProyecto/

> ⚠️ **Es un proyecto de práctica.** La clínica no existe y los datos de contacto son inventados. Ver [Pendientes](#pendientes) antes de usarla de verdad.

---

## Qué hay aquí

```
MiProyecto/
├── docs/
│   └── index.html    ← la página completa: HTML, CSS y JavaScript en un solo archivo
├── .gitignore
└── README.md         ← este archivo
```

Eso es todo. **No hay nada que instalar ni que compilar.** No usa React, ni npm, ni Node. Para verla en su computador, haga doble clic en `docs/index.html` y se abre en el navegador.

Lo único que la página pide por internet son las tipografías, que vienen de Google Fonts.

## Cómo publicar un cambio

El sitio se sirve con **GitHub Pages**, configurado para leer la carpeta `/docs` de la rama `main`. Es decir: lo que esté en `docs/index.html` es lo que se ve online.

1. Edite `docs/index.html`
2. En GitHub Desktop: **Commit** (con un mensaje que diga qué cambió)
3. **Push**
4. Espere alrededor de un minuto y recargue el sitio

No hay que tocar ninguna configuración: se actualiza solo.

### Cambio rápido, sin el computador de siempre

Entre a [el repositorio](https://github.com/Camilabuenocontreras/MiProyecto), abra `docs/index.html`, haga clic en el **lápiz**, edite y guarde con *Commit changes*. Funciona desde cualquier navegador, incluso el teléfono.

### Si trabaja en más de un computador

En el otro equipo, clone el repositorio una sola vez:

```bash
git clone https://github.com/Camilabuenocontreras/MiProyecto.git
```

Y después, siempre la misma regla: **pull al llegar, push al irse.** Si edita en dos computadores sin sincronizar, git no sabrá cuál versión vale y aparecerá un conflicto.

## Pendientes

Dos cosas que faltan para que esto sirva como sitio real de una clínica:

**1. Los datos de contacto son de relleno.** Están inventados y hoy son públicos:

| Dato | Valor actual (falso) |
|---|---|
| Teléfono | +56 2 2123 4567 |
| Correo | hola@sonrisaimperial.cl |
| Dirección | Avenida Providencia 1234, oficina 802 |
| Horarios | Lun–Jue 09:00–19:00, Vie 09:00–17:00, Sáb 10:00–14:00 |

También son inventadas las duraciones de los tratamientos.

**2. El formulario no envía nada a ninguna parte.** Valida los datos y muestra una confirmación en pantalla, pero **nadie recibe esas solicitudes de hora**. Para que lleguen de verdad hay que conectarlo a un servicio (Formspree, Netlify Forms, o un backend propio). El punto exacto está marcado con un comentario en `docs/index.html`, línea **626**, dentro del `submit`. Los datos ya están listos ahí, en `new FormData(form)`.

## Notas de diseño

Por si más adelante hay que agregar secciones y se quiere mantener la coherencia:

- **Tipografías:** Marcellus y Marcellus SC para títulos y rótulos; Karla para el texto.
- **Colores:** verde jade `#0B3A32`, oro `#A5854A` reservado solo para filetes y rótulos pequeños, fondo porcelana `#F4F6F4`, tinta `#121A17`.
- Todos los colores están definidos como variables CSS al principio del archivo, con su versión para **tema oscuro**. Si agrega un color, defínalo ahí y en los dos temas — nunca escriba un color suelto en medio del CSS, o la página se romperá en modo oscuro.
- Esquinas rectas y separadores de una línea, en vez de tarjetas redondeadas.
