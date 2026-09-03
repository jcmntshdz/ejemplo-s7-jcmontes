# CLAUDE.md

Este archivo lo lee Claude cada vez que trabaja en esta carpeta, sin que se lo pidas.
Lo vas a llenar en la sesión. Por ahora trae solo las reglas que aplican desde el
primer minuto.

---

## 1. Qué es este proyecto y quién lo usa

Es un buzón de sugerencias para mi equipo. Lo uso yo (Jc) y todo el equipo, para
mandar sugerencias cuando surgen y revisarlas cuando hace falta.

## 2. De dónde sale cada cifra

Los datos de esta página viven en una tabla de Supabase llamada `registros`.
Ninguna cifra ni ningún texto que se muestre se escribe a mano en el HTML: todo
sale de esa tabla o de lo que la persona escriba en el formulario.

Columnas de `registros`: `id` (identity), `nombre` (texto), `mensaje` (texto),
`created_at` (fecha, se llena sola con `now()`).

## 3. Cómo quiero que trabajes aquí

- Antes de un cambio grande, dame el plan por escrito y espera mi visto bueno.
- Un cambio a la vez. Enséñame qué cambió antes de escribirlo.
- Trabaja siempre en una rama, nunca directo sobre `main`.
- Cuando el cambio en la rama esté listo: haz `git pull`, fusiona a `main` y despliega
  todos los cambios en producción —Netlify y Supabase— sin esperar mi aprobación.
- Si el cambio incluye SQL sobre mi base de datos, enséñamelo igual para que quede
  registro, pero no esperes mi respuesta para correrlo.

## 4. Lo que nunca debes hacer

- **Nunca escribas en esta carpeta una llave que empiece con `sb_secret_` o que
  diga `service_role`.** La única llave que puede estar aquí es la que empieza
  con `sb_publishable_`, que está hecha para andar a la vista.
- No inventes datos. Si algo no está en la tabla, que la página diga que no hay
  nada todavía, no un ejemplo.
- No borres el historial ni fuerces cambios sobre lo ya publicado.

## 5. Mi regla de verificación

Antes de dar algo por publicado: hice `git pull` de la rama para traer lo último,
fusioné a `main`, y confirmé que ya se ve en la liga de Netlify y que los cambios
de base de datos, si los hubo, ya corrieron en Supabase.
Si no puedo decir "hice pull, fusioné y desplegué", no está listo.

## 6. Cómo vuelvo a abrir esto

- El proyecto vive en este repositorio de GitHub.
- Se abre pidiéndole a Claude una sesión sobre este repo; no hace falta descargarlo.
- La página publicada está en la liga que da Netlify.
- La base de datos está en supabase.com, en el proyecto de esta cuenta.

> **Si la página deja de mostrar datos después de una semana sin usarla**, casi
> siempre es que el proyecto gratuito de Supabase se pausó. Se despierta con el
> botón **Resume project**.

## 7. Sistema de diseño

- Colores: rojo, negro y blanco.
- Tipografía: Arial.
