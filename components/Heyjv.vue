<template>
  <div class="wrapper relative">
    <img class="w-full absolute top-0 left-0" src="/icons/Bubbles.svg" alt="">
    <img class="w-full absolute top-0 right-0" src="/icons/Hey_ellipse.svg" alt="">
    <div class="d-container sm:pt-[95px] pt-[30px] sm:pb-[115px] pb-[50px]">
        <img class="sm:max-w-[300px] max-w-[200px] mx-auto" src="/icons/Hey_jv.svg" alt="">
        <h1 class="lg:text-[60px] sm:text-[40px] text-[20px] font-bold text-center sm:pt-[60px] pt-[20px] pb-[10px]">The Artificial Intelligence (AI) + <br/> Agency Takeover is Here!</h1>
        <img class="sm:max-w-[300px] max-w-[100px] mx-auto lg:pb-[140px] sm:pb-[80px] pb-[30px]" src="/icons/underline_artwork.svg" alt="">

        <div class="flex sm:flex-row flex-col sm:space-y-0 space-y-6 sm:space-x-[100px] space-x-[40x]">
            <div class="lg:max-w-[400px] sm:max-w-[300px] sm:max-w-[90%]">
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">2023 is for Artificial Intelligence… while the year 2000 was for Google.</p>
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">Artificial Intelligence (AI) has completely transformed the way businesses operate & connect with their customers.</p>
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">Business owners want everything done at the snap of their fingers.</p>
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">They want quick & easy solutions that can keep up with the constantly changing online trends.</p>
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">And their customers demand nothing less too.</p>
                <p class="sm:text-[18px] text-[14px] opacity-80 pb-3">This means businesses need fresh content and other online assets  every week, and they need it fast</p>
                <p class="sm:text-[18px] text-[14px] text-bold">Aside the Trend of AI - Agency Positioning has been the Most Popular and Hottest Product Niche in the Market for a Long Time...</p>
            </div>
            <div class="sm:max-w-[420px] max-w-[100%] relative">
                <img class="w-full" src="/icons/Heyjs_sbg_one.svg" alt="">
            </div>
        </div>

        <article>
            <h1 class="sm:pt-[151px] pt-[60px] sm:pb-[66px] pb-[30px] lg:text-[48px] sm:text-[32px] text-[18px] font-bold text-center">AI & Small Businesses are <br/> Shaping the Future</h1>
            <div class="text-wrapper flex lg:flex-row flex-col">
                <div v-for="(text, i) in textContent" :key="i" class="bg-[#4359D6]">
                    <h1 class="lg:text-[40px] sm:text-[32px] text-[18px] bold pb-2">{{ text.header }}</h1>
                    <p class="sm:text-[16px] text-[14px]">{{ text.desc }}</p>
                </div>
            </div>
            <div class="lg:pt-[135px] sm:pt-[80px] pt-[40px] pb-[40px] mx-auto sm:max-w-[80%] max-w-[100%]">
                <img src="/icons/Hey_step.svg" alt="">
            </div>
            <div class="sm:max-w-[300px] max-w-[150px] sm:pb-[40px] pb-[16px] mx-auto">
                <img src="/icons/Hey_robot.svg" alt="">
            </div>
        </article>
    </div>
  </div>
</template>

<script setup lang="ts">
    const textContent = ref([
        {header:'$15.7 Trillion', desc:'The expected amount AI would contribute to the global Economy by 2030, more than the current output of China and India combined. (Forbes)'},
        {header:'80%', desc:'Industry experts integrate some form of AI technology into their online marketing activities. (HubSpot)'},
        {header:'88%', desc:'Of marketers believe their organization must increase its use of automation and AI to meet customer expectations and stay competitive (Mailchimp 2023)'},
        {header:'61.4%', desc:'Of marketers believe their organization must increase its use of automation and AI to meet customer expectations and stay competitive (Mailchimp 2023)'},
        {header:'50%', desc:'Of marketers believe inadequate AI adoption is holding them back from achieving their goals. (Mailchimp 2023)'},
    ])

</script>

<style scoped>
.wrapper {
  background: linear-gradient(165deg, #380251 0%, #331042 100%); color:#fff;
}
.text-wrapper > div {
    padding: 30px 15px;
    max-width: 400px;
}
.text-wrapper > div:nth-of-type(1) {
    background: #293272;
    margin-right: 20px;
}

@media screen and  (max-width: 1024px) {
    .text-wrapper > div {
    padding: 30px 15px;
    max-width: 100%;
 }
 .text-wrapper > div:nth-of-type(1) {
    margin-right: 0 ;
    margin-bottom: 16px;
 }
}
@media screen and  (max-width: 767px) {
    .text-wrapper > div {
    padding: 20px 10px;
 }

}

</style>