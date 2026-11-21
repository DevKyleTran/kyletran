# Kyle Tran — website developer

A portfolio site for a Wisconsin website developer: a home page with hero,
business types, selected work, services, process, testimonials, pricing and an
about section; a work index with project pages; pricing with add-ons and an
FAQ; and a contact brief. Copy lives in `src/data/projects.ts`; photography in
`public/images`.

The visual system is the editorial theme from this template: cream canvas, ink
text, a single terracotta accent, Instrument Serif for display type and Inter
for the rest. Everything rounded is a squircle via `corner-shape`.

## Run it

Requires Node 20+ (Node 22+ recommended, for the built-in test runner).

```sh
npm install
npm run dev        # http://localhost:5173
npm run build      # dist/client (assets) + dist/store/index.js (Worker)
npm run preview    # serve the production build
npm run typecheck
npm test           # API tests, via Node's built-in runner
```

## Make it yours

- `src/data/projects.ts` — projects, services, prices, add-ons, FAQ and contact
  details.
- `src/app/pages/*` — the screens; `src/app/components/*` — nav, footer, project
  cards, tier cards and primitives.
- `src/styles.css` — the tokens (canvas, ink, accent, fonts, radii).
- `src/worker/index.ts` — validates `/api/contact` and returns a demo
  reference. Nothing is emailed or stored; wire it to a mailbox, D1 or a CRM
  when you need real leads.

## Deploy with Freebuff Sites

`deploy.json` points at the build output. After `npm run build`, deploy with
the `sites_deploy` tool from this directory, or upload `dist/client` to any
static host (plus `dist/store/index.js` as the Worker if you need the contact
endpoint).
