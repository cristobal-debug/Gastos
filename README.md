# Gastos 2026 — Panel Financiero

App web para visualizar gastos bancarios desde Google Sheets.

## Estructura

```
gastos-2026/
├── index.html     ← toda la app (HTML + CSS + JS)
├── vercel.json    ← configuración de despliegue
└── README.md
```

## Configuración

En `index.html`, busca el bloque `CONFIG` (línea ~170):

```js
const CONFIG = {
  PIN:        '021111',          // ← tu PIN de acceso
  SHEET_ID:   '1ZpsF94DV7...',  // ← ID de tu Google Sheet
  SHEET_NAME: '2026 MOVIMIENTOS', // ← nombre exacto de la hoja
  PER_PAGE:   30,
};
```

## Requisito del Sheet

Tu Google Sheet debe estar compartido como **público** (cualquiera con el link puede ver).

Para verificarlo:
1. Abrí el Sheet → Compartir
2. "Cualquier persona con el link" → Lector

## Deploy en Vercel

1. Subí esta carpeta a GitHub
2. En Vercel → "Add New Project" → importá el repo
3. Framework: **Other** (detección automática)
4. Clic en **Deploy**

Vercel detecta el `vercel.json` y despliega automáticamente.

## Actualización de datos

Cuando agregues filas nuevas al Sheet, la app las muestra al instante
al pulsar **Actualizar** — sin necesidad de redesplegar en Vercel.
