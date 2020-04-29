<template>
  <section id="hero">
    <v-row no-gutters>
      <v-img :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'" src="/main-page.jpg">
        <v-theme-provider dark>
          <v-container fill-height>
            <v-row class="black--text mx-auto" justify="center">
              <v-col class="black--text text-center" cols="12" tag="h1">
                <span
                  class="font-weight-black"
                  :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                >HI! I'M TYLER</span>

                <br />

                <span
                  :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
                  class="font-weight-light"
                >I'm a Full Stack Web Developer</span>
              </v-col>

              <v-btn class="align-self-end" fab outlined @click="$vuetify.goTo('#about-me')">
                <v-icon>mdi-chevron-double-down</v-icon>
              </v-btn>
            </v-row>
          </v-container>
        </v-theme-provider>
      </v-img>
    </v-row>
  </section>
</template>

<script>
export default {}
</script>

<style lang="css" scoped>
</style>