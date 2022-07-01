<template>
  <div class="proyectos">
    <div class="proyectos__seccion proyectos__seccion-titulo">
      <h1>Proyectos</h1>
    </div>
    <div class="proyectos__seccion proyectos__seccion-proyectos">
          <Card :dataprops='proyects'/>
    </div>
  </div>
</template>

<script>
import Card from "../components/Card.vue"
export default {
  name: "ProyectosView",
  components: {
    Card,
  },
   data() {
    return {
      proyects: [],
    };
  },
   created() {
    fetch("data.json")
      .then((data) => data.json())
      .then((data) => {
        this.proyects = data;
        console.log(this.proyects);
      });
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.proyectos {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  &__seccion {
    &-titulo {
      margin-top: 9rem;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    &-proyectos {
      margin-bottom: 2rem;
      display: grid;
      grid-gap: 10px;
      grid-template-columns: 10px repeat(6, 1fr) 10px;
      padding: 60px 0;
    }
  }
}




@media only screen and (min-width: 500px) {
  .proyectos__seccion-proyectos {
    grid-gap: 20px;
  }


}

@media only screen and (min-width: 1024px) {
  .proyectos__seccion-proyectos {
    grid-gap: 100px;
  }



}
</style>
