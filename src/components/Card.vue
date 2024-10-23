<script setup>
import PetId from './PetId.vue'

// Déclaration de la props qui contient les informations d'un animal
const props = defineProps({
  animalInfos: Object
})
</script>

<template>
  <div class="card">
    <div>
      <PetId :name="animalInfos.name" :species="animalInfos.species" :age="animalInfos.age" />
    </div>

    <p class="description">{{ animalInfos.description }}</p>
  </div>
</template>

<style scoped>
.card {
  background-color: rgb(244, 246, 247);
  padding: 15px;
  border-radius: 5px;
  width: calc((100% - 15px) / 2);
  display: flex;
  flex-direction: row;
  gap: 10px;
  box-shadow: 0px 0px 7px rgb(114, 114, 193);
}
div {
  width: 150px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.description {
  flex: 1;
}
span {
  text-decoration: none;
  color: gray;
}
.card p {
  color: rgb(9, 77, 101);
}

.card > div {
  display: flex;
  gap: 10px;
}
</style>
