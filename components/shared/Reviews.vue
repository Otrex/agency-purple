<template>
  <main id="testimonials" class="lg:py-[160px] md:py-[100px] py-[50px]">
    <div class="d-container">
        <div class="md:w-[80%] w-[90%] mx-auto">
            <h3 :class="`text-center lg:text-[64px] md:text-[50px] text-[40px] ${headerTextColor} font-[700]`">What Our Partners Are saying</h3>
        </div>
        <div class="grid md:grid-cols-2 lg:mt-[150px] md:mt-[75px] mt-[50px]">
          <div class="mb-[20px] mr-[20px] relative text-left border border-[#D9D9D9] md:px-[45px] px-[32px] md:py-[34px] py-[24px] rounded-[20px] flex flex-col items-start justify-start">
            <p class="#000 md:text-[24px] text-[20px]">"[COMPANY NAME] transformed our online presence, delivering exceptional results. Highly recommended!"</p>
            <div class="flex items-center md:mt-[38px] mt-[24px]">
              <img class="w-[64px] h-[64px] rounded-[64px]" src="/images/dummy_user.png" alt="user">
              <div class="text-left ml-[16px]">
                <p class="#000 text-[24px] font-[700] mb-[4px]">- John D.</p>
                <p>CEO, Tizz Company</p>
              </div>
            </div>
          </div>
          <div class="mb-[20px] mr-[20px] relative text-left border border-[#D9D9D9] md:px-[45px] px-[32px] md:py-[34px] py-[24px] rounded-[20px] flex flex-col items-start justify-start">
            <p class="#000 md:text-[24px] text-[20px]">"[COMPANY NAME] transformed our online presence, delivering exceptional results. Highly recommended!"</p>
            <div class="flex items-center md:mt-[38px] mt-[24px]">
              <img class="w-[64px] h-[64px] rounded-[64px]" src="/images/dummy_user.png" alt="user">
              <div class="text-left ml-[16px]">
                <p class="#000 text-[24px] font-[700] mb-[4px]">- John D.</p>
                <p>CEO, Tizz Company</p>
              </div>
            </div>
          </div>
          <div class="mb-[20px] mr-[20px] relative text-left border border-[#D9D9D9] md:px-[45px] px-[32px] md:py-[34px] py-[24px] rounded-[20px] flex flex-col items-start justify-start">
            <p class="#000 md:text-[24px] text-[20px]">"[COMPANY NAME] transformed our online presence, delivering exceptional results. Highly recommended!"</p>
            <div class="flex items-center md:mt-[38px] mt-[24px]">
              <img class="w-[64px] h-[64px] rounded-[64px]" src="/images/dummy_user.png" alt="user">
              <div class="text-left ml-[16px]">
                <p class="#000 text-[24px] font-[700] mb-[4px]">- John D.</p>
                <p>CEO, Tizz Company</p>
              </div>
            </div>
          </div>
          <div class="mb-[20px] mr-[20px] relative text-left border border-[#D9D9D9] md:px-[45px] px-[32px] md:py-[34px] py-[24px] rounded-[20px] flex flex-col items-start justify-start">
            <p class="#000 md:text-[24px] text-[20px]">"[COMPANY NAME] transformed our online presence, delivering exceptional results. Highly recommended!"</p>
            <div class="flex items-center md:mt-[38px] mt-[24px]">
              <img class="w-[64px] h-[64px] rounded-[64px]" src="/images/dummy_user.png" alt="user">
              <div class="text-left ml-[16px]">
                <p class="#000 text-[24px] font-[700] mb-[4px]">- John D.</p>
                <p>CEO, Tizz Company</p>
              </div>
            </div>
          </div>
        </div>
    </div>
  </main>
</template>

<script setup lang="ts">
defineProps({
  headerTextColor: {
    type: String,
    default: "text-[#333]"
  }
})
</script>

<style scoped>
.purp_grad_text {
  color: linear-gradient(165deg, #AB3ADD 0%, #3B57F4 100%) !important
}
</style>