# Zone Brazil — actualizaciones para macOS

Repositorio de distribución de versiones de **Zone Brazil para Mac**.

## Cómo reciben las actualizaciones los jugadores

El lanzador **Zona Brazil 4.5** consulta la última publicación estable de GitHub Releases:

`https://api.github.com/repos/MRDIABLOYT669/ZonaBrazil-Updates/releases/latest`

Si aparece una versión superior a la instalada, el lanzador ofrece descargar un **único instalador .pkg**, comprueba el SHA-256 publicado por GitHub y abre el instalador de macOS. **No realiza instalaciones silenciosas** ni sustituye el juego mientras está abierto.

## Cómo publicar

Consulta [GUIA_PUBLICAR_VERSIONES.md](GUIA_PUBLICAR_VERSIONES.md). Para empezar, prepara y prueba el instalador completo de la versión `1.3.9`, crea un Release con etiqueta `v1.3.9` y adjunta el `.pkg`. Las siguientes versiones usarán etiquetas `v1.4.0`, `v1.4.1`, etc.

> **Estado:** crear este repositorio no publica automáticamente ningún juego. Para que el actualizador funcione se necesita al menos un Release con el instalador completo y el cliente 4.5 instalado.

## Seguridad y compatibilidad

- No publicar credenciales, sesiones del juego ni datos personales procedentes de la instalación de desarrollo.
- Conservar las licencias de los componentes de terceros, independientes de los créditos oficiales del juego.
- Para distribución profesional, firmar y notarizar instalador y aplicación con Apple Developer ID; la comprobación SHA-256 por sí sola no sustituye la firma.
- El motor del juego funciona sobre una base x86_64 de compatibilidad; la ejecución en Apple Silicon todavía requiere pruebas reales.
- El repositorio es público: no subir el código privado ni archivos que no se quieran distribuir.

© Los derechos del juego original pertenecen a sus respectivos titulares.
