<template>
  <v-content>
    <Landing></Landing>
    <AboutMe></AboutMe>
    <Profs></Profs>
    <Links></Links>
    <Projs></Projs>
    <v-container>
       <v-row>
        <nuxt-link to="/projects" class="link-decor"><v-btn class="ml-n4 font-weight-black" text>See More Projects</v-btn></nuxt-link>
      </v-row>
    </v-container>
    <Contact></Contact>
  </v-content>
</template>

<script>
import Landing from "../components/IndexComps/Landing.vue";
import AboutMe from "../components/IndexComps/AboutMe.vue";
import Profs from "../components/IndexComps/Profs.vue";
import Links from "../components/IndexComps/Links.vue";
import Projs from "../components/IndexComps/Projs.vue";
import Contact from "../components/IndexComps/Contact.vue";


export default {
  components: {
    Landing,
    AboutMe,
    Profs,
    Links,
    Projs,
    Contact
  }
}
</script>

style <style scoped>
.link-decor {
  text-decoration: none;
}
</style>
