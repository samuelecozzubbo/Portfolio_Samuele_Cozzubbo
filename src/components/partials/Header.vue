<script>
import Navbar from './Navbar.vue';
export default {
    name: 'Header',
    components:{
        Navbar,
    }
}
</script>

<template>
    <header>
        <Navbar/>
    </header>
</template>

<style lang="scss" scoped>
header{
    width: 100%;
    background-color: white;
    height: 50px;
}
</style>