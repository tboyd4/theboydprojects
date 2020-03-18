<template>
  <v-content>
    <section id="hero">
      <v-row no-gutters>
        <v-img
          :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          src="/frontpage.jpg"
        >
          <v-theme-provider dark>
            <v-container fill-height>
              <v-row align="center" class="black--text mx-auto" justify="center">
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

    <section id="about-me">
      <v-parallax :height="$vuetify.breakpoint.smAndDown ? 900 : 600" src="/devback3.jpg">
        <v-container class="text-center white black--text">
          <h2 class="display-2 font-weight-bold mb-3">ABOUT ME</h2>

          <v-responsive class="mx-auto mb-8" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-responsive class="mx-auto title font-weight-light mb-8" max-width="720">
            In west Philadelphia born and raised
            On the playground was where I spent most of my days
            Chillin' out maxin' relaxin' all cool
            And all shooting some b-ball outside of the school
            When a couple of guys who were up to no good
            Started making trouble in my neighborhood
            I got in one little fight and my mom got scared
            She said, "You're movin' with your auntie and uncle in Bel-Air"
          </v-responsive>

          <v-avatar class="elevation-12 mb-12" size="128">
            <v-img src="/mephoto.jpeg"></v-img>
          </v-avatar>

          <div></div>
        </v-container>
      </v-parallax>
    </section>

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

    <section id="stats">
      <v-parallax :height="$vuetify.breakpoint.smAndDown ? 700 : 500" src="/links.jpg">
        <v-container fill-height>
          <v-row class="mx-auto">
            <v-col v-for="[value, title, link] of stats" :key="title" cols="12" md="3">
              <div class="text-center">
                <div class="display-3 font-weight-black mb-4" v-text="value"></div>

                <a :href="link" class="links">
                  <div class="title font-weight-regular text-uppercase" v-text="title"></div>
                </a>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-parallax>
    </section>

    <section id="blog">
      <div class="py-12"></div>

      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Blog</h2>

        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col v-for="({ src, text, title }, i) in articles" :key="i" cols="12" md="4">
            <v-img :src="src" class="mb-4" height="275" max-width="100%"></v-img>

            <h3 class="font-weight-black mb-4 text-uppercase" v-text="title"></h3>

            <div class="title font-weight-light mb-5" v-text="text"></div>

            <v-btn class="ml-n4 font-weight-black" text>Continue Reading</v-btn>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <v-sheet id="contact" color="#333333" dark tag="section" tile>
      <div class="py-12"></div>

      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Contact Me</h2>

        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-theme-provider light>
          <v-row>
            <v-col cols="12">
              <v-text-field flat label="Name*" solo></v-text-field>
            </v-col>

            <v-col cols="12">
              <v-text-field flat label="Email*" solo></v-text-field>
            </v-col>

            <v-col cols="12">
              <v-text-field flat label="Subject*" solo></v-text-field>
            </v-col>

            <v-col cols="12">
              <v-textarea flat label="Message*" solo></v-textarea>
            </v-col>

            <v-col class="mx-auto" cols="auto">
              <v-btn color="accent" x-large>Submit</v-btn>
            </v-col>
          </v-row>
        </v-theme-provider>
      </v-container>

      <div class="py-12"></div>
    </v-sheet>
  </v-content>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          src:
            'https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Mobile first & Responsive',
          text:
            'Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum.'
        },
        {
          src:
            'https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Think outside the box',
          text:
            'Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.'
        },
        {
          src:
            'https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80',
          title: 'Small changes, big difference',
          text:
            'Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.'
        }
      ],
      features: [
        {
          icon: 'mdi-account-group-outline',
          title: 'Client-Side',
          text: 'HTML5, CSS, JavaScript, React.js, Vue.js, Vuex, Nuxt.js, JQUERY, BootStrap, MaterializeCSS, Vuetify'
        },
        {
          icon: 'mdi-update',
          title: 'Server-Side',
          text: 'Node.js, Express, Passport.js, API Creation, MongoDB, mySQL, Mongoose.js, Sequelize'
        },
        {
          icon: 'mdi-shield-outline',
          title: 'Concepts and Technologies',
          text: 'Best Practice Coding, Code Linting, MVC, Git Collaboration, Development to Production Builds, Application Deployment, Domain Management'
        }
      ],
      stats: [
        ['GitHub', 'Check out My Projects', 'https://github.com/tboyd4'],
        ['LinkedIn', 'Get Connected!', 'https://www.linkedin.com/in/tyler-boyd-a40770198/'],
        ['Resume', 'Take a Look at My Experience', '/tyler boyd.pdf']
      ]
    }
  }
}
</script>

style <style scoped>
  .links {
    text-decoration: none;
    color: white;
  }
</style>
