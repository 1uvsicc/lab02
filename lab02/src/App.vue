<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
<div id="layout">
   <header>
     <div class="wrapper">
       <nav>
         <RouterLink to="/">Home</RouterLink> |
         <RouterLink to="/about">About</RouterLink>
       </nav>
     </div>
   </header>

   <RouterView />
 </div>

</template>

<style scoped>
#layout {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  
  color: #2c3e50;
}

nav {
  padding: 30px;
 }



nav a {
  font-weight: bold;
  color: #2c3e50;

}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
