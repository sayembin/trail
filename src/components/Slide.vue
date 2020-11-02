<template>
  <section class="slide-section">
    <div class="row flex-column-reverse flex-md-row">
      <div id="text-under-mobile" class="col  slide_text">
        <p>
          Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere
          Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven
          Feuchttücher zu Größe 4 - 5.
        </p>
        <ul class="product-list">
          <li>Wir zahlen die Produkte, Du nur den Versand.</li>
          <li class="primary-color">
            Automatischer Übergang ins jederzeit kündbare Windel-Abo für
            49,50&nbsp;€ pro Lieferung.
          </li>
          <li>
            Preise inkl. MwSt., ggf. zzgl.
            <a href="#" target="_blank" rel="noreferrer noopener"
              >Versandkosten</a
            >
          </li>
        </ul>
        <button
          id="product-add-to-cart-tracking"
          class="trialbox-order-button button order-button product-form-button my-4"
          data-in-stock-label="In den Warenkorb legen"
          data-out-of-stock-label="Nicht erhältlich"
        >
          <span>In den Warenkorb legen</span>
        </button>
      </div>
      <div class="col">
        <div class=" pt-2 mb-3 pt-md-3 px-3 px-md-4  initialized">
          <ul class="slides">
            <li>
              <div class="image-container">
                <div v-if="oeko" class="stump-image">
                  <img
                    class="image"
                    width="200"
                    height="120"
                    src="../assets/slide/oekotex_green_de.svg"
                    alt=""
                  />
                </div>

                <div class="main_image">
                  <img
                    itemprop="image"
                    :src="require(`@/assets/slide/${image}`)"
                    draggable="false"
                    class="img-fluid"
                  />
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>

      <div class="col">
        <div class="trail-pack-headline">
          Entdecke unsere Hautfreundlichkeit
        </div>
        <div class="tb-list-buttons">
          <div>
            <p class="mb-2 text-uppercase text-left">Wähle Deine Größe</p>
          </div>
          <div class="tb-button-container">
            <ul>
              <li
                v-for="item in slides"
                :key="item.id"
                v-on:click="changeImageLink(item)"
                :class="{ 'flex-active': selected == item.id }"
              >
                <p>{{ item.name }}</p>
                <span>({{ item.spanText }})</span>
              </li>
            </ul>
          </div>
          <div class="col text-under-button slide_text">
            <p class="padding-left-0;">
              Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere
              Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven
              Feuchttücher zu Größe 4 - 5.
            </p>
            <ul class="product-list">
              <li>Wir zahlen die Produkte, Du nur den Versand.</li>
              <li class="primary-color">
                Automatischer Übergang ins jederzeit kündbare Windel-Abo für
                49,50&nbsp;€ pro Lieferung.
              </li>
              <li>
                Preise inkl. MwSt., ggf. zzgl.
                <a href="#" target="_blank" rel="noreferrer noopener"
                  >Versandkosten</a
                >
              </li>
            </ul>
            <button
              id="product-add-to-cart-tracking"
              class="trialbox-order-button button order-button product-form-button my-4"
              data-in-stock-label="In den Warenkorb legen"
              data-out-of-stock-label="Nicht erhältlich"
            >
              <span>In den Warenkorb legen</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <Card />
  <section class="bootstrap columns-wrapper  mb-n1">
    <div class="row justify-content-center ">
      <div class=" col-12 text-center m-5">
        <h2>Dein Testpaket enthält</h2>
      </div>
      <div class="card" v-for="pakItem in paketEnthalts" :key="pakItem.id">
        <div class="row no-gutters">
          <div class="col col-sm-5">
            <img
              class="card-img"
              style="width:100%;max-width:200px;max-height:150px;"
              :src="require(`@/assets/slide/${pakItem.image}`)"
              alt="Card"
            />
          </div>
          <div class="col col-sm-7">
            <div class="card-body">
              <h3 class="card-title">{{ pakItem.title }}</h3>
              <div>
                <Rate :max="5" :current="pakItem.rating"></Rate>({{
                  pakItem.totalRrating
                }})
              </div>
              <ul
                v-for="description in pakItem.description"
                :key="description.item"
              >
                <li>{{ description.item }}</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <Testimonial />
