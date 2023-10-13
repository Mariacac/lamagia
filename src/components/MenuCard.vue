<script setup>
const props = defineProps({
  product: {
    type: Object,
  },
});
</script>
<template>
  <div class="card" :class="`${product.available ? '' : 'false'}`">
    <h2 class="food--title">{{ product.product }}</h2>

    <img :src="product.image_url" class="food-img" />

    <p class="description">
      {{ product.description }}
    </p>

    <p class="price-number">$14</p>
    <img src="img/star.png" class="price-img" />
  </div>
</template>

<style scoped>
.false {
  filter: grayscale(100%);
}
.card {
  display: grid;
  background-color: var(--white-vintage);
  width: 250px;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 1fr);
  border-radius: 5%;
  align-items: center;
  justify-items: center;
  text-align: center;
}
.food--title {
  color: var(--red-vintage);
  font-family: Yusei Magic;
  font-size: 30px;
  grid-column: 1/3;
}
.food-img {
  width: 120px;
  height: 120px;
  grid-column: 1/3;

  border-radius: 99px;
}

.description {
  color: var(--yellow-vintage);
  font-family: josefin sans;
  font-size: 18px;
  grid-column: 1/1;
  grid-row: 3/3;
}

.price-number {
  display: flex;
  /*position: relative;*/
  color: var(--white-vintage);
  font-size: 30px;
  font-family: Yusei magic;
  grid-column: 2/2;
  grid-row: 3/3;
  z-index: 2;
}
.price-img {
  grid-column: 2/2;
  grid-row: 3/3;
}
img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
</style>
