<template>
    <section id="about-me">
      <v-parallax :height="$vuetify.breakpoint.smAndDown ? 900 : 600" src="/devback3.jpg">
        <v-container class="text-center white black--text">
          <h2 class="display-2 font-weight-bold mb-3">WHAT I DO</h2>

          <v-responsive class="mx-auto mb-8" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-responsive class="mx-auto title font-weight-light mb-8" max-width="720">
            Hello! My name is Tyler, and I want to build your website. I want to work with you
            to create something that will help your business or pursuit stand out. Whatever you envision
            as the perfect website for you, I want to help you get it. I am a Web Developer based in Kansas City,
            and I have been working, learning, and perfecting my art so that I can help people like yourself fulfull
            your passions. I want to help you put your ideas on the internet, because once it's on the internet,
            it's real. Let's work together to create something awesome.
          </v-responsive>

          <v-avatar class="elevation-12 mb-12" size="128">
            <v-img src="/mephoto.jpeg"></v-img>
          </v-avatar>

          <div></div>
        </v-container>
      </v-parallax>
    </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>