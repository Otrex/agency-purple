<template>
  <main class="ate-wrapper py-[80px]">
    <div class="d-container">
      <SharedLaunchingInfo />
      <SharedTicketForm />
      <div class="pt-[250px] lg:w-[80%] mx-auto"> 
        <div class="flex items-center justify-center my-[60px]">
            <img src="/icons/need_anything_text.svg" alt="">
        </div>
        <div class="flex md:flex-row flex-col items-center justify-center">
            <img src="/icons/godswillO.svg" alt="Godswill photo">
            <div class="g-info-box px-[50px] py-[30px] md:mt-[0] mt-[20px]">
                <p class="text-[#333] font-[700] text-[24px]">Goodwill Okoyomon</p>
                <div class="mt-[20px] mx-[20px] flex items-center justify-between">
                    <div class="flex items-center"><img class="mr-[8px]" src="/icons/email_icon.svg" alt="email">Email</div>
                    <div class="flex items-center"><img class="mr-[8px]" src="/icons/skype_icon.svg" alt="skype">Skype</div>
                </div>
            </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup></script>

<style scoped>
.ate-wrapper {
  background: url("/icons/design_pattern_one.svg");
}
.g-info-box {
    border-radius: 10px;
background: linear-gradient(226deg, #FFF 0%, rgba(255, 255, 255, 0.00) 100%);
}
</style>
