<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="container">
      <nav
        class="navbar navbar-expand-lg bg-body-tertiary-center">
          <a>القرآن</a>
          <router-link :class="{ active: $route.name === 'surah' }" class="y nav-link" to="/surah">Surah</router-link>
          <router-link :class="{ active: $route.name === 'about' }" class="y nav-link" to="/about" >About Us</router-link>
      </nav>
      <img src="../src/assets/w1.png"/>
    </div>
    
    
  </header>
  <RouterView />
</template>

<style scoped>
a{
  font-size: 40px;
}
.y {
  color: rgb(23, 21, 21);

    align-items: center;
    list-style: none;
    text-decoration: none;
}
.navbar-expand-lg {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    text-align: center;
    background: linear-gradient(rgba(9, 80, 231, 0.96), rgba(60, 125, 190, 0.9), rgba(218, 224, 224, 0.96)),center/cover no-repeat;
    background-size: cover;
    display: flex;
    justify-content: space-between;
    padding: 5px 10px ;

}
.y:hover {
    color: #06060b;
    font-size: 20px;
    transition: .2s;
    background-color: rgba(95, 98, 99, 0.595);
}

.active {
  color: black !important;
    text-align: center;
    padding: 5px;
}
header{
  text-align: center;
  background-image: url("../src/assets/p.jpg");
  background-size: cover;
  
  
  
}
</style>

