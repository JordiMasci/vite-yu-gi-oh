<script>
import SelectList from './characters/SelectList.vue';

export default {
components: { SelectList },

  data() {
    return {
      title: "Yu-Gi-Oh Api",
    };
  },
};
</script>

<template>
  <h1><font-awesome-icon icon="fa-solid fa-user-secret" />{{ title }}</h1>
  <SelectList />
</template>

<style lang="scss" scoped></style>
