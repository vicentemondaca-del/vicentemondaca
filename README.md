# vicentemondaca

Página personal de Vicente Mondaca. Es HTML y CSS puro: no hay build, no hay dependencias,
no hay nada que instalar. Cloudflare Pages toma los archivos tal cual y los publica.

El diseño sigue el design system de ComunidadFeliz: Montserrat, verde de marca `#4CBF8C`
para botones e íconos, `#00A27F` como único verde para texto, y espaciado en múltiplos de 4px.

```
index.html    la página
estilos.css   colores, tipografía y layout
favicon.svg   el ícono de la pestaña
```

Para verla en tu computador basta con abrir `index.html` en el navegador.

## Cómo se publica

El repo está conectado a Cloudflare Pages. Cada `git push` a `main` publica la página de nuevo,
sola, en uno o dos minutos.

Configuración del proyecto en Cloudflare:

| Campo | Valor |
|---|---|
| Framework preset | None |
| Build command | *(vacío)* |
| Build output directory | `/` |
| Production branch | `main` |

## Demo para la clase

1. **Cambiar algo y verlo publicado.** Edita el pie de página en `index.html`
   (`Versión 1` → `Versión 2`), y luego:
   ```bash
   git add index.html
   git commit -m "Versión 2"
   git push
   ```
   En Cloudflare, *Workers & Pages → vicentemondaca → Deployments* aparece el deploy nuevo.
   Cuando termina, recarga la página.

2. **Agregar una tarjeta.** En *En qué trabajo* de `index.html` se copia un `<li class="tarjeta">`
   completo, se cambia el título y el texto, y se hace push igual que arriba. La grilla la
   acomoda sola.

3. **Cambiar un color.** Todos los colores están arriba en `estilos.css`, en `:root`.
   Cambiar `--cf-green` cambia de una vez los botones, los íconos y el avatar. Después se
   vuelve a `#4CBF8C`, que es el verde de marca.

4. **Preview antes de publicar.** Si haces push a una rama que no sea `main`, Cloudflare
   la publica en una URL aparte (`https://<rama>.vicentemondaca.pages.dev`) sin tocar la
   página real. Sirve para mostrarle un cambio a alguien antes de mergearlo.
