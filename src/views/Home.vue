<script>
import Jumbotron from '@/components/partials/Jumbotron.vue';
import Projects from '@/components/partials/Projects.vue';

export default {
  name: 'Home',
  components: {
    Jumbotron,
    Projects,
  },
}
</script>

<template>
  <main>
   <Jumbotron/>
   <Projects/>
  </main>
</template>

<style lang="scss">

</style>
