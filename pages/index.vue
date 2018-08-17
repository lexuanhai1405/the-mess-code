<template>
  <v-container fluid
               fill-height
               class="container">
    <nav-header dark/>
    <main>
      <v-layout row
                wrap
                class="main-layout">
        <v-flex xs12
                sm6
                order-xs1
                order-sm0
                d-flex
                align-end
                justify-start>
          <section class="text--white">
            <h1 class="main-title">Hello,</h1>
            <h3 class="sub-title">My name is
              <span class="text--cyan">Hai</span>.
            </h3>
            <p class="paragraph">Welcome to
              <strong>the ugly code blocks</strong><br /> and
              <strong>the messy life</strong> of a full-stack developer.
            </p>
            <v-layout row
                      class="mt-5">
              <v-btn round
                     dark
                     large
                     color="orangeColor"
                     class="elevation-10 button">
                Visit my blog
              </v-btn>
              <v-btn flat
                     dark
                     large
                     round
                     class="button ml-2">
                My CV
              </v-btn>
            </v-layout>
          </section>
        </v-flex>
        <v-flex xs12
                sm6
                order-xs0
                order-sm1>
          <img src="/images/home/image_1.png"
               class="image" />
          <!-- <v-carousel dark
                      lazy
                      hide-controls
                      hide-delimiters
                      :interval="2000"
                      class="elevation-0">
            <v-carousel-item v-for="i in 4"
                             :key="i"
                             :src="'/images/home/image_' + i + '.png'"
                             reverse-transition="fade"
                             transition="fade">
            </v-carousel-item>
          </v-carousel> -->
        </v-flex>
      </v-layout>
    </main>
    <footer>

    </footer>
  </v-container>
</template>

<script>
  import NavHeader from "~/components/NavHeader";

  export default {
    components: {
      NavHeader
    }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/scss/main.scss";

  .container {
    display: block;
    background-color: $color-blue;
    background-repeat: no-repeat;
    background-image: url("/images/home/background.png");
    background-position: top center;
    background-size: cover;
    padding: 0;
    margin: 0;
  }

  // .main-layout {
  //   margin-top: 24px;
  // }

  .text--cyan {
    color: $color-cyan;
  }

  .text--white {
    color: white;
  }

  .main-title {
    font-weight: 700;
    font-size: 64px;
    margin-left: -2px;
  }

  .sub-title {
    font-weight: 700;
    font-size: 28px;
    margin-top: -1rem;
  }

  .paragraph {
    font-weight: 300;
    font-size: 18px;
    margin-top: 1.5rem;
  }

  .paragraph > strong {
    font-weight: 700;
  }

  .button {
    margin: 0;
    text-transform: none;
    font-weight: 700;
    font-size: 18px;
  }

  .image {
    width: 100%;
    height: auto;
    margin-bottom: 32px;
  }

  .fade {
    &-enter-active,
    &-leave-active,
    &-leave-to {
      transition: 1s ease-out;
      position: absolute;
      top: 0;
      left: 0;
    }
    &-enter,
    &-leave,
    &-leave-to {
      opacity: 0;
    }
  }

  /deep/ .v-jumbotron__image {
    max-width: 80%;
    height: auto;
  }

  /deep/ .v-carousel {
    height: 400px;
  }
</style>
