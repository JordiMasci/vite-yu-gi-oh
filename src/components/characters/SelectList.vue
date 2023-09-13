<script>
import axios from "axios";

export default {
  data() {
    return {
      types: [],
      currentType: "",
    };
  },

  methods: {
    fetchTypes() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/archetypes.php")
        .then((res) => {
          this.types = res.data;
          console.log(res.data);
        });
    },
    changeType() {
        console.log(this.currentType)
    },
  },

  created() {
    this.fetchTypes();
  },

};
</script>

<template>
  <!-- SELECT -->
  <select
    @change="changeType()"
    v-model="currentType"
    class="form-select"
    aria-label="Default select example"
  >
    <option
      v-for="(type, index) in types"
      :value="type.archetype_name"
      :key="index"
    >
      {{ type.archetype_name }}
    </option>
  </select>
</template>

<style lang="scss" scoped></style>
