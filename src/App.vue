<script>
import axios from "axios";
import { store } from "./data/store";

import AppHeader from "./components/AppHeader.vue";
import AppSearch from "./components/AppSearch.vue";
import CharacterList from "./components/CharacterList.vue";

export default {
  name: "App",
  data() {
    return {
      store,
    };
  },
  components: {
    AppHeader,
    AppSearch,
    CharacterList,
  },
  methods: {
    getCharacters() {
      axios
        .get(store.apiUrl, {
          params: {
            category: store.categoryToSearch,
          },
        })
        .then((result) => {
          store.charactersListData = result.data;
          console.log(store.charactersListData);
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
  mounted() {
    this.getCharacters();
  },
};
</script>

<template>
  <AppHeader title="Breaking Bad Api" />
  <main>
    <AppSearch @startSearch="getCharacters()" />
    <CharacterList />
  </main>
</template>


<style lang="scss">
@use "./styles/general";
</style>