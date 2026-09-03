# Buzón de sugerencias

Página del equipo de Jc: cualquiera manda una sugerencia por un formulario y se
puede revisar la lista de lo mandado.

**Datos:** todo sale de la tabla `registros` en Supabase (columnas `id`,
`nombre`, `mensaje`, `created_at`). Nada se escribe a mano en el HTML.

**`.claude/agents/revisor-antes-de-publicar.md`:** agente de solo lectura que
revisa el código antes de publicar (llaves expuestas, alcance del cambio,
calidad). Se dispara pidiéndole a Claude que revise antes de publicar.

**Estado actual:** `index.html` sigue siendo la página de prueba de la sesión;
falta pedirle a Claude que la reemplace por el formulario y la lista reales.

**Para continuar:**
1. Abre una sesión de Claude sobre este repositorio.
2. Pide el cambio en una rama, nunca en `main`.
3. Netlify da una vista previa por rama; se revisa ahí.
4. Al fusionar a `main`, Netlify publica solo. Reglas completas en `CLAUDE.md`.
