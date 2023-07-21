<template>
  <div>
    <div v-for="card in cardData" :key="card.id" class="card">
      <p class="role">{{ card.role }}</p>
      <img :src="card.imagePath" :alt="card.name" />
      <h3>{{ card.name }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardsComponent',
  props: ['cardData']
}
</script>

<style>
.card > img {
  width: 230px;
}
p.role {
  text-transform: uppercase;
  font-size: 12px;
  font-family: Poppins;
}
.card h3 {
  font-size: 18px;
  font-weight: 600;
  font-family: Poppins;
}
.role {
  margin: 0;
  margin-left: 18%;
 transform-origin: left;
 transform: rotate(90deg);
}
</style>
