<template>
  <ul class="nav nav-pills flex-column flex-sm-row">
    <li class="nav-item navbar-brand">
      <router-link class="nav-link" :to="{
            name: 'Landing'       
            }">
        <img src="@/assets/logo.png" width="50" alt />
      </router-link>
    </li>
    <li class="nav-link">
      <LanguageSwitcher />
    </li>
    <li class="nav-item">
      <router-link
        class="nav-link"
        :to="{
            name: 'Landing'
              }"
        @click.native="scrollFix('#about')"
      >About</router-link>
    </li>
    <li class="nav-item">
      <router-link
        class="nav-link"
        :to="{
            name: 'Landing'
              }"
        @click.native="scrollFix('#pricing')"
      >Pricing</router-link>
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
  </ul>
</template>

 <script>
import LanguageSwitcher from "../components/LanguageSwitcher";
import $ from "jquery";

export default {
  components: {
    LanguageSwitcher,
  },
  mounted: function () {
    setTimeout(() => this.scrollFix(this.$route.hash), 1);
  },
  methods: {
    scrollFix: function (hashbang) {
      setTimeout(
        () =>
          $("html, body").animate(
            {
              scrollTop: $(hashbang).offset().top,
            },
            800
          ),
        1
      );
    },
  },
};
</script>

<style scoped>
.nav {
  margin: 20px 0;
}
</style>