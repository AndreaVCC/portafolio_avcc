<template>
    <div class="inicio">
      <div class="inicio__seccion inicio__seccion-nombre">
        <h1>Andrea Carreño</h1>
        <p>FRONT-END DEVELOPER</p>
      </div>
      <div class="inicio__seccion inicio__seccion-descripcion">
        <p>
          Constantemente aprendiendo de nuevas herramientas y tecnologias para
          enfrentar nuevos desafíos. <br />
          Siempre busco desarrollar mi creatividad y conocimientos en nuevos
          proyectos que generen cambios positivos y mejoren la experiencia e
          interacción de las personas.
        </p>
        <p>
          Herramientas utilizadas en mis proyectos: Javascript, HTML5, CSS3,
          Vue, React, Bootstrap, SASS, WordPress.
        </p>
        <router-link class="inicio__links" to="/proyectos">
          <svg class="inicio__icon">
            <use href="../assets/img/icons.svg#go-icon" /></svg
          >Conoce mis proyectos</router-link
        >
      </div>
    </div>


  <!-- <svg class="icon-circle">
          <use href="../assets/img/icons.svg#circle-icon" />
      </svg> -->
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";



.inicio {
  width: 100%;
  display: flex;
  flex-direction: column;

  &__links {
    color: $secundary;
    display: flex;
    align-items: center;
  }

  &__icon {
    fill: $secundary;
    height: 1.6rem;
    width: 1.6rem;
    margin-right: 0.5rem;
  }

  &__seccion {
    

    &-nombre {
      margin-top: 9rem;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    &-descripcion {
      margin: 4rem 1rem;
      background-color: $primary;
      color: $light;
      padding: 2rem 2rem 2rem 3.2rem;
      border-radius: 5rem 0 5rem 0;
box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    }
  }
}

@media only screen and (min-width: 768px) {
  .inicio {
    flex-direction: row;
    &__seccion {
      margin-top: 200px;
      &-nombre {
        width: 50%;
      }
      &-descripcion {
        width: 50%;
      }
    }
  }
}

@media only screen and (min-width: 1024px) {
  .inicio {
    margin-top: 120px;

    &__seccion {
      &-nombre {
        width: 60%;
      }
      &-descripcion {
        width: 40%;
      }
    }
  }
}
</style>
