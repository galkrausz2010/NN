# CLAUDE.md — NaturalNet (NN)

Guía para Claude (y cualquier colaborador) al trabajar en este repositorio.

## Proyecto

**NaturalNet** es una aplicación móvil de tipo **webapp** (web app optimizada para móvil, instalable como PWA).

- Repositorio: https://github.com/galkrausz2010/NN
- Rama principal: `main`
- Idioma del proyecto y la documentación: español

## Estado actual

Existe un **prototipo funcional en un solo archivo HTML**: [`prototipo/fichafacil.html`](prototipo/fichafacil.html) ("FichaFácil"), una app de **fichaje / control horario** para personal de limpieza que trabaja en varios centros (restaurantes, oficinas, hoteles, colegios, tiendas...).

- Roles: trabajador/a (vista móvil: fichar entrada/salida, pausas, historial), supervisor/a y administración (panel con fichajes en vivo, alertas, informes, centros, trabajadores).
- Acceso por PIN; fichaje por GPS (radio del centro) o código QR; soporte sin conexión.
- Incluye datos de demostración (trabajadores, centros y fichajes ficticios en Barcelona).
- Se creó como Artifact de Claude: usa `window.claude.use('db')` y `('downloads')` si existen y, si no, recurre a `localStorage`, así que también funciona abierto directamente en el navegador.

Aún no se ha definido el stack definitivo. Ver [PROGRESS.md](PROGRESS.md) para el historial y los siguientes pasos.

## Reglas de trabajo (obligatorias)

1. **Cada cambio actualiza `PROGRESS.md`**: añadir una entrada en el registro de cambios con fecha (AAAA-MM-DD), qué se hizo y por qué. Actualizar también las secciones "Estado" y "Próximos pasos" si cambian.
2. **Cada cambio se commitea y se pushea a GitHub** (`origin/main`, salvo que se indique trabajar en otra rama).
   - Mensajes de commit en español, claros y en imperativo (p. ej. `Añade pantalla de inicio`).
   - Un commit por cambio lógico; el commit incluye la actualización de `PROGRESS.md`.
3. Mantener este `CLAUDE.md` al día cuando se tomen decisiones de arquitectura, stack, convenciones o comandos nuevos.

## Principios de la webapp

- **Mobile-first**: diseñar primero para pantallas de ~360–430 px de ancho.
- Interfaz táctil: áreas de toque ≥ 44 px, sin dependencia de hover.
- Pensada para instalarse como **PWA** (manifest + service worker) y funcionar con conexión inestable.
- Accesibilidad básica: contraste suficiente, etiquetas en formularios, soporte de modo oscuro.

## Stack y comandos

**Objetivo de infraestructura (decidido):**
- **Vercel** para desplegar y alojar la webapp.
- **Supabase** como backend: base de datos PostgreSQL, autenticación de usuarios, almacenamiento y (si hace falta) funciones.

Toda decisión técnica nueva debe ser compatible con este despliegue (p. ej. framework que Vercel soporte bien, datos en Supabase en lugar de `localStorage`).

Framework y comandos: _pendientes de definir._ Cuando se elijan, documentar aquí:

- Framework / librerías
- Cómo instalar dependencias
- Cómo arrancar en desarrollo
- Cómo compilar y desplegar
- Cómo ejecutar tests

## Estructura del repositorio

```
CLAUDE.md                   Guía y reglas del proyecto
PROGRESS.md                 Registro de progreso y cambios
prototipo/fichafacil.html   Prototipo de la app (HTML + CSS + JS en un solo archivo)
```
