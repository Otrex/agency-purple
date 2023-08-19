<template>
    <div class="relative mt-[50px]">
      <div class="sm:pt-[50px] pt-[30px] sm:pb-[80px] pb-[50px]">
        <section
          class="md:pr-[0px] pr-[16px] xl:pl-[115px] lg:pl-[80px] md:pl-[40px] pl-[16px]"
        >
          <div class="sm:pt-[0] pt-[50px]">
            <h1
              :class="`relative capitalize sm:pt-[40px] pt-[0px] sm:pb-[70px] pb-[35px] lg:text-[48px] sm:text-[32px] text-[26px] font-bold text-center bg-clip-text text-[#AB3ADD]`"
            >
              How can we help you
            </h1>
            <div
              class="flex sm:flex-row flex-col sm:space-y-0 space-y-6 space-x-[20px] lg:pb-[50px] sm:pb-[50px] pb-[40px]"
            >
              <div class="lg:w-[50%] md:w-[65%] w-[100%]">
                <h1
                  :class="`lg:text-[48px] text-[#333] sm:text-[32px] text-[20px] font-bold pb-[32px]`"
                >
                  {{ data?.agency_wizard.contact.help.help_headline || 'Empowering Your Digital Success with [COMPANY NAME]: Expert Solutions for the Digital Age.'}}
                </h1>
                <p v-html="data?.agency_wizard.contact.help.help_desc" class="sm:text-[16px] text-[14px] pb-3"></p>
                <button
                  :class="`py-3 px-6 bg-[#AB3ADD] rounded-full text-white mt-[20px]`"
                >
                  Contact Us
                </button>
              </div>
              <div class="md:w-[50%] w-[100%] relative">
                <img
                  class="w-full"
                  src="/images/smiling_help_lady.png"
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
  import { WizardResponse } from '../../type';

defineProps<{ data?: WizardResponse }>();
  </script>
  
  <style scoped></style>
  