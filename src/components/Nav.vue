<template>
  <nav class="desktop">
    <div class="desktop__container">
      <router-link to="/" class="desktop__logo">AV</router-link>
      <ul class="desktop__list">
        <li class="desktop__item">
          <router-link to="/" class="desktop__link">
            <svg class="desktop__icon">
              <use href="img/icons.svg#home-icon" />
            </svg>
            Inicio
          </router-link>
        </li>
        <li class="desktop__item">
          <router-link to="/proyectos" class="desktop__link">
            <svg class="desktop__icon">
              <use href="img/icons.svg#portfolio-icon" />
            </svg>
            Proyectos
          </router-link>
        </li>
        <li class="desktop__item">
          <router-link to="/contacto" class="desktop__link">
            <svg class="desktop__icon">
              <use href="img/icons.svg#contact-icon" />
            </svg>
            Contacto
          </router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
export default {
  name: "NavDesktop",
};
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato&family=Philosopher:wght@700&display=swap');
@import "../assets/scss/variables.scss";


.desktop {
  height: 64px;
  width: 100%;
  // position: fixed;
  top: 0;
  z-index: 1;
    // color: white;


  &__container {
    display: flex;
    height: 100%;
    justify-content: center;
    align-items: center;
  }

  &__logo {
    text-decoration: none;
   font-family: 'Philosopher', sans-serif;
    font-size: 40px;
    color:$light;
  z-index: 1;
  }

  &__list {
    z-index: 1;
    position: fixed;
    bottom: 0;
    background-color: rgb(255, 255, 255);
    display: flex;
    width: 100%;
    border-top: 1px solid rgba(0, 0, 0, 0.1);
    list-style: none;
    // height: 64px;
  }

  &__item {
    width: 33.3%;
    // border: 1px solid rgba(0, 0, 0, 0.032);
  }

  &__link {
    display: block;
    text-align: center;
    text-decoration: none;
    color: $dark;
    padding: 4px 0;

  }

  &__link.router-link-exact-active{
      background-color: $primary;
      color:$light;
  }

  &__icon {
    margin: auto;
    display: block;
    width: 24px;
    height: 24px;
    fill: rgba(0, 0, 0, 0.372);
  }

}

@media only screen and (min-width:600px){
.desktop{
   &__container {
    justify-content:space-between;
    padding-left: 20px;
   }

  &__icon {
   display: inline-block;
   margin-right:5px;
    width: 16px;
    height: 16px;
    fill: $light;

  }

   &__list {
    width: auto;
    position: relative;
    display: flex;
    border:none;
     background-color: transparent;
  }

   &__item {
    width: auto;
  }

  
  &__link {
    display: flex;
    align-items: center;
    padding: 22px 20px;
    color: $light;
  }

  &__link.router-link-exact-active{
    background-color: transparent;
    color: $secundary;
    // border-bottom: 2px solid rgb(0, 255, 162);
  }


}
}


</style>