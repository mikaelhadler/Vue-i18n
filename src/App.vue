<template>
  <div id="app">
    <h1>{{ $t("message.welcome") }}</h1>
    <button @click="setLocale">{{ $t("message.alterLanguage") }}</button>
  </div>
</template>

<script>
import Vue from "vue";

export default {
  name: "App",
  methods: {
    setLocale() {
      Vue.config.lang = Vue.config.lang === 'ja' ? 'en' : 'ja';
      this.$i18n.locale = Vue.config.lang;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
