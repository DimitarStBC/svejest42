<template>
  <ul class="d-flex justify-content-center">
    <li @click="setLocale('en')">ENG</li>|
    <li @click="setLocale('bg')">BUL</li>|
    <li @click="setLocale('ru')">RUS</li>
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