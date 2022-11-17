<script>
export default {
  name: "AppHeader",
  props: {
    title: String,
  },
};
</script>

<template>
  <div class="container-header py-3">
    <h1>{{ title }}</h1>
  </div>
</template>


<style lang="scss" scoped>
h1 {
  font-weight: 600;
}
</style>