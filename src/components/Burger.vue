<template>
  <header>
    <nav class="navbar navbar-light navbar-expand-lg py-3 px-4">
      <button
        class="navbar-toggler collapsed"
        type="button"
        data-toggle="collapse"
        data-target="#navbarCollapse"
        aria-controls="navbarCollapse"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span v-for="(n, index) in bar" :key="index"></span>
      </button>
      <a href="#" class="navbar-brand">
        LILLYDOO
      </a>
      <button class="navbar-toggler collapsed" type="button">
        <svg
          width="1em"
          height="1em"
          viewBox="0 0 16 16"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm7 0a1 1 0 1 0 0 2 1 1 0 0 0 0-2z"
          />
        </svg>
      </button>
      <div class="collapse navbar-collapse" id="navbarCollapse">
        <ul class="navbar-nav ml-auto text-left">
          <li
            v-for="item in menus"
            :key="item.item"
            data-toggle="collapse"
            data-target=".navbar-collapse.show"
          >
            <a :href="item.link" class="nav-link text-uppercase">
              {{ item.item }}
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      bar: 3,
      menus: [
        {
          item: "Gratis Tespaket",
          link: "#",
        },
        {
          item: "Flexibles Abo",
          link: "#",
        },
        {
          item: "Produkte",
          link: "#",
        },
        {
          item: "Magazin",
          link: "#",
        },
        {
          item: "Über LILLYDOO",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
header {
  a {
    color: white;
  }
  .navbar-light {
    background: #fff;
    a {
      color: #000; //overwrite bootstrap default brand
      font-size: 0.9rem;
      &:hover {
        color: #00afab !important;
      }
      &.navbar-brand {
        font-size: 30px;
        &:hover {
          color: #000 !important;
        }
      }
    }
  }
  .dropdown:hover > .dropdown-menu {
    display: block;
  }
  .dropdown > .dropdown-toggle:active {
    pointer-events: none;
  }
  .navbar-nav {
    padding-top: 1rem;
    @media (min-width: 875px) {
      padding-top: 0;
    }
  }
  .navbar-toggler:focus,
  .navbar-toggler:active {
    outline: 0;
  }
  .navbar-toggler {
    height: 40px;
    border: 0px;
  }
  .nav-link {
    @media (min-width: 875px) {
      border-top: 0px;
      line-height: 3;
    }
    height: 55px;
    line-height: 3;
    font-size: 16px;
    text-align: left;
    position: relative;
    border-top: 1px solid rgba(0, 0, 0, 0.1);
    padding-left: 20px;
  }

  .navbar-toggler span {
    display: block;
    background-color: #000;
    height: 2px;
    width: 25px;
    margin-top: 6px;
    margin-bottom: 4px;
    -webkit-transform: rotate(0deg);
    -moz-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
    position: relative;
    opacity: 1;
  }
  .navbar-toggler span:nth-child(1),
  .navbar-toggler span:nth-child(3) {
    -webkit-transition: transform 0.35s ease-in-out;
    -moz-transition: transform 0.35s ease-in-out;
    -o-transition: transform 0.35s ease-in-out;
    transition: transform 0.35s ease-in-out;
  }
  .navbar-toggler:not(.collapsed) span:nth-child(1) {
    position: absolute;
    top: 32px;
    -webkit-transform: rotate(-135deg);
    -moz-transform: rotate(-135deg);
    -o-transform: rotate(-135deg);
    transform: rotate(-135deg);
    opacity: 0.9;
  }
  .navbar-toggler:not(.collapsed) span:nth-child(2) {
    visibility: hidden;
    background-color: transparent;
  }
  .navbar-toggler:not(.collapsed) span:nth-child(3) {
    position: absolute;
    top: 32px;
    -webkit-transform: rotate(135deg);
    -moz-transform: rotate(135deg);
    -o-transform: rotate(135deg);
    transform: rotate(135deg);
    opacity: 0.9;
  }
}
</style>
