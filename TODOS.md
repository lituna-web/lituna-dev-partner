# Partner Page — Pendientes antes de producción

## Datos reales

- [ ] TODO[1]  Latencia: reemplazar `<800ms` con dato real medido en producción
- [ ] TODO[2]  Uptime: reemplazar `99.7%` con SLA real
- [ ] TODO[3]  Integraciones activas: reemplazar `12` con número real
- [ ] TODO[4]  Tiempo a primer deploy: reemplazar `<48h` con dato real
- [ ] TODO[5]  URL portal: reemplazar `https://portal.lituna.dev` con URL real
- [ ] TODO[6]  Casos de partners: reemplazar placeholders cuando haya casos reales
- [ ] TODO[7]  Email de contacto: verificar `partners@lituna.com` y confirmar monitoreo
- [ ] TODO[8]  URL documentación técnica: reemplazar `#` con URL real
- [ ] TODO[9]  URL preguntas frecuentes: reemplazar `#` con URL real
- [ ] TODO[10] Open Graph: agregar `og:image` cuando exista asset

## Analytics

Implementar `trackEvent()` en `index.html` antes de launch:

```js
function trackEvent(name, data) {
  gtag('event', name, data);
  // o: analytics.track(name, data);
}
```

## Modo IA — Diagnóstico dinámico

El componente `Diagnostico` acepta `mode: 'static' | 'ai'`.

Para activar modo IA:

```js
const diag = new Diagnostico(el, {
  mode: 'ai',
  aiEndpoint: 'https://api.lituna.dev/partner-profile'
});
```

El endpoint debe devolver: `{ title, tag, intro, benefits[], ctaLabel }`

## Notas de diseño

Editar `:root` en el bloque `<style>` para cambiar identidad visual:
- `--color-accent` → color de acento
- `--color-bg` → fondo base
- `--font-display` → tipografía editorial
- `--font-body` → tipografía de texto corrido
- `--font-mono` → tipografía monoespaciada
