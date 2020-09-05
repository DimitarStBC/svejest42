<template>
  <ul class="d-flex justify-content-center">
    <li class="liBTN" v-b-modal.activationLinkModal id="enLi" @click="setLocale('en')">English |</li>
    <li class="liBTN" v-b-modal.activationLinkModal id="bgLi" @click="setLocale('bg')">Български |</li>
    <li class="liBTN" v-b-modal.activationLinkModal id="ruLi" @click="setLocale('ru')">Руский |</li>
    <b-modal
      ok-only
      ref="modal"
      class="modal fade"
      id="activationLinkModal"
      tabindex="-1"
      aria-hidden="true"
    >
      <div>
        <div>
          <li v-on:click="changeActiveEn()" @click="setLocale('en')">English</li>
          <li v-on:click="changeActiveBg()" @click="setLocale('bg')">Български</li>
          <li v-on:click="changeActiveRu()" @click="setLocale('ru')">Руский</li>
        </div>
      </div>
    </b-modal>
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
    changeActiveEn: function () {
      document.getElementById("bgLi").style.display = "none";
      document.getElementById("ruLi").style.display = "none";
      document.getElementById("enLi").style.display = "inline-block";
      this.$refs["modal"].toggle(".liBTN");
    },
    changeActiveBg: function () {
      document.getElementById("bgLi").style.display = "inline-block";
      document.getElementById("ruLi").style.display = "none";
      document.getElementById("enLi").style.display = "none";
      this.$refs["modal"].toggle(".liBTN");
    },
    changeActiveRu: function () {
      document.getElementById("bgLi").style.display = "none";
      document.getElementById("ruLi").style.display = "inline-block";
      document.getElementById("enLi").style.display = "none";
      this.$refs["modal"].toggle(".liBTN");
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
#enLi {
  display: none;
}
#ruLi {
  display: none;
}
.liBTN {
  color: green;
}
li {
  list-style-type: none;
  cursor: pointer;
}
</style>