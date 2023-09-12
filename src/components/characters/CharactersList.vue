<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista card",
      characters: [],
    };
  },

  methods: {
    fetchCharacters() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then((res) => {
          this.characters = res.data.data;
          console.log(res.data.data)
          
        });
    },
  },

  created() {
    this.fetchCharacters();
  },
};
</script>

<template>
  <section class="container">
    <h3>{{ title }}</h3>

    <div class="row g-4">
        <div class="col-4" v-for="character in characters" :key="character.id">
            {{ character.name }}
        </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
