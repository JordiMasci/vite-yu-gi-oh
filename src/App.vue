<script>
// import MyComponent from "./components/MyComponent. vue!";

export default {
  data() {
   return {
     title: "Hello world"
   }
 }

 // components: {
 //   MyComponent,
 // },
};
</script>

<template>
   <h1 class="text-danger">{{ title }} <font-awesome-icon icon="fa-solid fa-user-secret" /></h1>
</template>

<style lang="scss" scoped></style>
