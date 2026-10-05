# supay-docs — Documentación y SDK de Supay (Fern)

Fuente de verdad para docs.supay.dev y el SDK TypeScript `@supay/sdk`.
Movido desde `supay/backend/fern` + `supay/backend/sdks/typescript` el 2026-10-05.

## Estructura

```
supay-docs/
  fern.config.json          # org: supay
  docs.yml                  # site: docs.supay.dev
  generators.yml            # SDK TS -> ./sdks/typescript
  supay-v1.openapi.yml      # contrato canónico v1
  una-factura.openapi.yml   # spec parcial (una factura)
  docs/pages/               # MDX por sección
  assets/                   # favicon + logos
  sdks/typescript/          # SDK generado (no editar a mano)
```

## Comandos

```bash
# preview docs
fern docs dev

# regenerar SDK tras cambiar el OpenAPI
fern generate --local --group local --force

# compilar SDK
(cd sdks/typescript && npm run build)
```

## Publicación

- Docs: `fern docs publish` (o CI hacia docs.supay.dev)
- SDK: aún no publicado en npm; instalar por ruta local hasta publicar.
