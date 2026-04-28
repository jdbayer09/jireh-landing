# JIREH Exportaciones y Asesorías S.A.S — Landing Page

Landing page corporativa para **JIREH Exportaciones y Asesorías S.A.S**, empresa colombiana especializada en la exportación de aguacate y productos agrícolas.

## 🛠️ Stack tecnológico

- [Astro 6](https://astro.build/) — Framework de generación estática
- [Tailwind CSS v4](https://tailwindcss.com/) — Estilos utilitarios (integrado vía `@tailwindcss/vite`)
- [Cloudflare Pages](https://pages.cloudflare.com/) — Hosting y despliegue

## Requisitos

- **Node.js** >= 22.12.0

## 📁 Estructura del proyecto

```text
/
├── public/                  # Archivos estáticos (favicon, imágenes)
├── src/
│   ├── assets/              # Imágenes optimizadas por Astro
│   ├── components/          # Componentes (Header, Hero, About, Services, Contact, Footer)
│   ├── config/
│   │   └── site.ts          # Configuración centralizada (empresa, contacto, redes)
│   ├── layouts/
│   │   └── Layout.astro     # Layout principal (meta, fuentes, dark mode)
│   ├── pages/
│   │   └── index.astro      # Página principal
│   └── styles/
│       └── global.css       # Tailwind CSS + custom variants
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## 🧞 Comandos

Todos los comandos se ejecutan desde la raíz del proyecto:

| Comando                              | Acción                                            |
| :----------------------------------- | :------------------------------------------------ |
| `npm install`                        | Instala dependencias                              |
| `npm run dev`                        | Inicia servidor de desarrollo en `localhost:4321` |
| `npm run build`                      | Genera el sitio estático en `./dist/`             |
| `npm run preview`                    | Vista previa del build localmente                 |
| `npx wrangler pages deploy dist`     | Despliega a Cloudflare Pages                      |

## ⚙️ Configuración centralizada

Todos los datos de la empresa (nombre, WhatsApp, email, redes sociales) están en un solo archivo:

```
src/config/site.ts
```

Para actualizar información de contacto o redes sociales, edita únicamente este archivo.

## 🌙 Modo oscuro

- Se activa automáticamente según la preferencia del sistema operativo
- El usuario puede alternar manualmente con el botón en el header
- La preferencia se persiste en `localStorage`
- Paleta oscura: tonos verdes (`green-950`, `green-900`, `green-800`)