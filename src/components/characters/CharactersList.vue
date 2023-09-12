<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Lista card",
      characters: [],
    };
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((res) => {
        // console.log(res.data.data);
        this.characters = res.data.data
      });
  },
};
</script>

<template>
  <section>
    <h3>{{ title }}</h3>
  </section>
</template>

<style lang="scss" scoped></style>
