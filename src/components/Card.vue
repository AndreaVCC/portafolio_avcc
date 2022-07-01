<template>
  <div class="cards">
    <div class="card" v-for="(item, id) in dataprops" :key="id">
      <div class="card__image-container">
        <img :src="item.img" :alt="item.title"/>
      </div>
      <div class="card__content">
        <p class="card__title">{{ item.title }}</p>
        <p class="card__description">
          {{ item.description }}
        </p>
        <div class="card__tecno">
          <span
            class="card__price"
            v-for="(item, id) in item.tools"
            :key="id"
            >{{ item }}</span
          >
        </div>
        <div class="card__info">
    
          <a class="card__links" target="_blank" :href="item.deploy">  <svg class="card__icon">
            <use href="img/icons.svg#ver-icon" />
          </svg>Visualizar</a>
          <a class="card__links" target="_blank" :href="item.github">  <svg class="card__icon">
            <use href="img/icons.svg#github-icon" />
          </svg>Github</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    dataprops: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.cards {
  display: grid;
  justify-content: center;
  grid-column: 2 / span 6;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 25px;
}

.card {
  grid-column-end: span 6;
  border-radius: 5rem 0 5rem 0;
  display: flex;
  flex-direction: column;
  // background-color:rgba(141, 140, 142, 0.394);
  cursor: pointer;
  transition: all 0.3s ease 0s;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.card__links {
  display: flex;
  align-items: center;
  margin-right: 1.8rem;
  color: $dark;
  text-decoration: none;
}

.card__icon {
  height: 2.4rem;
  width: 2.4rem;
  margin-right: 0.5rem;
}

.card:hover {
  transform: translateY(-7px);
}

.card__image-container {
  width: 100%;
  padding-top: 56.25%;
  overflow: hidden;
  position: relative;
   border-radius: 5rem 0 5rem 0;
}

.card__image-container img {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.card__content {
  padding: 20px;
}

.card__title {
  margin-bottom: 2rem;
}
.card__description {
  margin-bottom: 1rem;
}

.card__info {
  display: flex;
  align-self: end;
  align-items: center;
}

.card__tecno {
  margin-bottom: 2rem;
  display: flex;
  flex-wrap: wrap;
}
.card__price {
  font-size: 1rem;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  padding: 0 0.5rem;
  color: $light;
  background-color: $primary;
  border-radius: 20px;
}

@media only screen and (min-width: 500px) {
  .card {
    grid-column-end: span 6;
  }
  .cards {
    display: grid;
    grid-template-columns: repeat(12, minmax(auto, 60px));
    grid-gap: 40px;
  }
}

@media only screen and (min-width: 1024px) {
  .card {
    grid-column-end: span 4;
  }
  .cards {
    grid-gap: 40px;
  }
}
</style>