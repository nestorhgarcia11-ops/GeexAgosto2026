[README.md](https://github.com/user-attachments/files/31011720/README.md)
# Evaluación de estado de salud — OSTACC · ATACC

Cuestionario web confidencial de tamizaje de salud para afiliados. Es una **aplicación de un solo archivo** (`index.html`), sin dependencias ni servidor: funciona abriéndola en cualquier navegador y se puede publicar como sitio estático.

## Qué incluye

- Identificación mínima (DNI, fecha de nacimiento, sexo) y consentimiento por casilla.
- Secciones: hipertensión, historia de salud (con tamizaje colorrectal ajustado por edad), peso y medidas (IMC + perímetro de cintura), antecedentes tóxicos (**AUDIT-C**), salud de la mujer, ánimo y bienestar (**PHQ-4**), alimentación, ITS y —desde los 60— memoria y cognición.
- Puntajes automáticos: riesgo de diabetes (**ADA-CDC**), riesgo de hipertensión, IMC, AUDIT-C, PHQ-2 / GAD-2.
- **Aviso prioritario** ante señales de alarma (dolor de pecho, signos de ACV, etc.).
- Resumen con derivaciones sugeridas, **impresión/PDF**, **enlace de resultado** para el equipo de salud y **descarga en JSON** para el pipeline de análisis.

## Publicar en GitHub Pages

1. Iniciá sesión en github.com y creá un repositorio nuevo (por ejemplo `evaluacion-salud`), **público**.
2. En el repositorio: **Add file → Upload files** y subí `index.html` (y opcionalmente `.nojekyll` y este `README.md`). **Commit changes**.
3. **Settings → Pages**. En *Source* elegí **Deploy from a branch**, rama **main**, carpeta **/(root)**. **Save**.
4. Esperá 1–2 minutos. La URL pública queda con el formato:
   `https://TU-USUARIO.github.io/evaluacion-salud/`

El archivo se llama `index.html` a propósito: así el sitio abre directo en esa dirección, sin agregar nada al final.

Para actualizarlo, volvé a subir `index.html` con el mismo nombre y GitHub republica solo.

## Privacidad (importante)

- El **formulario en blanco** es público, y eso está bien: la app no guarda ni envía datos por sí sola.
- El botón **"Enviar al equipo de salud"** genera un enlace que lleva las respuestas dentro de la propia URL (`#r=...`). Ese enlace contiene datos personales: **compartirlo solo con OSTACC**, nunca publicarlo.
- Los sitios de GitHub Pages son públicos en internet aunque el repositorio sea privado. Por eso esta versión sirve como **piloto/demo**. Para uso real con recolección segura y centralizada de respuestas (base cifrada, acceso autenticado, separada de RRHH), hace falta un backend.

## Notas clínicas

Es un tamizaje **orientativo, no diagnóstico**. Conviene que el equipo de OSTACC/ATACC valide los puntos de corte (ADA-CDC, AUDIT-C, perímetro de cintura, franjas de edad del tamizaje colorrectal) antes del uso real.
