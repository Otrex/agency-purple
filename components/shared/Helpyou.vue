<template>
  <div class="relative mt-[200px]">
    <div class="sm:pt-[200px] pt-[30px] sm:pb-[80px] pb-[50px]">
      <section
        class="md:pr-[0px] pr-[16px] xl:pl-[115px] lg:pl-[80px] md:pl-[40px] pl-[16px]"
      >
        <div class="sm:pt-[0] pt-[50px]">
          <h1
            :class="`relative capitalize sm:pt-[40px] pt-[0px] sm:pb-[70px] pb-[35px] lg:text-[48px] sm:text-[32px] text-[26px] font-bold text-center bg-clip-text text-[${headerTextColor}]`"
          >
            How can we <span :class="helpTextColor ? `text-[${helpTextColor}]` : `text-[${headerTextColor}]`">help</span> you
          </h1>
          <div
            class="flex sm:flex-row flex-col sm:space-y-0 space-y-6 space-x-[20px] lg:pb-[50px] sm:pb-[50px] pb-[40px]"
          >
            <div class="lg:w-[50%] md:w-[65%] w-[100%]">
              <h1
                :class="`lg:text-[48px] text-[${introTextColor}] sm:text-[32px] text-[20px] font-bold pb-[32px]`"
              >
                Empowering Your Digital Success with [COMPANY NAME]: Expert
                Solutions for the Digital Age.
              </h1>
              <p class="sm:text-[16px] text-[14px] pb-3">
                At [COMPANY NAME], we understand that navigating the
                complexities of the digital age can be daunting. That's why our
                team of experts is dedicated to helping you succeed. Whether
                yo're a small business owner, an entrepreneur, or a busy
                professional, we offer a wide range of services that cover every
                aspect of your online presence.
              </p>
              <p class="sm:text-[16px] text-[14px] pb-3">
                With our in-depth understanding of the online market, we create
                stunning and high-converting Sales copies, Video Scripts, blog
                post creation, Ads campaign copies, business proposals and so
                much more that captures attention, drives engagement for your
                business, and aligns with your brand messaging. We employ
                conversion-focused strategies, utilizing persuasive content,
                call-to-actions, and conversion tracking to drive desired
                actions and boost sales for your business.
              </p>
              <p class="sm:text-[16px] text-[14px] pb-3">
                Choose [COMPANY NAME] as your trusted partner for exceptional
                online marketing assets. Contact us today and experience the
                comprehensive solutions that will propel your business to new
                heights.
              </p>
              <button
                :class="`py-3 px-6 bg-[${buttonBg}] rounded-full text-white mt-[20px]`"
              >
                Contact Us
              </button>
            </div>
            <div class="md:w-[50%] w-[100%] relative">
              <img
                class="w-full"
                :src="image"
                alt="illustration"
              />
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  image: {
    type: String,
    default: ""
  },
  buttonBg: {
    type: String,
    default: "#000"
  },
  headerTextColor: {
    type: String,
    default: "#000"
  },
  introTextColor: {
    type: String,
    default: "#000"
  },
  helpTextColor: {
    type: String,
    default: ""
  },
})
</script>

<style scoped></style>
