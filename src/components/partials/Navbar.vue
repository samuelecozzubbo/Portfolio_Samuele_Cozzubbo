<script>
export default {
    name : 'Navbar',
}
</script>

<template>
    <nav>
      <div class="logo">
        SAMUELE COZZUBBO
      </div>
      <div>
        <routerLink :to="{name:'home' }">Home</routerLink>
        <routerLink :to="{name:'about' }">About</routerLink>
      </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
  background-color: rgb(255, 255, 255);
  max-width: 1120px;
  margin: 0 auto;
  padding: 0 20px;
  height: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  a.router-link-exact-active {
    color: hsla(160, 100%, 37%, 1);
    transition: color 0.4s;
  }
  a .router-link-exact-active:hover {
    background-color: lightgrey;
  }

  a {
    display: inline-block;
    padding: 0 2rem;
    border-left: 1px solid var(--color-border);
    text-decoration: none;
  }

  a:first-of-type {
    border: 0;
  }
  }
</style>