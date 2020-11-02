<template>
  <section class="content-header text-center dein-gratis-testpaket ">
    <div class="info-overlay">
      <h1 class="text-center content-header-headline">Dein gratis Testpaket</h1>
      <a href="" class="button">Wähle Deine Größe</a>
    </div>
  </section>
</template>
<script>
export default {
  name: "MainImage"
};
</script>
<style lang="scss">
$tablet: "834px";
$mobile: "420px";
.content-header {
  display: flex;
  padding-top: 0;
  padding-bottom: 0;
  min-height: 35.25rem;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-color: #f2f0ec;
  .dein-gratis-testpaket {
    background-image: url("../assets/header-trialbox-desktop.jpg");
  }
  .info-overlay {
    align-self: flex-end;
    padding: 2.5rem 1rem 1.5rem 1rem;
    width: 100%;
    background: rgba(255, 255, 255, 0.7);
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
    min-width: 16rem;
    &:hover {
      opacity: 0.6;
    }
  }
}
@media (max-width: $mobile) {
  .dein-gratis-testpaket {
    background-image: url("../assets/header-trialbox-mobile.jpg");
  }
}

@media (max-width: $tablet) {
  .dein-gratis-testpaket {
    background-image: url("../assets/header-trialbox-tablet.jpg");
  }
}
@media (min-width: $tablet) {
  // desktop
  .content-header {
    min-height: 38rem;
    justify-content: flex-end;
    .info-overlay {
      padding: 2.5rem 2.5rem 1.5rem 2.5rem;
      width: 31.25rem;
      margin-right: 4rem;
      align-self: center;
      justify-self: right;
    }
  }
  .dein-gratis-testpaket {
    background-image: url("../assets/header-trialbox-desktop.jpg");
  }
}
</style>
