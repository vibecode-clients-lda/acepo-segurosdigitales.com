---
name: especialista-acepo
description: ESPECIALISTA ACEPO — Landing page explicadora del Seguro Colectivo de Vida ACEPO (póliza INS 0101VTM0000704). Single-file HTML+CSS+JS vanilla, paleta teal/cian + navy + dorado, 6 coberturas en bento clickeable, 9 convenios en acordeón <details>, botón flotante WhatsApp 8624-8757, CTA "Quiero afiliarme" conectado a Google Form https://forms.gle/7GGYVKYeXprWELet9. Repo vibecode-clients-lda/acepo-segurosdigitales.com (cliente Vibecode, no SDI). Usar este skill cuando JC pida cualquier cambio al proyecto ACEPO.
---

# Especialista ACEPO — Seguro Colectivo de Vida

Contexto completo del proyecto para retomar sin perder contexto. Leer COMPLETO antes de tocar código.

## Qué es

Landing page explicadora del **Seguro Colectivo de Vida ACEPO** (Asociación Cultural y Educativa Para La Policía), respaldado por el INS, dirigido a **funcionarios públicos** (origen histórico: policía). No es exclusivo SDI — ACEPO es cliente de Vibecode bajo la marca propia.

Producto: póliza madre `0101VTM0000704` con el INS, modalidad contributiva, registro SUGESE `P14-26-A01-884 V7`. ¢15M de cobertura base, hasta ¢30M con doble indemnización accidental, beneficio familiar de hasta +¢15M adicional, costo ¢8.631/mes (rebajo de planilla, ¢4.316 quincenal).

## Estado actual (checkpoint 2026-05-12)

Sesión productiva inicial completa: del repo vacío al sitio listo para deploy con afiliación funcional.

- **`a2a50ab` (12 may 2026):** CTA "Quiero afiliarme" conectado a Google Form `https://forms.gle/7GGYVKYeXprWELet9` (target=_blank)
- **`177d862` (11 may 2026):** SKILL.md agregado al repo
- **`19a2450` (11 may 2026):** monto beneficio familiar +¢15M + separación visual del hint CTA
- **`a2eec6d` (11 may 2026):** WhatsApp pasa a botón flotante (bottom-left) con pulse animado; CTA "Quiero afiliarme" sin competencia visual
- **`52907c2` (11 may 2026):** rebalanceo Sección 2 — Convenios full-width con 2 columnas internas + 3 bloques chicos abajo
- **`9040d07` (11 may 2026):** icono 💡 ("Bueno saber") en lugar de ⓘ ("Importante") en nota de rebajo
- **`f9ae478` (11 may 2026):** 9 convenios desplegables con `<details>` + nota legal del primer rebajo de planilla en paso 3
- **`e57ea49` (11 may 2026):** logo ACEPO PNG oficial (`img/acepo-logo.png`) — sin recreaciones, archivo provisto por JC
- **`6a710d5` (11 may 2026):** 8 correcciones de copy (CCSS no sujeto a revisión, "INS por medio de ACEPO", 5 mil M en siniestros, etc.)
- **`78418e8` (11 may 2026):** 40+ años de trayectoria + Beneficio Familiar como adicional al principal
- **`c146628` (11 may 2026):** primer commit — explicador completo con 6 coberturas, respaldo INS visible, footer SUGESE

