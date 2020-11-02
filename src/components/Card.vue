<template>
  <section class="bootstrap columns-wrapper  mb-n1">
    <div class="container">
      <div class="row justify-content-center content-columns">
        <div class="col-12 text-center m-5">
          <h2>Wie es funktioniert</h2>
        </div>
        <div class="column-item col-md col-sm-12 mb-0 text-center ">
          <div style="font-size:50px;">
            <svg
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              class="bi bi-gift"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M3 2.5a2.5 2.5 0 0 1 5 0 2.5 2.5 0 0 1 5 0v.006c0 .07 0 .27-.038.494H15a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1v7.5a1.5 1.5 0 0 1-1.5 1.5h-11A1.5 1.5 0 0 1 1 14.5V7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1h2.038A2.968 2.968 0 0 1 3 2.506V2.5zm1.068.5H7v-.5a1.5 1.5 0 1 0-3 0c0 .085.002.274.045.43a.522.522 0 0 0 .023.07zM9 3h2.932a.56.56 0 0 0 .023-.07c.043-.156.045-.345.045-.43a1.5 1.5 0 0 0-3 0V3zM1 4v2h6V4H1zm8 0v2h6V4H9zm5 3H9v8h4.5a.5.5 0 0 0 .5-.5V7zm-7 8V7H2v7.5a.5.5 0 0 0 .5.5H7z"
              />
            </svg>
          </div>
          <div class="column-content">
            <h3>DEIN TESTPAKET</h3>
            <p class="content-1 mb-0">
              Wir schenken Dir die Produkte, Du übernimmst nur das Porto.
            </p>
          </div>
        </div>
        <div class="column-item col-md col-sm-12 mb-0 text-center ">
          <div style="font-size:50px;">
            <svg
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              class="bi bi-unlock"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M9.655 8H2.333c-.264 0-.398.068-.471.121a.73.73 0 0 0-.224.296 1.626 1.626 0 0 0-.138.59V14c0 .342.076.531.14.635.064.106.151.18.256.237a1.122 1.122 0 0 0 .436.127l.013.001h7.322c.264 0 .398-.068.471-.121a.73.73 0 0 0 .224-.296 1.627 1.627 0 0 0 .138-.59V9c0-.342-.076-.531-.14-.635a.658.658 0 0 0-.255-.237A1.122 1.122 0 0 0 9.655 8zm.012-1H2.333C.5 7 .5 9 .5 9v5c0 2 1.833 2 1.833 2h7.334c1.833 0 1.833-2 1.833-2V9c0-2-1.833-2-1.833-2zM8.5 4a3.5 3.5 0 1 1 7 0v3h-1V4a2.5 2.5 0 0 0-5 0v3h-1V4z"
              />
            </svg>
          </div>
          <div class="column-content">
            <h3>DEINE FLEXIBILITÄT</h3>
            <p class="content-1 mb-0">
              Erste Monatsbox nach 14 Tagen für 49,50 € erhalten. Oder noch vor
              der ersten Lieferung kündigen.
            </p>
            <div class="primary-color extra-text">
              Erfahre hier mehr über das LILLYDOO Windel-Abo.
            </div>
          </div>
        </div>
        <div class="column-item col-md col-sm-12 mb-0 text-center ">
          <div style="font-size:50px;">
            <svg
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              class="bi bi-box-seam"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M8.186 1.113a.5.5 0 0 0-.372 0L1.846 3.5l2.404.961L10.404 2l-2.218-.887zm3.564 1.426L5.596 5 8 5.961 14.154 3.5l-2.404-.961zm3.25 1.7l-6.5 2.6v7.922l6.5-2.6V4.24zM7.5 14.762V6.838L1 4.239v7.923l6.5 2.6zM7.443.184a1.5 1.5 0 0 1 1.114 0l7.129 2.852A.5.5 0 0 1 16 3.5v8.662a1 1 0 0 1-.629.928l-7.185 2.874a.5.5 0 0 1-.372 0L.63 13.09a1 1 0 0 1-.63-.928V3.5a.5.5 0 0 1 .314-.464L7.443.184z"
              />
            </svg>
          </div>

          <div class="column-content">
            <h3>DEINE MONATSBOX</h3>
            <p class="content-1 mb-0">
              Jederzeit Windelgröße, Designs und Lieferintervalle anpassen oder
              weitere Produkte hinzufügen.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Card",
};
</script>
<style lang="scss">
$colorPrimary: #00afab;
.primary-color {
  color: $colorPrimary;
}
section {
  font-family: roboto;
}
.column-content {
  h3 {
    font-size: 16px;
    font-weight: bold;
    margin: 20px;
  }
  .extra-text {
    margin: 20px;
  }
}
</style>
