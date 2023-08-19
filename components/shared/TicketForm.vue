<template>
  <div>
    <article class="b-box md:pt-[62px] pt-[40px] md:pb-[52px] pb-[30px]">
      <div class="flex flex-col items-center justify-center">
        <p class="text-center flex items-center justify-center">
          <span>Get Your</span>
          <img class="mx-[5px]" src="/images/nzoo.png" alt="nzoo" />
          <span>Affiliate Links</span>
        </p>
        <form
          class="my-[32px] md:mx-[0] mx-[16px] flex items-center justify-center"
        >
          <div class="bg-[#fff] rounded-full pl-[20px] flex items-center justify-between">
            <img class="mr-[10px]" src="/icons/mail.svg" alt="mail icon" />
            <input type="text" class="m:w-auto w-[45%] bg-transparent" />
            <button
              type="submit"
              class="purple-bg-btn md:text-[18px] text-[14px] text-[#fff] md:px-[20px] px-[14px] md:py-[14px] py-[10px] self-end"
            >
              Get Affilliate Link
            </button>
          </div>
        </form>
        <button
          class="yellow-bg-btn md:text-[24px] text-[18px] flex items-center"
        >
          <img
            class="mr-[10px]"
            src="/icons/download.svg"
            alt="download icon"
          />
          Grab Your Promo Tools
        </button>
      </div>
    </article>
  </div>
</template>

<script setup></script>

<style scoped>
.yellow-bg-btn {
  border-radius: 74px;
  background: #ffbb38;
  box-shadow: 0px 16px 80px 0px rgba(255, 194, 54, 0.6);
  color: #201f20;
  padding: 14px 24px;
}
.b-box {
  border-radius: 24px;
  background: #e3e7fe70;
}
.purple-bg-btn {
  border-radius: 132.338px;
  background: #ab3add;
}
</style>
