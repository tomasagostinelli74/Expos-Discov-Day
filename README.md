# Aranceles UADE — página para prospectos

Página de un solo archivo (`index.html`, sin build ni servidor) para que los prospectos consulten el arancel de su carrera: menú con las 7 facultades → carreras de cada facultad → PDF del arancel.

## Actualizar datos

Todo se edita al principio del `<script>` de `index.html`:

- **`CONFIG.cohortes`** — períodos de ingreso a la venta. Hoy solo Marzo 2027; para volver a vender Agosto, descomentar su línea (los links ya están cargados).
- **`FACULTADES`** — orden, nombre, color e ícono de cada facultad.
- **`CARRERAS`** — una fila por carrera: `[FACULTAD, NOMBRE, LINK PDF MARZO, LINK PDF AGOSTO]`.
  Las sedes y modalidades van entre paréntesis (`"Abogacía (Sede Recoleta)"`) y se agrupan solas bajo la misma carrera.

Fuente de los links: `crm.uade.edu.ar/Aranceles` (FACO figura como FAEN; Comunicación, Comunicación Global, Publicidad y RR.PP. pasaron a FAJU).

## Deploy

GitHub + Vercel (Framework Preset **Other**, sin build command). Cada `git push` a `main` vuelve a publicar.
