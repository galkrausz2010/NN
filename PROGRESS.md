# Progreso — NaturalNet (NN)

## Estado

Fase: **Prototipo**. Hay un prototipo funcional de la app de fichaje (FichaFácil) en `prototipo/fichafacil.html`.

## Próximos pasos

- [x] Prototipo inicial de la app de fichaje (FichaFácil)
- [ ] Revisar el prototipo y confirmar funcionalidades principales de NaturalNet
- [x] Decidir hosting y backend: **Vercel** + **Supabase**
- [ ] Elegir el framework de la webapp (compatible con Vercel)
- [ ] Crear proyecto en Supabase y diseñar el esquema de datos (trabajadores, centros, fichajes)
- [ ] Conectar el repositorio a Vercel para despliegue automático
- [ ] Convertir el prototipo en app real (mobile-first, PWA, backend con usuarios y datos persistentes)
- [x] Aplicar identidad visual de NaturalNet (colores, tipografía, logotipo)
- [x] Sustituir el logotipo dibujado por el archivo oficial de NaturalNet
- [ ] Conseguir el logotipo en alta resolución o SVG (el actual es de 300×77 px)

## Registro de cambios

### 2026-09-24
- Sustituye el logotipo dibujado por el logotipo oficial de NaturalNet (`prototipo/assets/logo-naturalnet.jpg`) en acceso, vista de trabajador y panel de administración.
- Aplica el branding de NaturalNet al prototipo: colores de naturalnet.es (verde, azul marino, azul cielo), tipografía Open Sans, logotipo NaturalNet y lema en la pantalla de acceso; sustituye todas las menciones a "FichaFácil".
- Registra la decisión de infraestructura: despliegue en Vercel y backend en Supabase (documentado en `CLAUDE.md`).
- Añade el prototipo `prototipo/fichafacil.html` (importado desde el Artifact de Claude): fichaje por GPS/QR, pausas, historial, panel de administración con datos de demo. Documentado en `CLAUDE.md`.
- Inicializa el repositorio con `CLAUDE.md` (guía y reglas de trabajo) y `PROGRESS.md` (seguimiento de cambios).
