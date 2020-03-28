<template>
  <section id="blog">
    <div class="py-12"></div>

    <v-container>
      <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Recent Projects</h2>

      <v-responsive class="mx-auto mb-12" width="56">
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col v-for="({ src, text, title, url }, i) in articles" :key="i" cols="12" md="4">
          <v-img :src="src" class="mb-4" height="275" max-width="100%"></v-img>
          <div class="projects-card">
            <h3 class="font-weight-black mb-4 text-uppercase" v-text="title"></h3>

            <div class="title font-weight-light mb-5" v-text="text"></div>

            <a :href="url"><v-btn class="ml-n4 font-weight-black" text>Visit Site</v-btn></a>
          </div>
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
      articles: [
        {
          src: '/coffee-proj.jpg',
          title: 'KC Home Barista',
          text:
            'Barista Tutorial and Coffee Education website. This site was built using Nuxt.js, Vuetify, and boasts an Express/Node backend and a SQL database. ',
          url: '#'
        },
        {
          src: '/comic-proj.jpg',
          title: 'My Hero Comics',
          text:
            'This website is a comic book lookup and collection tracking website. This site uses Handlebars, Sequelize, and Passport.js for Authentication',
          url: 'https://myherocomics.herokuapp.com/'
        },
        {
          src: '/event-proj.jpg',
          title: 'Real World Events',
          text:
            'This is an event lookup website, that allows event creation and tracking. It is built on Nuxt.js, Bootstrap, and SQL on the back end. ',
          url: 'https://secure-dawn-98530.herokuapp.com/'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.projects-card {
  height: 300px;
}
</style>