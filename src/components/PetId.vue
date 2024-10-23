<script setup>
const props = defineProps ({
    name: String,
    species: String,
    age: Number
})
console.log(props.animalInfos);

</script>

<template>

<h2>{{ name }}</h2>
      <p><span>Espèce</span> : {{ species }}</p>
      <p><span>Age</span> : {{ age }}</p>

</template>

<style scoped></style>