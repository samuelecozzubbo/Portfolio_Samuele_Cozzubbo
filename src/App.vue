<script>
import { RouterLink, RouterView } from 'vue-router';
import Header from './components/partials/Header.vue';
export default {
  components: {
    Header,
  }
}
</script>

<template>
    <Header/>
    <router-view>
    </router-view>
  
  
</template>

<style scoped lang="scss">

</style>
