<template>
  <nav class="nav-mobile">
    <p>soy el nav de mobile</p>
  </nav>
</template>
<script>
export default {
  name: 'NavMobile'
}
</script>
<style lang="scss">
  

  @media screen and (min-width: 600px) {
.nav-mobile{
display:none;
}
}
</style>