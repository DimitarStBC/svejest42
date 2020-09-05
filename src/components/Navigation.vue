<template>
  <ul class="nav nav-pills flex-column flex-sm-row">
    <li class="nav-item navbar-brand">
      <router-link class="nav-link" :to="{
            name: 'Landing'
              }">
        <img src="@/assets/logo.png" width="50" alt />
      </router-link>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#about" v-smooth-scroll>About</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Pricing</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Contact</a>
    </li>
    <li class="nav-item">
      <router-link class="nav-link" :to="{
            name: 'Blog'
              }">Blog</router-link>
    </li>
    <li class="nav-item">
      <router-link class="nav-link" :to="{
            name: 'Services'
              }">Services</router-link>
    </li>

    <LanguageSwitcher />
  </ul>
</template>

 <script>
import LanguageSwitcher from "../components/LanguageSwitcher";

export default {
  components: {
    LanguageSwitcher,
  },
};
</script>

<style scoped>
.nav {
  margin: 20px 0;
}
</style>