**Repo:** [vibecode-clients-lda/acepo-segurosdigitales.com](https://github.com/vibecode-clients-lda/acepo-segurosdigitales.com)
**Local clone:** `C:/Users/segur/Desktop/acepo-segurosdigitales.com/`
**Preview local:** `http://localhost:8910` (entrada `acepo` en `.claude/launch.json`)

## Stack técnico

- **Frontend:** HTML5 + CSS inline + JS vanilla (single-file, sin build, sin npm)
- **Tipografías:** Space Grotesk + Inter + JetBrains Mono (Google Fonts)
- **Animaciones:** CSS transitions + IntersectionObserver para fade-in de secciones
- **Interactividad:** `<details>` nativos para convenios, click handlers para bento expand/collapse
- **Hosting:** Pendiente (recomendado Netlify desde `main` + DNS `acepo-segurosdigitales.com`)
- **Sin backend, sin DB, sin localStorage** — todo estático

## Estructura del repo

```
acepo-segurosdigitales.com/
├── index.html              # App completa (~1500 líneas)
├── img/
│   ├── acepo-logo.png      # Logo ACEPO oficial (76 KB) — NO MODIFICAR
│   └── ins-blanco.png      # Logo INS BLANCO (72 KB)
└── SKILL.md                # Este archivo (sync con 3 paths)
```

## Coberturas (orden en el bento de la Sección 1)

| # | Cobertura | Monto destacado | Notas clave |
|---|---|---|---|
| 1 | ⭐ **Muerte Plus** | ¢15.000.000 | + adelanto enfermedad terminal 50% (¢7.5M) + funerarios 20% (¢2M) |
| 2 | Muerte Accidental (DID) | ¢30.000.000 | Doble indemnización + desmembramiento tabla INS |
| 3 | Incapacidad Total y Permanente (BI-1) | ¢15.000.000 | Requiere dictamen Unidad Calificadora CCSS "NO SUJETO A REVISIÓN". El INS por medio de ACEPO adelanta en vida. **Anula cobertura de muerte posterior** |
| 4 | Beneficio Familiar | **+¢15.000.000 adicional al principal** | Cónyuge ¢7.5M + 2 hijos ¢3.75M c/u (hasta 18, o 23 si estudia y depende econ.) |
| 5 | Cobertura Mutual ACEPO | +¢400.000 | Beneficio solidario aparte (¢400/200/100K) |
| 6 | Medicina Virtual | 100% gratis | 6 consultas/año |

**Costo:** ¢8.631/mes (mensual con 7% recargo) ó **¢4.316/quincena**, rebajo automático de planilla.
**Edad afiliación:** 18 a 39 años con 11 meses (único requisito).

## Convenios comerciales (9 desplegables)

Usan `<details>` nativos en una grilla 2 columnas internas:

| Convenio | Pill | Detalle |
|---|---|---|
| Hotel Arenas | 10% – 15% | L-V 10% / S-D 15%, presentar certificado en reserva |
| Hotel Fiesta | 12% – 10% | L-V 12% / S-D 10%, presentar certificado en reserva |
| Hotel Barceló | 10% | Sobre tarifas regulares, presentar certificado |
| Ponderosa | 20% | — |
| Funeraria Polini | ₡5.000/mes | **Plan 9+2** (9 personas + 2 mascotas): cofre, cremación, autopsia, urna laqueada, capillas, cremación mascotas. Tel 2231-3121 / WA 6004-3121 / ventas@funerariapolini.com |
| Asembis | Variable | Según servicio |
| Ekono | 5% | — |
| Adobe Rent a Car | Tarifa socio | — |
| Ópticas Visión | Tarifa socio | — |

## Diseño visual

Estilo **basado en el explicador del cotizador-autos** (mismo patrón visual: bento clickeable + sticky nav + floating nav + fade-in secciones).

### Paleta (no Modern SaaS Bento Tricolor — adaptación para ACEPO)
```css
--navy:       #0c2340     /* header, footer */
--teal:       #06b6d4     /* brand primario ACEPO */
--teal-deep:  #0e7490
--teal-bright:#22d3ee
--teal-light: #67e8f9
--teal-bg:    #ecfeff
--acepo-blue: #4a9fd9     /* azul del logo */
--acepo-blue-deep: #2b7cb8
--gold-mid:   #fbbf24     /* tagline + nota rebajo */
--gold-bg:    #fef3c7
--green-fresh:#10b981     /* tarjetas DID */
```

### Secciones
1. **Hero** "Para usted, que sirve y protege 🛡️" con bubble persuasivo
2. **Sección 1 — Coberturas** (bento de 6 clickeable, single-open)
3. **Sección 2 — Beneficios** (Convenios wide arriba + 3 chicos abajo: Actividades / Respaldo institucional / Sin fines de lucro)
4. **Sección 3 — Costo vs protección** (card navy con ¢8.631 → ¢30M comparativa + 4 reglas)
5. **Sección 4 — 3 pasos de afiliación** + nota dorada de rebajo + CTA principal
6. **Cierre** + footer SUGESE + WhatsApp flotante bottom-left + float-nav bottom-right

## Reglas de marca (🔴 obligatorias)

- **Logo ACEPO**: usar SOLO el archivo `img/acepo-logo.png` provisto por JC. NUNCA recrear paths SVG, NUNCA cambiar colores, NUNCA inventar tipografías. Si JC quiere reemplazar el archivo, sustituir el PNG entero.
- **Logo INS BLANCO**: archivo oficial `img/ins-blanco.png` (heredado del cotizador-autos). Sin filtros que alteren el color.
- **Tagline ACEPO oficial**: *"TRANQUILIDAD PARA USTED. SEGURIDAD PARA ELLOS."* (en la cinta dorada del header). No alterar.
- **Subtítulo institucional oficial**: *"Asociación Cultural y Educativa Para La Policía"* (no "Para La Policía" solo — incluye "Asociación Cultural y Educativa").
- **Trayectoria**: **+40 años** (más de 40 años, no 35). ACEPO fue creada en 1983.

## Tono persuasivo y de copy

- **Voz**: cercana pero respetuosa (no tutea — usa "usted").
- **Público objetivo**: funcionarios públicos en general (no solo policía).
- **No prometer**: solo lo que está en condiciones particulares VTM0000704. Si JC corrige un copy, ese copy es ley.
- **Disclosure obligatorio en footer**: nombre póliza madre + registro SUGESE + INS + texto de prelación de Condiciones Particulares sobre Generales.
- **Atribución de pagos**: usar **"el INS por medio de ACEPO le adelanta..."** (no "ACEPO le paga"). ACEPO es tomador, INS es asegurador.

## Pendientes

- **Subdominio + deploy**: pendiente Netlify connect + DNS `acepo-segurosdigitales.com` (apuntar al sitio Netlify).
- **PNG oficial de mayor resolución**: el actual (76 KB) sirve, pero si JC consigue uno de mayor resolución se reemplaza el archivo sin cambiar nada más.

## Completados

- ✅ **CTA Afiliarse conectado al Google Form** `https://forms.gle/7GGYVKYeXprWELet9` (commit `a2a50ab`, 12 may 2026). Abre en pestaña nueva (`target=_blank rel=noopener`).

## Flujo de trabajo (cómo hacer cambios)

1. Editar `index.html` en `C:/Users/segur/Desktop/acepo-segurosdigitales.com/`
2. Verificar local con preview `acepo` (puerto 8910) — recargar con `window.location.reload()` después de cada edit
3. Validar via `preview_eval` (DOM inspection) — el `preview_screenshot` puede dar timeout
4. `git add` + `git commit` + `git push origin main`
5. **Sincronizar SKILL.md en las 3 ubicaciones** (ver siguiente sección)

## Sincronización del SKILL.md (REGLA 🔴)

Cuando se actualice este SKILL.md, sincronizar en las 3 ubicaciones:

1. **Repo (visible en GitHub):** `C:/Users/segur/Desktop/acepo-segurosdigitales.com/SKILL.md`
2. **Skill instalado (Claude Code):** `C:/Users/segur/.claude/skills/especialista-acepo/SKILL.md`
3. **Backup en Downloads:** `C:/Users/segur/Downloads/SKILL_ACEPO.md`

Comando rápido para syncar las 3:

```bash
cp C:/Users/segur/Desktop/acepo-segurosdigitales.com/SKILL.md \
   C:/Users/segur/.claude/skills/especialista-acepo/SKILL.md && \
cp C:/Users/segur/Desktop/acepo-segurosdigitales.com/SKILL.md \
   C:/Users/segur/Downloads/SKILL_ACEPO.md
```

## Decisiones de diseño descartadas

- **SVG recreado del logo** — JC lo prohibió expresamente ("EL LOGO DEBE SER IDENTICO, NO PUEDES INVENTAR NI CAMBIAR NADA"). Sustituido por el PNG oficial.
- **Botón WhatsApp grande junto al CTA principal** — repartía la atención visual. Sustituido por botón flotante bottom-left con pulse animado.
- **Pill "✓ Respaldado por el INS" en el header** — redundante al agregar el logo INS BLANCO. Eliminada.
- **Stat "40+ años acompañando familias" en Actividades sociales** — la trayectoria pertenece al bloque de Respaldo institucional.
- **"No queda sujeto a revisión de la CCSS"** como ventaja propia de ACEPO — INCORRECTO. La CCSS emite el dictamen "no sujeto a revisión" y CON ese documento el INS adelanta. Reescrito.
- **Declaración de salud V7 en el paso 2 de afiliación** — ACEPO negoció que NO se requiera. Solo formulario autogestión de menos de 3 minutos.

## Reglas de trabajo con Juan Carlos (JC)

- JC NO programa. Necesita código completo o cambios ya pusheados.
- **No inventar datos del producto**: si una cifra no está en el PDF de condiciones particulares o en lo que JC dijo, no se pone. ACEPO es agente SUGESE — todo dato debe ser defendible.
- Pushear a main directo cuando JC autorice ("push", "actualiza", "listo", etc.).
- Verificación obligatoria antes de marcar completo: `preview_eval` para confirmar el cambio en el DOM. Si el `preview_screenshot` da timeout, no insistir — usar inspect/snapshot.
- Si JC se equivoca sobre un dato del producto, validar con el PDF de condiciones particulares antes de "corregir".
- **No mencionar SASINS, Reclamos-SDI ni otros proyectos** si JC no los invoca explícitamente.
