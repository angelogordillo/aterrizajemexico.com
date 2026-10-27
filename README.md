# aterrizajemexico.com

Sitio web de **Aterrizaje México**, consultoría para la entrada de empresas extranjeras a México.

Es un sitio estático de una sola página: HTML y CSS, sin dependencias ni proceso de compilación.

## Estructura

```
index.html                Landing completa (estilos en línea)
gracias.html              Página tras enviar el formulario
aviso-de-privacidad.html  Aviso de privacidad integral
en/                       Versión en inglés (index, thank-you, privacy)
assets/favicon.svg        Ícono del sitio
assets/img/               Foto del fundador y logos de empresas y aliados
CNAME                     Dominio personalizado para GitHub Pages
```

## Ver en local

Abre `index.html` en el navegador, o sirve la carpeta:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Publicar con GitHub Pages

1. En el repositorio: **Settings → Pages → Build and deployment**, origen **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
2. El archivo `CNAME` ya apunta a `aterrizajemexico.com`.
3. En el proveedor del dominio, crea estos registros DNS:
   - `A` para `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` para `www` → `<usuario>.github.io`
4. Cuando el dominio verifique, activa **Enforce HTTPS**.

GitHub Pages gratuito requiere repositorio público; con un plan pago funciona también en privado.

## Pendientes

- **Formulario de contacto:** envía a angelo@aterrizajemexico.com vía FormSubmit (HTTPS). El primer envío llega como correo de activación que hay que confirmar una sola vez. Tras enviar, redirige a `gracias.html`.
- **Versión en inglés:** publicada en `/en/`. Al cambiar textos en español, actualizar también la versión en inglés.
- **Aviso de privacidad:** publicado en `aviso-de-privacidad.html`; falta completar el domicilio del responsable.

## Contacto

Angelo Gordillo Avila · angelo@aterrizajemexico.com · +52 56 1033 0956 · WhatsApp +52 55 7970 9893
