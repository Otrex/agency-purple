

<template>
  <section
      id="about-us"
      :class="`relative ${bgColor} lg:py-[180px] sm:py-[70px] py-[35px] mt-[80px]`"
    >
    <img v-if="showEclipse" class="absolute top-0 left-0" src="/icons/left_eclipse.svg" alt="illus">
      <div
        class="d-container flex justify-between sm:flex-row flex-col-reverse space-x-[30px] sm:space-y-0 space-y-6"
      >
        <div class="lg:w-[50%] md:w-[30%] w-[100%] relative">
          <img
            class="w-full"
            :src="image"
            alt="illustration"
          />
        </div>
        <div class="lg:w-[50%] md:w-[70%] w-[100%]">
          <h1
            :class="`lg:text-[60px] text-[32px] font-bold pb-3 capitalize ${headerTextColor || 'text-[#333]' }`"
          >
            About Us
          </h1>
          <p v-html="data?.agency_wizard.contact.about.about_desc" class="sm:text-[16px] text-[14px] pb-3">
            
          </p>
          <button
            :class="`py-3 px-6 ${buttonBg || 'bg-[#333]'} rounded-full text-white mt-[20px]`"
          >
            Contact Us
          </button>
        </div>
      </div>
    </section>
</template>

<script setup lang="ts">
import { WizardResponse } from "../../type";
defineProps<{
  data?: WizardResponse, 
  headerTextColor: string, 
  buttonBg: string, 
  image: string, 
  showEclipse?: boolean,
  bgColor: string,
}>();
</script>

<style>

</style>