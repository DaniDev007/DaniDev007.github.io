# Portfolio — publicación en GitHub Pages

Este repositorio contiene la versión web compilada del portfolio. El código editable continúa en Replit; aquí se suben únicamente los archivos públicos necesarios para mostrar la web.

## Publicar por primera vez

1. En este repositorio, abre **Settings → Pages**.
2. En **Build and deployment → Source**, selecciona **GitHub Actions**.
3. Abre **Actions → Publicar portfolio**.
4. Pulsa **Run workflow**, selecciona `main` y confirma.
5. Espera a que termine correctamente. GitHub mostrará el enlace de la web en **Settings → Pages** y en la ejecución.

La preparación de los archivos no ejecuta esta publicación. El proceso se inicia únicamente cuando eliges **Run workflow**.

## Usar un dominio propio más adelante

No necesitas cambiar el nombre del repositorio. Cuando compres el dominio:

1. Verifica que el dominio es tuyo siguiendo la documentación de GitHub.
2. Añádelo en **Settings → Pages → Custom domain**.
3. Configura los registros DNS en la empresa donde lo compraste.
4. Activa **Enforce HTTPS** cuando el certificado esté disponible.

El título visible del portfolio puede cambiarse independientemente del repositorio o del dominio.

Guía oficial: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Actualizar el portfolio desde Replit

En el workspace original:

```sh
PORT=5000 BASE_PATH=/ pnpm --filter @workspace/daniel-portfolio run build
node scripts/prepare-portfolio-pages.mjs
node scripts/upload-portfolio-pages.mjs
```

Después, repite **Actions → Publicar portfolio → Run workflow** para actualizar la web.

El script de subida utiliza la conexión de GitHub de Replit: no se deben introducir claves en el código, en este repositorio ni en la conversación.

## Qué se incluye

- La página principal y Other work.
- Los estilos y el JavaScript compilados.
- Las imágenes, los vídeos y el CV que ya son públicos en el portfolio.
- Un proceso de publicación manual.

No se incluyen el backend, archivos originales de chat, notas del agente, secretos ni configuración privada del workspace. Los medios existentes se conservan sin recomprimir ni alterar.
