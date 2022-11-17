<script>
export default {
  name: "CharacterCard",
  props: {
    character: Object,
  },
};
</script>

<template>
  <div class="eb-card">
    {{ character.name }}
  </div>
</template>


<style lang="scss" scoped>
</style>