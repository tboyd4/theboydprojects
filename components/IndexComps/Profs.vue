<template>
  <section id="features" class="grey lighten-3">
    <div class="py-12"></div>

    <v-container class="text-center black--text">
      <h2 class="display-2 font-weight-bold mb-3">My Proficiencies</h2>

      <v-responsive class="mx-auto mb-12" width="56">
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col v-for="({ icon, title, text }, i) in features" :key="i" cols="12" md="4">
          <v-card class="py-12 px-4" height="100%" color="grey lighten-5 black--text" flat>
            <v-theme-provider dark>
              <div>
                <v-avatar color="primary" size="88">
                  <v-icon large v-text="icon"></v-icon>
                </v-avatar>
              </div>
            </v-theme-provider>

            <v-card-title
              class="justify-center font-weight-black black--text text-uppercase"
              v-text="title"
            ></v-card-title>

            <v-card-text class="subtitle-1 black--text" v-text="text"></v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          icon: 'mdi-account-group-outline',
          title: 'Client-Side',
          text:
            'HTML5, CSS, JavaScript, React.js, Vue.js, Vuex, Nuxt.js, JQUERY, BootStrap, MaterializeCSS, Vuetify'
        },
        {
          icon: 'mdi-update',
          title: 'Server-Side',
          text:
            'Node.js, Express, Passport.js, API Creation, MongoDB, mySQL, Mongoose.js, Sequelize'
        },
        {
          icon: 'mdi-shield-outline',
          title: 'Concepts and Technologies',
          text:
            'Best Practice Coding, Code Linting, MVC, Git Collaboration, Development to Production Builds, Application Deployment, Domain Management'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
</style>