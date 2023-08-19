<template>
   <header
    :class="{ 'shadow-md bg-white': isScrolled }"
    class="sticky relative top-0 w-full py-4 bg-transparent z-50 lg:px-[80px] px-[16px]"
  >
    <div class="max-w-[1200px] mx-auto w-full flex items-center justify-between">
      <div>
        <img class="sm:w-[200px] w-[120px]" src="/icons/logo.svg" alt="agency_ai_logo">
      </div>
      <nav class="nav-desktop">
        <ul class="header_one flex items-center lg:space-x-8 space-x-4">
          <NuxtLink to="/" class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Products</NuxtLink>
          <NuxtLink to="/features" class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Features</NuxtLink>
          <NuxtLink to="/how-it-works" class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">How It Works</NuxtLink>
          <NuxtLink to="/tools" class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Tools</NuxtLink>
        </ul>
      </nav>
     <div class="flex items-center space-x-3">
      <a href="#">
        <button class="bg-[#AB3ADD] rounded-full text-white px-4 sm:py-3 py-2">Affiliate Link</button>
      </a>

      <button class="togglebtn" @click="toggleMobileNav">
      <template v-if="!mobileNavOpen">
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="#141414" viewBox="0 0 256 256"><path d="M224,128a8,8,0,0,1-8,8H40a8,8,0,0,1,0-16H216A8,8,0,0,1,224,128ZM40,72H216a8,8,0,0,0,0-16H40a8,8,0,0,0,0,16ZM216,184H40a8,8,0,0,0,0,16H216a8,8,0,0,0,0-16Z"></path></svg>
      </template>
      <template v-else>
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="#141414" viewBox="0 0 256 256"><path d="M205.66,194.34a8,8,0,0,1-11.32,11.32L128,139.31,61.66,205.66a8,8,0,0,1-11.32-11.32L116.69,128,50.34,61.66A8,8,0,0,1,61.66,50.34L128,116.69l66.34-66.35a8,8,0,0,1,11.32,11.32L139.31,128Z"></path></svg>
      </template>
    </button>
     </div>
    </div>

    <transition name="slide-fade" mode="out-in">
    <aside class="nav-mobile" v-if="mobileNavOpen" key="mobileNav">
      <div class="mb-12">
        <img class="w-[120px]" src="/icons/logo.svg" alt="agency_ai_logo">
      </div>
      <nav>
        <ul class="header_one flex items-start flex-col space-y-6">
          <a href="#"><li class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Products</li></a>
          <a href="#"><li class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Features</li></a>
          <a href="#"><li class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">How It Works</li></a>
          <a href="#"><li class="border-b-2 border-transparent hover:border-b-2 hover:border-[#AB3ADD] hover:text-[#AB3ADD] transition duration-300">Tools</li></a>
        </ul>
      </nav>
    </aside>
  </transition>
  </header>
</template>



<script setup>
import { ref, onMounted } from 'vue';

const isScrolled = ref(false);
const mobileNavOpen = ref(false);

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

const toggleMobileNav = () => {
  console.log('hgjgh')
  mobileNavOpen.value = !mobileNavOpen.value;
};
</script>

<style scoped>
.nav-mobile { display: none;}
.togglebtn { display: none;}

.slide-fade-enter-active, .slide-fade-leave-active {
  transition: opacity 0.5s, transform 0.5s;
}
.slide-fade-enter, .slide-fade-leave-to {
  opacity: 0;
  transform: translateX(-20px);
}

.header_one > a.router-link-active {
  border-bottom: 2px solid #AB3ADD;
  color: #AB3ADD
}

 @media screen and (max-width: 767px) {
  .nav-desktop { display: none;}
  .nav-mobile { display: block; background: #ffffff; padding: 20px 30px; position: fixed; top: 0; left: 0; width: 300px; height: 100%; box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px; }
  .togglebtn { display: block;}
 }
</style>