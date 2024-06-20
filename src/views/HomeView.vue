<template>
  <div>
    <section
      class="bg-[url('../assets/BackImageOne.jpg')] flex items-center bg-bottom bg-no-repeat bg-cover w-full mx-auto bg-b md:max-w-7xl h-[90vh]"
    >
      <div class="content pl-5 bg bg-gray-900 p-5 rounded-xl shadow-2xl">
        <h1 class=" text-xl text-white md:text-3xl *:first-letter:">
          {{ F_name }} <Span class="text-blue-500"> 
            {{ L_name }}
          </Span>
        </h1>
        <h1 class=" text-white md:text-xl">Developer, Programmer and Designer.</h1>
        <div class="mt-2 px-3 py-1 rounded gap-5  bg-white inline-flex">
            <img class="w-5 hover:scale-150 transition duration-300" src="../assets/icons8-facebook-50.png" alt="">
            <img class="w-5 hover:scale-150 transition duration-300" src="../assets/icons8-linkedin-50.png" alt="">
            <img class="w-5 hover:scale-150 transition duration-300" src="../assets/icons8-twitter-32.png" alt="">
            <img class="w-5 hover:scale-150 transition duration-300" src="../assets/icons8-github-50.png" alt="">
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const F_name = ref("Clinton");
    const L_name = ref("Karanja.")
    let path = "/about"

    return { F_name, L_name};
  },
};
</script>

<style lang="scss" scoped></style>
