<template>
  <div id="app">


   
   <header>
      <!-- <na-link to="/lost-items" class="nav-link"> Lost Items </router-link>
        <router-link to="/found-items" class="nav-link"> Found Items </router-link>
        <router-link to="/Register" class="nav-link"> Register </router-link> -->
       
      </header>
      <router-view></router-view>

      </div>
      </template>

        <script>
         import '@fortawesome/fontawesome-free/css/all.css'

        </script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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
}
</style>
