<template>
  <div id="app" class="container">
    <Navigation />

    <router-view />
  </div>
</template>

<script>
import Navigation from "./components/Navigation";

export default {
  name: "app",
  components: {
    Navigation,
  },
};
</script>

<style>
::-webkit-scrollbar {
  width: 8px;
}
::-webkit-scrollbar-thumb {
  background: rgb(168, 187, 224);
}
</style>
