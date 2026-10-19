# Tropper Creations · tienda y panel interno

E-commerce de prendas y objetos sublimados (camisetas, pocillos, gorras y llaveros) con línea propia, línea personalizada y packs, más un panel interno de inventario, costeo, pedidos y roles.

**Proyecto:** Ingesoft Pro · **Ingeniero a cargo:** Jimmy Guerrero
**Estado:** prototipo funcional (primera vista). Los datos viven en el navegador para que el demo funcione sin backend; el esquema para Neon ya está listo en `src/server/db`.

## Qué incluye

| Tienda | Panel interno |
| --- | --- |
| Portada con personalizador en vivo (texto o imagen, papel en espejo y prensa) | Resumen con ventas, saldos por cobrar, margen y alertas |
| Catálogo por línea (Tropper / personalizada), categoría y tipo (unisex, pareja, individual) | Pedidos y pagos: validar comprobantes, mover estados, orden de producción |
| Ficha de producto con color, talla, diseño propio y favoritos | Inventario: insumos, máquinas, entradas y salidas, importación CSV y Excel |
| Packs con descuento fijo ($2.000 o $3.000) | Productos: crear, publicar, precio y fotos |
| Carrito, checkout y pago con Nequi, Daviplata o Llave Bre-B con anticipo del 50 % | Costeo y precios: egresos por pieza, margen, simulador y comparación con el mercado |
| Seguimiento del pedido y carga del comprobante | Packs con precio automático |
| Blog de uso, cómo pagar, mi cuenta, ingreso con Google o correo | Automatizaciones, usuarios y roles, configuración |

Roles: **super admin** (gerencia), **admin** (taller) y **cliente**. En `/ingresar` hay accesos de demostración para cada uno.

## Correr en local

```bash
npm install
npm run dev        # http://localhost:3000
npm run build      # compilación de producción
```

## Base de datos en Neon

```bash
cp .env.example .env.local     # pega tu DATABASE_URL de Neon
npm run db:migrate             # aplica drizzle/0000_init.sql
npm run db:seed                # carga productos, insumos, packs y configuración
```

## Documentación

- [`docs/ARQUITECTURA.md`](docs/ARQUITECTURA.md): arquitectura, modelo de datos, flujo de pagos, automatizaciones, costeo, seguridad y hoja de ruta.

## Stack

Next.js 16 (App Router) · React 19 · Tailwind CSS 4 · Zustand · Drizzle ORM · Neon Postgres · Vercel.
