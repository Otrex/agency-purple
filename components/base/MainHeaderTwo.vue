<template>
    <header
     :class="{ 'shadow-md bg-white': isScrolled }"
     class="sticky relative top-0 w-full py-4 bg-transparent z-50 lg:px-[80px] px-[16px]"
   >
     <div class="max-w-[1200px] mx-auto w-full flex items-center justify-between">
       <div>
         <img class="sm:w-[200px] w-[120px]" :src="isScrolled ? '/icons/logo.svg' : '/icons/footer_logo.svg'" alt="agency_ai_logo">
       </div>
       <nav class="nav-desktop">
         <ul :class="`header_two flex items-center lg:space-x-8 space-x-4 ${isScrolled ? 'text-[#AC3BDE]' : 'text-[#fff]'}`">
           <NuxtLink href="#quote" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300" :class="{ active: isActive('#quote') }">Quote</NuxtLink>
           <NuxtLink href="#our-services" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300" :class="{ active: isActive('#our-services') }">Our Services</NuxtLink>
           <NuxtLink href="#about-us" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300" :class="{ active: isActive('#about-us') }" >About Us</NuxtLink>
           <NuxtLink href="#testimonials" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300" :class="{ active: isActive('#testimonials') }">Testimonials</NuxtLink>
         </ul>
       </nav>
      <div class="flex items-center space-x-3">
       <a href="#">
         <button class="bg-[#2C093B] sm:text-[16px] text-[13px] rounded-full text-white px-4 sm:py-3 py-2">Contact Us</button>
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
         <img class="w-[120px]" src="/icons/footer_logo.svg" alt="agency_ai_logo">
       </div>
       <nav>
         <ul class="header_two flex items-start flex-col space-y-6 text-[#fff]">
           <NuxtLink @click="mobileNavOpen = false" to="#quote" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300">Quote</NuxtLink>
           <NuxtLink @click="mobileNavOpen = false" to="#our-services" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300">Our Services</NuxtLink>
           <NuxtLink @click="mobileNavOpen = false" to="#about-us" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300">About Us</NuxtLink>
           <NuxtLink @click="mobileNavOpen = false" to="#testimonials" class="border-b-2 border-transparent hover:text-[#2C093B] transition duration-300">Testimonials</NuxtLink>
         </ul>
       </nav>
     </aside>
   </transition>
   </header>
 </template>
 
 
 
 <script setup lang="ts">
 import { ref, onMounted } from 'vue';
 
 const isScrolled = ref(false);
 const mobileNavOpen = ref(false);
 const route = useRoute as any
 
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

 const isActive = (section: string) => {
  const currentHash = route.hash;
  return currentHash === section;
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
 
 .header_two  > .active {
  border-radius: 100px;
   color: #AC3BDE;
   background: #E19CFF;
   padding: 8px 16px;
 }
 
  @media screen and (max-width: 767px) {
   .nav-desktop { display: none;}
   .nav-mobile { display: block; background: #2C093B; padding: 20px 30px; position: fixed; top: 0; left: 0; width: 300px; height: 100%; box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px; }
   .togglebtn { display: block;}
   .header_two  > .active {
   color: #fff !important;
   font-weight: 700;
 }
  }
 </style>