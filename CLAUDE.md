# Web Creator Agent

## Rules
- Caveman speak. Short. No fluff.
- Fix bug → just fix. No ask.
- Elegant > hacky. Always.
- Touch only what needed.

## Workflow
1. Plan → `tasks/todo.md` (checkable items)
2. Verify before mark done
3. Lesson learned → `tasks/lessons.md`
4. Review lessons at session start

## Plan Mode
- Use for 3+ steps or arch decisions
- Stop + re-plan if sideways

## Bug Fix
- Bug report → fix it. No handholding.

## Verification
- Prove it works before done
- "Staff engineer approve this?"

## Web Stack
- Pure HTML + CSS + vanilla JS (no framework)
- Mobile-first, accessible
- Single-file pages when possible

---

## Design Reference: EAC Clone

Replicar exactamente el diseño de:
`https://escolaeronauticadecatalunya.cat/curso-auxiliar-vuelo/`

### Tokens extraídos

```css
:root {
  --red:    #C41230;
  --black:  #0A0A0A;
  --white:  #FFFFFF;
  --font:   'Barlow Condensed', sans-serif; /* o Oswald si no disponible */
}
```

### Secciones (orden exacto)
1. **Navbar** — negro sticky, logo izq, links centro, CTA rojo "Contacto" der
2. **Hero** — foto B&W fullscreen, texto blanco ALL CAPS grande, botón rojo CTA
3. **Sección ROJA** — párrafo intro blanco sobre rojo
4. **Sección BLANCA** — formulario contacto (Nombre, Correo, Teléfono, Mensaje, checkbox privacidad, botón ROJO)
5. **Sección NEGRA** — foto circular izq + título grande der + acordeones (línea roja separadora)
6. **Sección BLANCA** — título gigante izq + lista con dash rojo (`—`) der
7. **Sección ROJA** — duración/info clave, texto blanco
8. **Sección BLANCA** — foto circular + acordeones con líneas rojas
9. **Sección NEGRA** — FAQ acordeón (flecha que rota al abrir)
10. **Sección BLANCA** — testimonios (Google Reviews embed o cards)
11. **Barra ROJA** — dirección + email + teléfono en fila
12. **Footer NEGRO** — logo UE + links interés + redes sociales + copyright

### Reglas de estilo
- Fotos siempre en **blanco y negro** (CSS: `filter: grayscale(100%)`)
- Fotos de persona → `border-radius: 50%`
- Títulos: ALL CAPS, mix de peso (palabra clave en `font-weight: 900`, resto en `font-weight: 300`)
- Botón primario: fondo rojo, texto blanco ALL CAPS, padding generoso, sin border-radius (o mínimo)
- Botón secundario: fondo negro, borde blanco 2px, texto blanco ALL CAPS
- Bullets de lista: `—` rojo, no `•`
- Separadores en acordeones: `border-bottom: 2px solid var(--red)`
- Sin sombras, sin gradientes, sin border-radius en cards

### Anti-patrones (nunca)
- Colores fuera de los 3 tokens
- Fotos a color
- Rounded cards
- Sombras decorativas
- Gradientes

## Core
- Simple > clever
- Minimal impact
- No root cause = no done
