<template>
  <header class="header">
    <nav class="mt-3">
      <v-layout row
                align-center>
        <v-flex sm4
                d-flex
                align-center>
          <nuxt-link to="/"
                     :class="[ dark ? 'link--dark' : 'link--light' ]">
            <v-layout row
                      align-center>
              <div :class="[ dark ? 'logo--dark' : 'logo--light', 'logo' ]"></div>
              <span class="ml-2">theMessCode</span>
            </v-layout>
          </nuxt-link>
        </v-flex>
        <v-flex sm8
                d-flex
                align-center
                justify-end>
          <nuxt-link to="/"
                     :class="[ dark ? 'link--dark' : 'link--light', 'flexbox--none', 'link__right' ]">
            Home
          </nuxt-link>
          <nuxt-link to="/blog"
                     :class="[ dark ? 'link--dark' : 'link--light', 'flexbox--none', 'link__right' ]">
            Blog
          </nuxt-link>
          <nuxt-link to="/cv"
                     :class="[ dark ? 'link--dark' : 'link--light', 'flexbox--none', 'link__right' ]">
            CV
          </nuxt-link>
          <nuxt-link to="/about"
                     :class="[ dark ? 'link--dark' : 'link--light', 'flexbox--none', 'link__right' ]">
            About
          </nuxt-link>
        </v-flex>
      </v-layout>
    </nav>
  </header>
</template>

<script>
  export default {
    name: "NavHeader",
    props: {
      dark: {
        type: Boolean,
        default: false
      }
    }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/scss/main.scss";

  .logo {
    height: 20px;
    width: 32px;
    -webkit-mask-image: url("/icons/logo.svg");
    -webkit-mask-repeat: no-repeat;

    &--light {
      background-color: $color-blue;
    }
    &--dark {
      background-color: white;
    }
  }

  .header {
    font-size: 14px;
    font-weight: 300;
  }

  .link {
    &--light {
      color: $color-blue;
      text-decoration: unset;
    }
    &--dark {
      color: white;
      text-decoration: unset;
    }

    &__right {
      margin-left: 3em;
    }
  }
</style>

