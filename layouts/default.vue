<template>
  <v-app class="app">
    <nuxt />
  </v-app>
</template>

<style>
  html {
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
  }

  .app {
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
  }

  html,
  body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
  }

  header,
  main,
  footer {
    padding: 24px 0;
    width: 90%;
    max-width: 1006px;
    margin: 0 auto;
  }
</style>
