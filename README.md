[<img src="https://novatorem-two-woad.vercel.app/api/spotify" alt="codeSTACKr Spotify Playing" width="350" />](https://open.spotify.com/user/qwertyuiop1234567890-4)

npm install blueimp-gallery

<link rel="stylesheet" href="css/blueimp-gallery.min.css" />

<!-- The Gallery as lightbox dialog, should be a document body child element -->
<div
  id="blueimp-gallery"
  class="blueimp-gallery"
  aria-label="image gallery"
  aria-modal="true"
  role="dialog"
>
  <div class="slides" aria-live="polite"></div>
  <h3 class="title"></h3>
  <a
    class="prev"
    aria-controls="blueimp-gallery"
    aria-label="previous slide"
    aria-keyshortcuts="ArrowLeft"
  ></a>
  <a
    class="next"
    aria-controls="blueimp-gallery"
    aria-label="next slide"
    aria-keyshortcuts="ArrowRight"
  ></a>
  <a
    class="close"
    aria-controls="blueimp-gallery"
    aria-label="close"
    aria-keyshortcuts="Escape"
  ></a>
  <a
    class="play-pause"
    aria-controls="blueimp-gallery"
    aria-label="play slideshow"
    aria-keyshortcuts="Space"
    aria-pressed="false"
    role="button"
  ></a>
  <ol class="indicator"></ol>
</div>

<div
  id="blueimp-gallery"
  class="blueimp-gallery blueimp-gallery-controls"
  aria-label="image gallery"
  aria-modal="true"
  role="dialog"
>
</div>

<div
  id="blueimp-gallery"
  class="blueimp-gallery blueimp-gallery-contain"
  aria-label="image gallery"
  aria-modal="true"
  role="dialog"
>
</div>

<div id="links">
  <a>
    <img src="IMG_4613.jpg"/>
  </a>
  <a>
    <img src="IMG_4615"/>
  </a>
</div>

<script src="js/blueimp-gallery.min.js"></script>

<script>
  document.getElementById('links').onclick = function (event) {
    event = event || window.event
    var target = event.target || event.srcElement
    var link = target.src ? target.parentNode : target
    var options = { index: link, event: event }
    var links = this.getElementsByTagName('a')
    blueimp.Gallery(links, options)
  }
</script>
