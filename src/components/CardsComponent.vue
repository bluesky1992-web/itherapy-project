<template>
  <div class="card-grid">
    <div
      v-for="(card, index) in cardData"
      :key="card.id"
      class="card-container"
      :class="{ 'middle-column': isMiddleColumn(index) }"
    >
      <div class="card">
        <p class="role">{{ card.role }}</p>
        <img :src="card.imagePath" :alt="card.name" />
        <h3>{{ card.name }}</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardsComponent',
  props: ['cardData'],
  methods: {
    isMiddleColumn(index) {
      return index === 1 || index === 4  ;
    },
  },
};
</script>

<style>
.middle-column {
 padding-top: 70px;
 
 
}
.card-grid {
  display: flex;
  flex-wrap: wrap;

  margin-left: 15%;
}

.card-container {
  flex: 1 0 calc(30% - 20px); /* Adjust the width of the card container to fit 2 cards per row */
  width: 200px;
  
}

.card {
  /* Add your card styles here */
  width: 300px;
}
img {
  width: 200px;
}
p.role {
  text-transform: uppercase;
  font-size: 12px;
  font-family: Poppins;
}
h3 {
  font-size: 18px;
  font-weight: 600;
  font-family: Poppins;
  margin: 0;
}
.role {
  margin: 0;
  margin-left: 68%;
  /* writing-mode: vertical-rl; */
  transform: rotate(90deg);
  transform-origin: left 18px;
  padding-left: 10px;
  margin-bottom: 10px;
}
</style>
