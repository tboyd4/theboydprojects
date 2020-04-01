<template>
  <div>
    <navigation></navigation>
    <v-container>
      <div class="py-12"></div>
      <ProjectsGrid></ProjectsGrid>
      <div class="py-6"></div>
    </v-container>
  </div>
</template>

<script>
import ProjectsGrid from '../components/ProjectsComps/ProjectGrid.vue'
import NavBar from '../components/ProjectsComps/NavBar.vue'
export default {
  components: {
    ProjectsGrid,
    navigation: NavBar
  }
}
</script>

<style scoped>
</style>