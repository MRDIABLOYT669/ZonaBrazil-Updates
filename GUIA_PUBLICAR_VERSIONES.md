# Guía para publicar actualizaciones — Zone Brazil Mac

## 1. Generar el instalador completo

En la Mac del desarrollador, conserva la carpeta `~/Downloads/ZoneBrasil-1.3.9-64bits` y un DMG/ZIP anterior con el entorno funcional para Mac. Descomprime el constructor **Zona Brazil 4.5 Builder**, abre `CREAR_INSTALADOR.command` y prepara el único instalador `.pkg` con el juego y el lanzador incluidos.

**Antes de compartir:** pruébalo desde una instalación limpia de macOS. No publiques archivos que contengan sesiones, contraseñas o datos privados.

## 2. Crear el primer Release

1. En GitHub abre `Releases` → `Draft a new release`.
2. Crea etiqueta **`v1.3.9`**, basada en `main`.
3. Título sugerido: **`Zone Brazil 1.3.9 — macOS`**.
4. Adjunta el archivo único **`Zona Brazil.pkg`** generado en tu Mac.
5. Redacta las novedades, requisitos y limitaciones de compatibilidad.
6. Comprueba que el instalador es el correcto; publica el Release como estable (no Draft ni Prerelease).

## 3. Futuras versiones

Cuando dispongas de la siguiente compilación, por ejemplo `1.4.0`:

1. Actualiza el juego empaquetado y la versión `GameVersion.txt` del lanzador.
2. Genera un nuevo `.pkg`, **conservando el mismo nombre de aplicación y el mismo identificador de paquete** para facilitar la actualización.
3. Firma y notariza el paquete si corresponde; prueba la actualización conservando partidas y configuraciones.
4. Publica un Release con etiqueta **`v1.4.0`** y el nuevo `.pkg`.
5. Los lanzadores 4.5 comprobarán automáticamente la versión en GitHub cuando se abran; si es más reciente, ofrecerán descargarla y abrir el instalador.

## Formato y controles de seguridad

- Etiquetas de versión: `vMAYOR.MENOR.PARCHE`, por ejemplo `v1.3.9` y `v1.4.0`.
- Adjuntar un archivo `.pkg` en cada Release estable.
- El lanzador 4.5 exige que GitHub exponga una huella `digest: sha256:...` para el instalador. Si falta, **no lo descargará**, como medida de seguridad.
- GitHub Releases tiene límites por archivo: si un `.pkg` excede el tamaño máximo permitido, será necesario otro alojamiento o una estrategia de distribución distinta.
- No volver a instalar mientras el juego esté ejecutándose. El instalador de macOS puede solicitar permiso de administrador.
- Las comprobaciones de integridad del instalador no sustituyen los mecanismos antitrampas internos del juego ni la validación en servidor.
- Los derechos de distribución del juego y las licencias de componentes de terceros se gestionan por separado.

## Diagnóstico

Si no aparece una versión nueva, comprueba:
- que el Release esté **publicado** y no marcado como prerelease;
- que la etiqueta tenga formato `vX.Y.Z` y represente una versión superior;
- que el Release contenga el `.pkg` completo;
- que la computadora tenga conexión a Internet y pueda acceder a GitHub.

Si aparece un error de SHA-256, **no fuerces la instalación**: revisa el archivo publicado y vuelve a publicar una versión íntegra y firmada.
