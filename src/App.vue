<script setup lang="ts">
import MyImage from "./components/MyImage.vue";
const onLoad = (e: Event) => {
  console.log("load: ", e);
};
const onError = (e: Event) => {
  console.log("error: ", e);
};
</script>

<template>
  <header>
    <div class="wrapper">
      <MyImage
        src="https://avatars.githubusercontent.com/u/6128107?s=200&v=4"
        v-on:load="onLoad"
      ></MyImage>

      <MyImage src="error.png" v-on:error="onError"></MyImage>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
