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
            :class="`lg:text-[60px] text-[32px] font-bold pb-3 capitalize ${headerTextColor}`"
          >
            About Us
          </h1>
          <p class="sm:text-[16px] text-[14px] pb-3">
            [COMPANY NAME] is the leading provider of comprehensive online marketing
            solutions. We are passionate about helping businesses like yours
            thrive in the digital landscape. With our expertise and dedication,
            we are your trusted partner for all your online marketing needs.
          </p>
          <p class="sm:text-[16px] text-[14px] pb-3">
            We offer a comprehensive suite of services to cover every aspect of
            your online marketing requirements. From business consulting and
            strategy development to social media management, content creation,
            email marketing, video script writing, Sales copies, Business
            Proposals, persuasive copywriting and so much more – we have the
            expertise and capabilities to elevate your brand's online presence
            and drive tangible results.
          </p>
          <p class="sm:text-[16px] text-[14px] pb-3">
            We invite you to experience the power of [COMPANY NAME] and unlock your
            business's full potential in the digital landscape.
          </p>
          <p class="sm:text-[16px] text-[14px] pb-3">
            Contact us today to take your online marketing to new heights and
            embark on a journey of success.
          </p>
          <button
            :class="`py-3 px-6 ${buttonBg} rounded-full text-white mt-[20px]`"
          >
            Contact Us
          </button>
        </div>
      </div>
    </section>
</template>

<script setup lang="ts">
defineProps ({
  headerTextColor: {
    type: String,
    default: 'text-[#333]'
  },
  buttonBg: {
    type: String,
    default: 'bg-[#333]'
  },
  image: {
    type: String,
    default: ''
  },
  showEclipse: {
    type: Boolean,
    default: false
  },
  bgColor: {
    type: String,
    default: ""
  }
})
</script>

<style>

</style>