<template>
  <section id="projects">
    <v-row>
      <v-col cols="12" sm="6" offset-sm="3">
        <v-card>
          <v-container fluid>
            <v-row>
              <v-col v-for="n in 9" :key="n" class="d-flex child-flex" cols="4">
                <a href="https://www.reddit.com">
                  <v-card flat tile class="d-flex project-photo">
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="grey lighten-2"
                    >
                      <template v-slot:placeholder>
                        <v-row class="fill-height ma-0" align="center" justify="center">
                          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-row>
                      </template>
                    </v-img>
                  </v-card>
                </a>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {link: "#", picture: "#"},
        {link: "#", picture: "#"},
        {link: "#", picture: "#"},
        {link: "#", picture: "#"},
        {link: "#", picture: "#"},
        {link: "#", picture: "#"},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.projects-card {
  height: 300px;
}
.link-decor {
  text-decoration: none;
}
.project-photo {
  cursor: pointer;
}
.project-photo:hover {
  border: solid white 2px;
  box-shadow: white 0 1px 1px;
}
</style>