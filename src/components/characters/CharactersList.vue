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
          console.log(res.data.data);
        });
    },
  },

  created() {
    this.fetchCharacters();
  },
};
</script>

<template>
  <section class="container mt-5">
    <div class="row g-4">
      <div
        class="col-custom"
        v-for="character in characters"
        :key="character.id"
      >
        <img :src="character.card_images[0].image_url" alt="" />
        <p>{{ character.name }}</p>
        <p>{{ character.archetype }}</p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.container {
  background-color: orange;
  text-align: center;

  img {
    width: 100%;
  }

  .col-custom {
    width: 20%;
  }
}
</style>
