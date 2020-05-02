<template>
  <section id="blog">
    <v-container>
      <v-responsive class="mx-auto mb-12" width="56">
        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col
          v-for="({ src, text, title, url }, i) in projects"
          :key="i"
          cols="12"
          md="4"
        >
          <v-img :src="src" class="mb-4" height="275" max-width="100%"></v-img>
          <div class="projects-card">
            <h3
              class="font-weight-black mb-4 text-uppercase"
              v-text="title"
            ></h3>

            <div class="title font-weight-light mb-5" v-text="text"></div>

            <a :href="url" class="link-decor"
              ><v-btn class="ml-n4 font-weight-black" text>Visit Site</v-btn></a
            >
          </div>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-3"></div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          src: '/vuetify.png',
          title: 'Dashboard Application',
          text: 'Application to Showcase a Dashboard built with Vue + Vuetify.',
          url: 'https://vuetify-dashboard-34123.herokuapp.com/'
        },
        {
          src: '/budget.jpg',
          title: 'Budget Tracker',
          text: 'Budget Tracker Application, with Offline Functionality',
          url: 'https://new-budget-tracker-1231.herokuapp.com/'
        },
        {
          src: '/IMG_0570.jpg',
          title: 'Lindsey Renae Photography',
          text: 'Photography Portfolio for Lindsey Renae Photo.',
          url: 'https://www.lindseyrenaephoto.com/'
        },
        {
          src: '/notes-img.jpeg',
          title: 'Knowtepad Note Taking',
          text: 'Note Taking and Saving Application, built with JavaScript',
          url: 'https://afternoon-castle-15258.herokuapp.com/'
        },
        {
          src: '/flooring-img.jpg',
          title: 'Flooring Company Website',
          text: 'Website for Local Flooring Company, to display info and show work. ',
          url: 'https://gallant-dijkstra-f572c4.netlify.app/'
        },
        {
          src: '/events-img.jpg',
          title: 'Event Tracking',
          text: 'Application to display events received from database, using Nuxt.js',
          url: 'https://nifty-thompson-b0a8ab.netlify.app/'
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects-card {
  height: 300px;
}
.link-decor {
  text-decoration: none;
}
</style>
