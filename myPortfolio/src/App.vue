<template>
  <section>
    <header class="w-full mx-auto h-[10vh] relative md:max-w-7xl">
      <div class="wrapper">
        <nav
         
          class="absolute right-5 top-10 w-10 cursor-pointer flex items-center justify-center sm:w-20"
        >
          <div @click = "hundleClick" class="trasition duration-1000">
            <img v-if="hum" class="w-5 sm:w-10" src="./assets/hamburger.png" />
            <img v-else class="w-5 sm:w-10" src="./assets/close.png" />
          </div>
          
        </nav>
      </div>
    </header>
  </section>
  <div v-if="hum">
    <HomeView />
  </div>
  <div v-else>
    <AboutView />
  </div>
  <RouterViewv/>
</template>

<script>
import { ref } from "vue"
import HomeView from './views/HomeView.vue';
import AboutView from './views/AboutView.vue';
import { RouterView } from "vue-router";
export default {
  components: { HomeView, AboutView },

setup (){
  const hum = ref(true);
  
  
  const hundleClick = () => {
    hum.value = !hum.value
  }

  return{ hum, hundleClick}
}


}
 
</script>

<style scoped></style>
