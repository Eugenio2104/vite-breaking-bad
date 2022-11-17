<script>
export default {
  name: "CharacterCard",
  props: {
    character: Object,
  },
};
</script>

<template>
  <!-- name, category, status -->
  <div class="card col-2 text-center">
    <img :src="character.img" :alt="character.name" />
    <h6>{{ character.name }}</h6>
    <p>{{ character.category }}</p>
    <p>{{ character.status }}</p>
  </div>
</template>


<style lang="scss" scoped>
</style>