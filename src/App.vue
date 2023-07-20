<template>
  <div class="header">
    <h2>The creative crew</h2>
    <div class="right">
      <h3>Who we are</h3>
      <p>
        We are team of creatively diverse. driven. innovative individuals working in various
        locations from the world.
      </p>
    </div>
  </div>
  <CardsComponent />
</template>

<script>
import CardsComponent from './components/CardsComponent.vue'
export default {
  name: 'App',
  components: {
    CardsComponent
  },
  data () {
     return {
      cards : [
        
      ]
     }
  }
}
</script>

<style scoped>
.header {
  text-align: center;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}
.header > h2 {
  font-size: 32px;
}
.right {
  text-align: left;
  margin-top: 15px;
}
.right > h3 {
  font-size: 18px;
  font-family: Poppins;
  font-weight: 600;
}

p {
  width: 420px;
  text-align: left;
  font-size: 18px;
  margin-top: -7px;
  font-family: Poppins, sans-serif, serif;
}

@media only screen and (max-width: 480px) {
  /* Styles for mobile devices */
  p {
    font-size: 14px;
    width: 320px;
  }
  .header > h2 {
    margin-left: -20%;
  }
}
</style>
