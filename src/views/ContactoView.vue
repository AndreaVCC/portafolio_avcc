<template>
  <div class="contacto">
      <div class="contacto__seccion contacto__seccion-titulo">
          <h1>Contacto</h1>
      </div>
        <div class="contacto__seccion contacto__seccion-contacto">
        <p>Gracias por visitar mi sitio, ¡Conectemonos!</p>
        <p>
        <svg class="contacto__icon">
  <use href="../assets/img/icons.svg#contact-icon" />
        </svg>
        </p>
        <p>  <svg class="contacto__icon">
          <use href="../assets/img/icons.svg#github-icon" />
        </svg></p>
       
      </div>
    </div>

</template>

<script>
export default {
  name: 'ContactoView',
  components: {
  }
}
</script>
<style lang="scss">
  @import "../assets/scss/variables.scss";

.contacto {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.contacto__icon{
  fill: $primary;
  width:4.0rem;
  height:4.0rem;
}

.contacto {
  width: 100%;
  display: flex;
  flex-wrap: wrap;

  &__seccion {
    margin-top: 120px;
    &-titulo {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    &-contacto {
      margin-top: 80px;
      padding: 20px;
      margin-bottom: 20px;
    }
  }
}

@media only screen and (min-width: 768px) {
  .contacto {
    flex-direction: row;
    &__seccion {
      margin-top: 200px;
      &-titulo {
        width: 50%;
      }
      &-contacto {
        width: 50%;
      }
    }
  }
}


@media only screen and (min-width: 1024px) {
  .contacto {
    margin-top: 120px;

    &__seccion {
      &-titulo {
        width: 60%;
      }
      &-contacto {
        width: 40%;
      }
    }
  }
}
</style>
