# 🌙 Lunaris

Catálogo virtual de productos para un negocio: la web muestra el catálogo con búsqueda, filtros y detalle de producto, y la API lee los productos desde Google Sheets.

🌐 **Web:** [juanfeds.com/lunaris](https://juanfeds.com/lunaris/)

## Estructura

```
lunaris/
├── web/   # Catálogo en Next.js (export estático, Tailwind, Jest)
├── api/   # API en Node desplegada en Vercel, con Google Sheets como base de datos
└── .github/workflows/
    └── web.yml   # Lint, type check, tests, export y deploy a GitHub Pages
```

La API se despliega en Vercel con *Root Directory* = `api/`.

## Desarrollo

**Web**

```bash
cd web
npm install
npm run dev
```

**API**

```bash
cd api
npm install
npm run dev
```

La API necesita `GOOGLE_SHEETS_ID` y `GOOGLE_SHEETS_API_KEY` en un `.env`. Detalle de cada parte en [`web/README.md`](web/README.md) y [`api/README.md`](api/README.md).
