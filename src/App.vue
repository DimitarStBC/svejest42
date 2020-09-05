<template>
  <div id="app container">
    <div>
      <LanguageSwitcher />
    </div>

    <router-view />
  </div>
</template>

<script>
import LanguageSwitcher from "./components/LanguageSwitcher";

export default {
  name: "app",
  components: {
    LanguageSwitcher,
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
