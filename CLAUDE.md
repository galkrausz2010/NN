# CLAUDE.md — NaturalNet (NN)

Guía para Claude (y cualquier colaborador) al trabajar en este repositorio.

## Proyecto

**NaturalNet** es una aplicación móvil de tipo **webapp** (web app optimizada para móvil, instalable como PWA).

- Repositorio: https://github.com/galkrausz2010/NN
- Rama principal: `main`
- Idioma del proyecto y la documentación: español

## Estado actual

Proyecto recién iniciado. Aún no se ha definido el stack tecnológico, el alcance funcional ni el diseño.
Ver [PROGRESS.md](PROGRESS.md) para el historial y los siguientes pasos.

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

_Pendiente de definir._ Cuando se elija, documentar aquí:

- Framework / librerías
- Cómo instalar dependencias
- Cómo arrancar en desarrollo
- Cómo compilar y desplegar
- Cómo ejecutar tests

## Estructura del repositorio

```
CLAUDE.md     Guía y reglas del proyecto
PROGRESS.md   Registro de progreso y cambios
```
