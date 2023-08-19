<template>
  <main id="quote">
    <section
      class="op-hero xl:pt-[130px] lg:pt-[140px] md:pt-[120px] pt-[115px] -mt-[80px]"
    >
      <div
        class="font_jakarta max-w-[1200px] mx-auto xl:px-[10px] lg:px-[60px] md:px-[24px] sm:px-[80px] pb-[200px]"
      >
        <div class="w-full grid md:grid-cols-2 items-center">
          <div class="md:text-left text-center px-[20px]">
            <h2
              class="font-[800] capitalize xl:text-[50px] lg:text-[40px] sm:text-[30px] text-[24px] text-[#3B57F4] mb-[24px]"
            >
              Unleash Your Brand Potential WIth Marketing Done Right
            </h2>
            <p
              class="font-[400] xl:text-[28px] lg:text-[24px] smtext-[20px] text-[16px] text-[#232323] leading-[-1.4px]"
            >
              Leverage our Exceptional Services to boost your Online Business
              growth.
            </p>
            <button
              class="md:mt-[48px] mt-[60px] xl:mb-[120px] lg:mb-[260px] md:mb-[150px] rounded-full md:px-[60px] px-[40px] md:py-[22px] py-[18px] bg-[#3B57F4] text-[20px] text-[#fff]"
            >
              Get Started
            </button>
          </div>
          <div class="md:order-2 order-1">
            <img
              class="w-full"
              src="/images/hero_img_3.png"
              alt="illustration"
            />
          </div>
        </div>
      </div>
    </section>
  <div class=" relative bg-gradient-to-b from-[#F0F3FF] to-[#fff]">
      <Type2QuoteT2 />
    </div>
  </main>
</template>

<script setup lang="ts"></script>

<style scoped>
.op-hero {
  background: #f0f3ff;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  max-height: 150vh;
  height: 100%;
}
</style>
