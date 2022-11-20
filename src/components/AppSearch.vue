<script>
import { store } from "../data/store";

export default {
  name: "AppSearch",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container">
    <select
      @change="$emit('startSearch')"
      v-model="store.categoryToSearch"
      class="form-select"
    >
      <option value="" selected>Select category</option>
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>
  </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/vars" as *;

.container {
  background-color: $primary-color;
  margin: 0 auto;
  select {
    width: 200px;
    margin-bottom: 30px;
  }
}
</style>