</template>
<script>
import slides from "../data/slide.json";
import Card from "@/components/Card.vue";
import Rate from "@/components/Rate.vue";
import Testimonial from "@/components/Testimonial.vue";

export default {
  name: "Slide",
  components: {
    Card,
    Rate,
    Testimonial,
  },
  data() {
    return {
      image: "lillydoo-testpaket-10.jpg",
      imageAlt: "testpaket-10",
      slides: slides,
      isActive: false,
      selected: 0,
      oeko: true,
      paketEnthalts: slides[0]?.paketEnthalt,
    };
  },
  methods: {
    changeImageLink: function(item) {
      this.image = item.image;
      this.imageAlt = item.imageAlt;
      this.isActive = !this.isActive;
      this.selected = item.id;
      this.oeko = item.oeko;
      this.paketEnthalts = item.paketEnthalt;
    },
    activateClass: function() {},
  },
};
</script>

<style scoped lang="scss">
$mobile: "790px";
.slide-section {
  padding: 10px;
  overflow-x: hidden;
}
ul {
  list-style: none;
  padding: 0px;
}
.tb-button-container {
  margin-bottom: 30px;
  ul {
    display: flex;
    -webkit-justify-content: space-between;
    -ms-flex-pack: justify;
    justify-content: space-between;
    li {
      border: 1px solid #7c7c7c;
      text-align: center;
      width: 30%;
      padding: 7px 5px 2px 5px;
      color: #7c7c7c;
      margin-right: 10px;
      &:hover {
        background-color: #00afab;
        border-color: #00afab;
        color: #fff;
        cursor: pointer;
      }
      :last-child {
        margin-right: 0;
      }
      &.flex-active,
      &.selected {
        background-color: #00afab;
        border-color: #00afab;
        color: #fff;
      }
      p {
        font-size: 1.3rem;
        line-height: 1;
        margin: 0;
      }
      span {
        line-height: 1;
        font-size: 0.8rem;
      }
    }
  }
}

.card {
  border: 0px !important;
  margin: 0px;
  text-align: left;
  .card-body {
    width: 350px;
    ul {
      list-style-type: disc;
    }
  }
  h3 {
    font-size: 16px;
    font-weight: bold;
  }
}
.slide_text {
  margin: 0px;
  padding: 5px;
  widows: 100%;
  text-align: left !important;
  ul {
    list-style: disc !important;
    margin-left: 1.1rem;
  }
  p {
    font-family: Roboto;
    font-weight: 400;
    line-height: 1.4;
    text-rendering: optimizeLegibility;
  }
  .button {
    display: inline-flex;
    justify-content: center;
    height: auto;
    background-color: #00afab;
    color: #fafafa;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 1rem;
    line-height: 1.4375rem;
    font-weight: 500;
    padding: 0.5rem 1.25rem 0.4375rem 1.25rem;
    outline: 0;
    border: 1px solid #00afab;
    transition: 0.3s ease-in-out;
    margin: 0.875rem 0 0.625rem 0;
    appearance: none;
    position: relative;
    width: 100%;
    &:hover {
      opacity: 0.6;
    }
  }
}
.trail-pack-headline {
  font-family: roboto;
  font-size: 1.6rem;
  line-height: 1.2;
  text-transform: none;
  margin-bottom: 10px;
  text-align: left;
}
p {
  font-size: 0.938rem;
}
.image-container {
  position: relative;
}
.stump-image {
  position: absolute;
  top: 0;
  left: 0;
}
.main-image {
  position: absolute;
  top: 0;
  left: 0;
}

#text-under-mobile {
  display: none !important;
}
.text-under-button {
  display: block;
}
@media (max-width: $mobile) {
  .text-under-button {
    display: none;
  }
  #text-under-mobile {
    display: block !important;
  }
}
</style>
