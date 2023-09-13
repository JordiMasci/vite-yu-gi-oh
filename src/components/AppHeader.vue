<script>
export default {
  data() {
    return {
      title: "Yu-Gi-Oh Api",
    };
  },
};
</script>

<template>
  <h1><font-awesome-icon icon="fa-solid fa-user-secret" />{{ title }}</h1>
  <!-- SELECT -->
  <select class="form-select" aria-label="Default select example">
    <option selected>Open this select menu</option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
</template>

<style lang="scss" scoped></style>
