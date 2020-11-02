<template>
  <section class="dark ">
    <div class="row justify-content-center">
      <div class="small-12 columns text-center m-5">
        <h2>Was andere über unser Windel-Abo&nbsp;sagen</h2>
      </div>
    </div>
    <div class="row">
      <div class="small-12 medium-8 medium-centered column testimonials">
        <div
          class="testimonial-item"
          v-for="item in testimonials"
          :key="item.item"
        >
          <div class="testimonial-img">
            <img :src="require(`@/assets/testimonials/${item.item}`)" />
          </div>
          <div class="testimonial-content">
            <blockquote>
              <p>"{{ item.text }}"</p>
              <p class="quote-author">
                {{ item.name }} -
                <a
                  href="{{item.link}}"
                  target="_blank"
                  rel="noreferrer noopener"
                  >{{ item.title }}</a
                >
              </p>
            </blockquote>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section>
    <div class="magazine-discover small-12 text-center">
      <h3>Überzeug Dich selbst</h3>
      <div class="button-wrapper">
        <a href="/de/newsletter/anmeldung-momlife" class="button"
          >JETZT GRATIS TESTEN
        </a>
      </div>
    </div>
    <div class="row">
      <img src="../assets/blow_pic.png" class="img-fluid" alt="Blow  image" />
    </div>
  </section>
</template>
<script>
export default {
  name: "Testimonial",
  data() {
    return {
      testimonials: [
        {
          name: "Jessica Kroos",
          item: "kroos.png",
          title: "Vorstandsmitglied Toni Kroos Stiftung",
          link: "#",
          text:
            "Wir lieben das Design der LILLYDOO Windeln und noch dazu sind sie besonders hautfreundlich, deswegen nehme ich nur diese für unsere Kids. Das Abo ist super praktisch, denn die Windeln werden direkt nach Hause geliefert! Besser geht es nicht!",
        },
        {
          name: "Johanna Klum",
          item: "klum.png",
          title: "Moderatorin",
          link: "#",
          text:
            "Auch bei meinem 2. Baby nehme ich nur LILLYDOO Windeln! Ich liebe die Qualität und das schöne Design – und nicht auch noch Windeln schleppen zu müssen, wenn man zwei kleine Kids hat und voll arbeitet, ist wirklich einfach toll!",
        },
        {
          name: "Laura Niemeyer",
          item: "niemeyer.png",
          title: "trendshock",
          link: "#",
          text:
            "LILLYDOO begleitet uns nun seit mehr als drei Jahren voller Begeisterung. Die Windeln und Pflegeprodukte sind wie auf uns zugeschnitten – besonders hautfreundlich, hohe Qualität und modernes Design. Wir fühlen uns mit den Produkten angekommen und werden sie auch noch lange nutzen.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
h3 {
  color: #000;
}
img {
  width: 100%;
}
.dark {
  background: #f8f8f8;
  color: #000;
  font-family: roboto;
  .row {
    .column {
      position: relative;
      padding-left: 100px;
      padding-right: 100px;
      float: left;
    }
    margin: 0 auto;
    width: 100%;
    .testimonials {
      float: none;
      .testimonial-item {
        display: flex;
        align-items: center;
        margin-bottom: 50px;
        .testimonial-img {
          width: 18%;
          margin-right: 45px;
        }
        .testimonial-content {
          width: 80%;
          text-align: left;
          p {
            font-size: 15px;
          }
        }
      }
    }
  }
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
  max-width: 300px;
  &:hover {
    opacity: 0.6;
  }
}
</style>
