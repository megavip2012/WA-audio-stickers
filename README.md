<p align="center"><img src="extension/icons/icono-128.png" width="96" alt=""></p>

<h1 align="center">Stickers con sonido</h1>

<p align="center">Convierte un video, una imagen o un GIF en un <b>sticker con sonido</b> y envíalo desde <b>WhatsApp Web</b>.<br>Todo se procesa en tu navegador: nada se sube a otro servidor que no sea WhatsApp.</p>

<p align="center"><a href="https://github.com/Shirtep/WA-audio-stickers/releases/latest/download/stickers-con-sonido.zip"><img src="docs/img/boton-descargar.png" width="352" alt="Descargar gratis (ZIP para Chrome, Edge o Brave)"></a></p>

<p align="center"><a href="#instalación"><img src="docs/img/boton-guia.png" width="282" alt="Guía de instalación"></a></p>

> **Aviso:** proyecto personal, **no oficial**, sin relación con WhatsApp ni con Meta. Usa funciones internas de WhatsApp Web que pueden cambiar en cualquier momento, y activa en tu navegador la función de stickers con sonido, que WhatsApp está probando. Úsalo bajo tu propia responsabilidad.

## Instalación

No hay que ejecutar ningún programa: se carga la carpeta de la extensión en el navegador (Chrome, Edge o Brave de escritorio). **No funciona en Firefox** ni en navegadores basados en él (ver [Requisitos](#requisitos)).

1. Descarga el [**ZIP de la última versión**](https://github.com/Shirtep/WA-audio-stickers/releases/latest/download/stickers-con-sonido.zip) (también está en la página de [versiones](https://github.com/Shirtep/WA-audio-stickers/releases/latest)).
2. Descomprímelo en un lugar donde se vaya a quedar, por ejemplo `Documentos`. Obtendrás una carpeta `stickers-con-sonido`.
   **No la borres ni la muevas después:** el navegador carga la extensión desde ahí.
3. Abre la página de extensiones: escribe `chrome://extensions` en la barra de direcciones (en Edge, `edge://extensions`).
4. Activa **Modo de desarrollador** (arriba a la derecha):

   <img src="docs/img/paso1-modo-desarrollador.png" alt="Interruptor Modo de desarrollador activado" width="230">

5. Pulsa **Cargar extensión sin empaquetar** (en algunas versiones se llama *Cargar descomprimida*):

   <img src="docs/img/paso2-cargar-sin-empaquetar.png" alt="Botón Cargar extensión sin empaquetar" width="420">

6. Elige la carpeta `stickers-con-sonido` del paso 2 y pulsa **Seleccionar carpeta**. Aparecerá la extensión:

   <img src="docs/img/paso3-extension-instalada.png" alt="Tarjeta de la extensión Stickers con sonido" width="380">

7. Pulsa el icono del rompecabezas de la barra del navegador y fija **Stickers con sonido** con la chincheta, para tener a mano su icono violeta.

Las capturas son de Brave. En Chrome y Edge se ve igual, con otros colores.

**Idioma:** escolha um idioma no seletor do painel. A interface é atualizada imediatamente, sem recarregar o WhatsApp Web, e a preferência fica salva.

**Atualizar:** baixe o ZIP da nova versão e substitua o conteúdo da pasta `stickers-con-sonido`. Depois clique em recarregar (↻) na página de extensões. Seus ajustes são preservados.

**Desinstalar:** pulsa **Quitar** en la página de extensiones y borra la carpeta.

## Uso

1. Abre [web.whatsapp.com](https://web.whatsapp.com) y entra al chat donde quieres enviar el sticker.
2. Pulsa el icono violeta de la extensión. El panel tiene tres pestañas, cada una con su formulario:
   - **Video:** un video con su propio sonido (los pasos de abajo).
   - **Imagen + audio:** una imagen fija con el sonido que elijas (MP3, M4A, OGG, WAV o el sonido de un video). Recortas el audio con asas sobre su forma de onda y el sticker dura lo que dure ese tramo.
   - **Video o GIF + audio:** una animación (un video sin su sonido, o un GIF) con otro audio. Si duran distinto, por defecto cada uno dura lo suyo: al tocar el sticker empiezan juntos y terminan por separado. También puedes repetir la animación o dejar quieto su último cuadro hasta que acabe el audio. Cambiar el tramo de audio no obliga a recalcular las opciones.

   En la pestaña **Video** hay cuatro pasos:
   1. **Video:** elige un video con sonido.
   2. **Tramo:** arrastra las asas verdes para marcar el inicio y el fin. El video muestra el cuadro exacto, y **−/+** mueven un cuadro.
   3. **Formato:** pulsa **Calcular opciones**. Aparece una tabla de resolución × fps con el peso estimado de cada combinación:
      - verde: cabe;
      - amarillo: cabe bajando la calidad;
      - ✕: no cabe;
      - ★: la recomendada.
   4. **Crear y enviar:** opcionalmente escribe el **paquete** y el **autor** (WhatsApp los muestra bajo el sticker), crea el sticker, revisa la vista previa y envíalo.
3. Desde el celular puedes marcarlo como favorito para volver a usarlo.

## Límites

| | Límite | Motivo |
|---|---|---|
| Peso del sticker | **1 MB** | El servidor de WhatsApp rechaza archivos más grandes (error 413). |
| Peso del audio | 1 MB (≈ 10 min) | Límite de WhatsApp Web para el audio del sticker. |
| Resolución | 64 a 512 px | WhatsApp usa 512 px. Más grande no se ve mejor y pesa más. |
| Fluidez | hasta 30 fps | WhatsApp solo exige que cada cuadro dure al menos 8 ms. |

Cuanto más largo es el tramo, menos resolución o fps caben en 1 MB: la tabla del paso 3 muestra qué cabe antes de crear nada.

Quien recibe el sticker necesita una versión de WhatsApp que ya reproduzca stickers con sonido. Si no la tiene, en lugar del sticker verá el aviso *«Recibiste un mensaje que no es compatible con tu versión de WhatsApp»* y tendrá que actualizar WhatsApp para verlo.

## Privacidad

- La conversión del video ocurre en tu navegador.
- La extensión guarda un **registro de diagnóstico** solo en tu navegador, con los números de teléfono ocultos y sin claves. Puedes verlo, descargarlo o borrarlo desde *Herramientas de prueba* en el panel, o con clic derecho en el icono → *Opciones*.

## Requisitos

- Chrome, Edge o Brave de escritorio, actualizado (usa WebCodecs para codificar el audio). Otros navegadores basados en Chromium, como Opera o Vivaldi, probablemente funcionen, pero no están probados.
- Una cuenta de WhatsApp abierta en WhatsApp Web.

**No funciona en Firefox** ni en los navegadores basados en él (LibreWolf, Waterfox, Floorp, Zen, Tor Browser…): usan otro sistema de extensiones y no pueden cargarla. Tampoco funciona en Safari ni en navegadores de celular.

## ¿No te funciona?

Revisa esto antes de reportarlo; resuelve la mayoría de los casos:

1. **Al cargarla, el navegador dice que falta el manifiesto (`manifest.json`):** elegiste la carpeta equivocada. Algunos descompresores crean una carpeta dentro de otra: elige la que contiene directamente `manifest.json`.
2. **La extensión aparece con error o desapareció:** moviste o borraste la carpeta después de instalarla. Vuelve a ponerla donde estaba, o quítala y cárgala de nuevo.
3. **Pulsas el icono y no pasa nada:** recarga la pestaña de WhatsApp Web (F5). Las pestañas abiertas antes de instalar o actualizar la extensión no la tienen.
4. **El navegador está desactualizado:** actualízalo (en Chrome: menú ⋮ → Ayuda → Información de Google Chrome) y vuelve a probar.
5. **Quien lo recibe ve «Recibiste un mensaje que no es compatible con tu versión de WhatsApp»:** el sticker se envió bien, pero su WhatsApp todavía no reproduce stickers con sonido. Tiene que actualizar WhatsApp desde la tienda de su celular. No es un problema de la extensión.
6. **Tienes una versión antigua de la extensión:** [descarga la última](https://github.com/Shirtep/WA-audio-stickers/releases/latest/download/stickers-con-sonido.zip) y actualiza (ver *Actualizar* en la instalación).

Si nada de esto lo resuelve, puede ser que tu WhatsApp Web sea distinto: WhatsApp no le da a todos la misma versión al mismo tiempo, y la extensión usa partes internas que pueden cambiar. En ese caso, repórtalo como se explica abajo, con el registro de diagnóstico.

## Reportar un problema o sugerir algo

Los reportes y sugerencias se reciben en [**Issues**](https://github.com/Shirtep/WA-audio-stickers/issues/new/choose). Necesitas una cuenta de GitHub (es gratis). Pulsa **New issue** y elige:

- **Problema:** algo falla al instalarla o al usarla.
- **Sugerencia:** una idea o mejora.

Antes, busca en los [issues existentes](https://github.com/Shirtep/WA-audio-stickers/issues?q=is%3Aissue) por si alguien ya lo reportó: si es así, comenta ahí en vez de abrir otro.

Para un **problema**, incluye:

- Tu navegador y su versión, y tu sistema (Windows, macOS, Linux).
- La versión de la extensión (aparece arriba del panel).
- Qué hiciste, qué esperabas y qué pasó. Una captura ayuda mucho; tapa los chats y números que aparezcan.
- **El registro de diagnóstico**, si el problema es al usarla:
  1. Abre el panel, despliega **Herramientas de prueba** al final y pulsa **Diagnóstico**.
  2. Repite lo que falló.
  3. Pulsa **Guardar registro…** y adjunta el archivo `.json` al issue (arrástralo al cuadro de texto). Si GitHub no lo acepta, comprímelo en un ZIP.

  El registro oculta los números de teléfono y no incluye mensajes ni claves, pero sí los nombres de los archivos que elegiste y el nombre del chat al que enviaste el sticker. Ábrelo con un editor de texto y borra o cambia lo que no quieras compartir antes de adjuntarlo.

Si el problema es al instalarla, no hace falta el registro: basta con una captura del mensaje de error de la página de extensiones.

## Para desarrolladores

- [`docs/como-funciona.md`](docs/como-funciona.md): cómo se arma un sticker con sonido (protobuf, formato del audio, límites) y cómo trabaja la extensión.
- [`dev/`](dev/): páginas para probar la conversión sin WhatsApp y el video de calibración de sincronía.

## Licencia

Uso libre y gratuito, **sin fines comerciales**: puedes usarla, estudiarla, modificarla y compartirla, pero no venderla ni usarla para lucrar. Texto completo en [`LICENSE.md`](LICENSE.md) ([PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0)). Se ofrece tal cual, sin garantías.
