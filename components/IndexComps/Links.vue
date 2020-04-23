<template>
  <div>
    <section id="stats">
      <v-parallax :height="$vuetify.breakpoint.smAndDown ? 700 : 500" src="/background-image.png">
        <v-container fill-height>
          <v-row class="mx-auto">
            <v-col v-for="[value, title, link] of stats" :key="title" cols="12" md="3">
              <div class="text-center">
                <div class="display-3 font-weight-black mb-4" v-text="value"></div>

                <a :href="link" class="links" target="_blank">
                  <v-btn class="title font-weight-regular text-uppercase" v-text="title"></v-btn>
                </a>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-parallax>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      stats: [
        ['GitHub', 'Check out My Projects', 'https://github.com/tboyd4'],
        [
          'LinkedIn',
          'Get Connected!',
          'https://www.linkedin.com/in/tyler-boyd-a40770198/'
        ],
        ['Resume', 'Take a Look at My Experience', '/tyler boyd.pdf']
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.links {
  text-decoration: none;
  color: white;
}
</style>