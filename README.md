# Lente DIA · Manuel Belgrano (IA al Colorado)

Al enfocar la lámina impresa con el celular, aparece el video del humano digital de Manuel Belgrano hablando sobre la lámina. Es una **recreación digital educativa**.

## Archivos que tienen que estar en el repositorio

```
index.html              La lente AR (ya incluido)
lamina/belgrano.png     OBLIGATORIO: el PNG de la lámina, con ese nombre exacto
video/belgrano.mp4      Tu video del humano digital hablando (sin él, la lente anda en modo prueba)
targets.mind            OPCIONAL: no hace falta, la página lo arma sola desde el PNG
```

## Cómo se arregla el error "Falta el archivo targets.mind"

Esta versión ya no necesita `targets.mind`. La página arma el marcador sola, en tu celular, a partir de `lamina/belgrano.png`:

1. Subí el PNG de la lámina al repositorio en la carpeta `lamina/` con el nombre `belgrano.png`. En GitHub: Add file > Upload files; para crear la carpeta, al renombrar escribí `lamina/belgrano.png`.
2. Abrí la página y tocá "Activar cámara". La primera vez muestra "Preparando la lámina… %" y tarda hasta un minuto. El resultado se guarda en el celular, así que las próximas veces es inmediato.
3. Si cambiás la lámina, cambiá `version` en `CFG` (por ejemplo a `v2`) para que se vuelva a preparar.

Si preferís generar `targets.mind` con el compilador web de MindAR y subirlo a la raíz, la página lo usa primero y no compila nada.

## La lámina

- Diseño editable en Canva: https://canva.link/ahgwbodp68gfs98
- Los enlaces de descarga de Canva caducan en horas. Si venció, exportá de nuevo desde Canva (Compartir > Descargar > PNG).
- Imprimila en A4, en papel mate y sin recortar los bordes.
- Es una recreación artística generada con IA, no un retrato documentado de Belgrano.

## El video

- Guardalo como `video/belgrano.mp4` (H.264 + AAC), liviano (menos de 20 MB) y corto.
- Sin video, la lente muestra un panel azul sobre la lámina: sirve para comprobar que el marcador se reconoce.
- Para mover o agrandar el video, cambiá `x`, `y` y `ancho` en `CFG` dentro de `index.html`.

## Publicar en GitHub Pages

Settings > Pages > Deploy from a branch > `main` / root. Abrilo desde el celular por https (GitHub Pages ya lo incluye).

## Pendiente

- Proyecto `.son`: falta el ejemplo de la plataforma Lente DIA.
- No hay audio de voz sintética hasta que lo agregues al video.

## Notas

- Carga A-Frame 1.5.0 y MindAR 1.2.5 desde jsDelivr.
- El reconocimiento de la imagen ocurre en el dispositivo; no se envía la cámara a ningún servidor.
