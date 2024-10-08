<script>
export default {
    name : 'Navbar',
    data() {
      return {
        isOpen: false, // Stato del menu
      };
    },
    methods: {
      toggleMenu() {
        this.isOpen = !this.isOpen; // Alterna il menu
      },
  },
}
</script>

<template>
    <nav>
      <div class="logo">
        SAMUELE COZZUBBO
      </div>
      <!-- Hamburger Icon -->
      <div class="hamburger" @click="toggleMenu">
        <i class="fa fa-bars"></i>
      </div>
      <!-- Links -->
      <div class="nav-links" :class="{ open: isOpen }">
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
  /* Hamburger menu */
  .hamburger {
    display: none;
    font-size: 2rem;
    cursor: pointer;
  }
  .nav-links{
    &.open {
      display: block;
    }
  }

/* Media query */
@media (max-width: 768px) {
  .hamburger {
      display: block; /* Mostra l'hamburger su schermi piccoli */
    }

  .nav-links {
    display: none; /* Nascondi i link di navigazione su mobile */

    &.open {
      display: block; /* Mostra il menu dropdown se isOpen è true */
      position: absolute;
      top: 50px;
      right: 20px;
      background-color: white;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 10px;
      border-radius: 8px;
      z-index: 1000;

      a {
        display: block;
        margin-bottom: 10px;
        padding: 10px 0;
      }
    }
  }
}

</style>