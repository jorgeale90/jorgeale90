# 🎮 Plan para materializar tu perfil de GitHub

## Paso 1 — Crear el repo especial (5 min)

GitHub muestra el README en tu portada solo si el repo se llama **exactamente igual que tu usuario**:

1. Ve a https://github.com/new
2. Nombre del repo: `jorgeale90`
3. Público ✅ · marca "Add a README file"
4. GitHub mostrará el banner "✨ jorgeale90/jorgeale90 is a special repository"

## Paso 2 — Subir el README

Reemplaza el contenido del README con el archivo `README.md` que te generé:

```bash
git clone https://github.com/jorgeale90/jorgeale90.git
cd jorgeale90
# copia aquí el README.md generado
git add README.md
git commit -m "feat: profile README"
git push
```

## Paso 3 — Añadir los GIFs de Mario (10 min)

El README referencia dos GIFs locales para que nunca se rompan (los servicios externos de GIFs caducan):

1. Crea la carpeta `assets/` en el repo
2. Descarga dos GIFs pixel-art de Mario (fondo transparente idealmente):
   - Mario corriendo → guárdalo como `assets/mario-running.gif`
   - Mario en la bandera/castillo → guárdalo como `assets/mario-flag.gif`
   - Fuentes: Tenor, Giphy o https://www.deviantart.com buscando "mario running pixel gif transparent"
3. Commit y push:

```bash
git add assets/
git commit -m "feat: add Mario gifs"
git push
```

> ⚠️ Nota legal: los sprites de Mario son propiedad de Nintendo. Para un perfil personal es práctica común y tolerada, pero si prefieres cero riesgo, usa un pixel-art genérico de un personaje corriendo (itch.io tiene sprites libres) o cambia a la "snake" de contribuciones (paso 6).

## Paso 4 — Verificar los widgets dinámicos

Estos servicios ya funcionan sin configuración (solo dependen de tu usuario `jorgeale90`):

| Widget | Servicio |
|---|---|
| Banner animado header/footer | capsule-render.vercel.app |
| Texto que se escribe solo | readme-typing-svg.demolab.com |
| Stats + Top languages | github-readme-stats.vercel.app |
| Racha de contribuciones | streak-stats.demolab.com |
| Gráfico de actividad | github-readme-activity-graph.vercel.app |
| Contador de visitas | komarev.com |
| Iconos de skills | skillicons.dev |

Si alguno tarda en cargar la primera vez es normal (cold start de Vercel).

## Paso 5 — Ajustes de privacidad de stats

- En `github-readme-stats` el parámetro `count_private=true` solo funciona si tú mismo despliegas la instancia; con la pública se cuentan solo repos públicos.
- Si tus contribuciones son mayormente privadas (trabajo), activa en GitHub: Settings → Profile → **Include private contributions on my profile**.

## Paso 6 — (Opcional) Snake animada con GitHub Actions

Si más adelante quieres añadir la serpiente que se come tus contribuciones:

1. Crea `.github/workflows/snake.yml` con la action `Platane/snk`
2. Se regenera sola cada 12 h y publica el SVG en la rama `output`
3. La añades al README con una sola línea de imagen

Dímelo y te genero el workflow listo.

## Paso 7 — Verificación final

- Abre https://github.com/jorgeale90 en incógnito y revisa que todo renderiza
- Prueba en modo claro y oscuro de GitHub (el tema del README es oscuro fijo, se ve bien en ambos)
- Revisa en el móvil: las stats cards se apilan verticalmente, es el comportamiento esperado

## Personalización rápida

- **Colores**: el esquema actual es rojo Mario `#e60012` + amarillo moneda `#ffcb05` + fondo Tokyo Night `#1a1b27`. Se cambian en los parámetros `color`, `bg_color`, `title_color` de cada URL.
- **Frases del typing**: edita el parámetro `lines=` (separadas por `;`, espacios como `+`).
- **Niveles/mundos** de la tabla de experiencia: puro markdown, edítalo a gusto.
