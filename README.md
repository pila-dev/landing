# Pila Landing Page

Landing creada con **Astro** para presentar Pila: una app de finanzas personales que permite cargar ingresos, registrar gastos por categoría y seguir el balance en tiempo real.

## 🧩 Características

- Single page construida con componentes Astro (`Hero`, `StatsSection`, `FeaturesSection`, `StepsSection`, `FooterSection`, `TopBar`).
- Hero con CTA hacia las tiendas móviles y mockup/captura real de la app.
- Secciones de estadísticas, beneficios y pasos guiados alimentadas por arreglos (`features`, `steps`, `stats`) definidos en la página principal.
- Estilos encapsulados dentro de cada componente para facilitar el mantenimiento.

## 🗂️ Estructura relevante

```text
src/
├── assets/             # Logos, CTAs y captura principal
├── components/         # Hero, Stats, Features, Steps, Footer, TopBar
├── layouts/
│   └── Layout.astro    # Marco común (head meta, tipografía y variables globales)
└── pages/
    └── index.astro     # Única página pública que orquesta los componentes
```

## 🚀 Comenzar

1. **Instalar dependencias**
   ```bash
   npm install
   ```
2. **Entorno de desarrollo**
   ```bash
   npm run dev
   ```
   El servidor queda disponible (por defecto) en `http://localhost:4321`.
3. **Build de producción**
   ```bash
   npm run build
   ```
   Los artefactos se generan en `dist/`.
4. **Preview del build**
   ```bash
   npm run preview
   ```

## ✏️ Cómo editar el contenido

- Toda la data visible (copy + emojis) sigue concentrada al comienzo de `src/pages/index.astro`:
  - `heroContent`: eyebrow, título y cuerpo del hero.
  - `features`: tarjetas del bloque "Beneficios clave".
  - `steps`: lista del "Proceso guiado".
  - `stats`: indicadores que aparecen debajo del hero.
  - `currentYear`: controla automáticamente el año en el footer.
- Los estilos particulares están en cada componente dentro de `src/components/`.
- Las imágenes (logo, botones de tienda, captura) residen en `src/assets`. Reemplaza el archivo y mantén el mismo nombre/import.

## 🧪 Scripts disponibles

| Comando          | Descripción                                      |
| ---------------- | ------------------------------------------------ |
| `npm run dev`    | Levanta servidor de desarrollo con HMR           |
| `npm run build`  | Compila el sitio estático listo para producción  |
| `npm run preview`| Sirve el build para validación final             |

## 📦 Deploy

El resultado es 100 % estático, por lo que puede desplegarse en cualquier servicio como Vercel, Netlify, GitHub Pages o un bucket S3. Solo asegurate de publicar el contenido de `dist/`.

## 📄 Licencia

Este proyecto se basa en la plantilla básica de Astro. Ajusta esta sección según la licencia que prefieras utilizar para Pila.
