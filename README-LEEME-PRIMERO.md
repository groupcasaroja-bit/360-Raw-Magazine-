# 360 Raw Magazine — panel editorial (guía en español)

## Qué incluye
- La identidad visual negra, blanca y verde lima de la página HTML que compartiste.
- Un generador de sitio (Eleventy) para convertir las noticias Markdown en páginas web.
- Decap CMS en `/admin/` para crear, editar y preparar borradores de noticias.
- Campos para titular, fecha, categoría, autor, resumen, fotografía, etiquetas y contenido.
- Configuración inicial de Netlify (`netlify.toml`).

## Importante antes de subirlo
Este ZIP es una base de integración creada a partir del HTML que compartiste. **No se ha instalado en tu sitio publicado y no puede reemplazar el repositorio real sin revisarlo.** No subas este proyecto encima de tu sitio existente sin hacer una copia de seguridad. El diseño original se ha mantenido como base, pero hay que probar el resultado antes de publicar.

## Pasos sin programar
1. En GitHub, abre el repositorio que publica `360-raw-magazine.netlify.app`.
2. Descarga una copia de seguridad del repositorio antes de cambiar nada.
3. Sube los archivos de este ZIP al repositorio. Si ya existen archivos con el mismo nombre, no los reemplaces a ciegas: primero hay que comparar.
4. En `admin/config.yml`, cambia `YOUR_GITHUB_USERNAME/YOUR_REPOSITORY` por la dirección real del repositorio, por ejemplo `miusuario/mi-revista`.
5. En Netlify, abre **Site configuration / Build & deploy** y configura el comando de compilación `npm run build` y la carpeta publicada `_site`. El archivo `netlify.toml` también contiene estos valores si Netlify está configurado para leerlo.
6. Configura la autenticación de Decap CMS para GitHub con el método OAuth seguro compatible con tu sitio. No pongas un client secret, contraseña o token en archivos públicos. El panel no permitirá iniciar sesión hasta completar esta parte.
7. Espera el despliegue y comprueba primero la portada y después `/admin/`.
8. En el panel, crea una noticia de prueba, guarda como borrador, revisa la vista previa y publícala. Comprueba que aparece en portada y que su imagen carga.

## Para publicar una noticia después de la instalación
1. Abre `https://360-raw-magazine.netlify.app/admin/`.
2. Inicia sesión con la cuenta autorizada.
3. Entra en **Noticias → Nueva noticia**.
4. Completa titular, fecha, categoría, autor, resumen y contenido. Sube una fotografía principal si corresponde.
5. Guarda como borrador o envía para revisión y publica cuando esté lista.

## Límites conocidos
- El formulario de suscripción del HTML original es demostrativo; todavía no guarda correos. Debe conectarse a un proveedor de newsletter.
- La autenticación de CMS requiere configuración aparte.
- El diseño actual del HTML es una portada editorial de demostración. El ZIP añade el sistema de artículos, pero hay que validar rutas, estilos, imágenes y autenticación en un despliegue de prueba.
- El CMS crea contenido en GitHub; Netlify vuelve a generar el sitio cuando se activa el despliegue automático.
