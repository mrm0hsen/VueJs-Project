<template>
  <Home :user-info="userInfo" />
  <h1>App.Vue</h1>
</template>

<script>
import HomeComponent from "./components/HomeComponent.vue";

export default {
  components: {
    Home: HomeComponent,
  },
  data() {
    return {
      userInfo: {
        name: "Mohsen",
        age: 27,
      },
    };
  },
};
</script>

<style scoped></style>
