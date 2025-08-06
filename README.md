# Pokedex for CI

Este proyecto es una SPA (Single Page Application) desarrollada en React que simula una Pokédex. Se integró un pipeline de CI con GitHub Actions y se desplegó a Vercel.

## 🔧 Tecnologías

- React
- GitHub Actions
- Vercel (Hosting)
- Jest / ESLint

## 🚀 CI/CD

El flujo incluye:
- Instalación de dependencias
- Linting (`eslint`)
- Pruebas con `jest`
- Deploy automático a Vercel


## 🐛 Problemas conocidos

En Vercel, las imágenes podrían no cargarse si:
- No están en `/public`
- Se usan rutas relativas mal construidas
- No se incluye `_redirects` si se usa React Router

**Solución sugerida:**
1. Usa rutas absolutas para imágenes desde `public` (`/img.png`).
2. Agrega un archivo `_redirects` para SPA:
   ```
   /* /index.html 200
   ```


