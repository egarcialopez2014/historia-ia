# De ver a actuar

Una historia animada de la IA en seis etapas, pensada para proyectarse en una charla y abrirse después en el móvil mediante un QR.

Publicada en **https://ia.egarcialopez.dev**.

## Contenido

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La web completa: HTML, CSS, JavaScript, gráfico SVG y QR, todo en un solo archivo. |
| `CNAME` | El dominio personalizado de GitHub Pages. |

La página funciona sin conexión. No usa CDN, fuentes externas ni imágenes.

## Antes de la charla: poner las cifras reales

Al principio del `<script>` de `index.html` hay dos constantes:

```js
const MINUTOS = null; // minutos reales que tardó el agente
const PROMPTS = null; // instrucciones que se le dieron
```

Sustituye `null` por números, por ejemplo `const MINUTOS = 25;`. Mientras valgan `null`, la última pantalla dice «Unos minutos · unas pocas instrucciones».

Después, sube el cambio:

```sh
git commit -am "Cifras reales para la charla"
git push
```

GitHub Pages publica la nueva versión en uno o dos minutos.

## Cómo presentarla

- **Flechas, Avanzar página / Retroceder página y Espacio** pasan de una etapa a otra. Son las teclas que envían los mandos de presentación.
- **Inicio y Fin** saltan a la portada y a las fuentes.
- También funciona con el desplazamiento normal y en el móvil.
- Para usarla sin internet, abre `index.html` directamente en el navegador.

## Cómo se despliega

El repositorio publica la rama `main` con GitHub Pages, desde la raíz. El archivo `CNAME` apunta al dominio `ia.egarcialopez.dev`.

Para que el dominio funcione, el DNS de `egarcialopez.dev` necesita este registro:

```
ia   CNAME   egarcialopez2014.github.io.
```

Cuando el DNS resuelva, activa «Enforce HTTPS» en Settings › Pages.

## Datos

Cada cifra está verificada y enlazada en la sección «Fuentes» de la página. El gráfico usa los datos publicados por METR, versión 1.1 de su medida de horizonte temporal, consultados en octubre de 2026.
