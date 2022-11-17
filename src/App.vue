<script>
import axios from "axios";

import AppHeader from "./components/AppHeader.vue";
import AppSearch from "./components/AppSearch.vue";
import CharacterList from "./components/CharacterList.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppSearch,
    CharacterList,
  },
  mounted() {
    //https://www.breakingbadapi.com/api/characters
    axios
      .get("https://www.breakingbadapi.com/api/characters")
      .then((result) => {
        console.log(result.data);
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<template>
  <AppHeader title="Breaking Bad Api" />
  <main>
    <AppSearch />
    <CharacterList />
  </main>
</template>


<style lang="scss">
@use "./styles/general";
</style>