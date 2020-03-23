<template>
    <section id="hero">
    <v-row no-gutters>
        <v-theme-provider dark>
          <v-container fill-height>
            <v-row align="center" class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="12" tag="h1">
                <span
                  class="font-weight-black"
                  :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                >Site Build In Progress</span>
              </v-col>
            </v-row>
          </v-container>
        </v-theme-provider>
      </v-img>
    </v-row>
  </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>