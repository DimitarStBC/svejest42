<template>
  <ul class="languageMenu">
    <li id="enLi" v-on:click="changeActiveEn()" @click="setLocale('en')">ENG</li>|
    <li style="color: #3D853C" id="bgLi" v-on:click="changeActiveBg()" @click="setLocale('bg')">BUL</li>|
    <li id="ruLi" v-on:click="changeActiveRu()" @click="setLocale('ru')">RUS</li>
  </ul>
</template>

<script>
export default {
  name: "LanguageSwitcher",
  methods: {
    setLocale: function (locale) {
      this.$i18n.locale = locale;
      this.$router.push({
        params: { lang: locale },
      });
    },
  },
  data: function () {
    return {
      classActive: {
        inactive: false,
        active: true,
      },
    };
  },
};
</script>

<style scoped>
</style>