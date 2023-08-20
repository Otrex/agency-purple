

<template>
  <section class="d-container" id="benefits">
        <div>
          <h1
            :class="`relative sm:pb-[70px] pb-[35px] lg:text-[48px] sm:text-[32px] text-[26px] font-bold text-center ${headerTextColor || 'text-[#333]'}`"
          >
            Benefits of {{ data?.agency_wizard.website_details.agencyName}} <br />
            Services
          </h1>

          <div
            class="flex sm:flex-row flex-col sm:space-x-5 space-x-0 sm:space-y-0 space-y-5"
          >
            <div class="border-2 sm:p-[30px] p-[14px] rounded-[20px]">
              <div
                v-for="(text, i) in benefits.one"
                :key="i"
                class="mx-w-[300px] w-full"
              >
                <h1
                  class="sm:text-[20px] text-[16px] sm:pt-[30px] pt-[10px] pb-2 font-bold text-[#3B57F4]"
                >
                  {{ text.name }}
                </h1>
                <p class="sm:text-[16px] text-[14px]">{{ text.description }}</p>
              </div>
            </div>
            <div class="border-2 sm:p-[30px] p-[14px] rounded-[20px]">
              <div
                v-for="(text, i) in benefits.two"
                :key="i"
                class="mx-w-[300px] w-full"
              >
                <h1
                  class="sm:text-[20px] text-[16px] sm:pt-[30px] pt-[10px] pb-2 font-bold text-[#3B57F4]"
                >
                  {{ text.name }}
                </h1>
                <p class="sm:text-[16px] text-[14px]">{{ text.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>

<script setup lang="ts">
import { ServiceBenefit, WizardResponse } from "../../type";

const props = defineProps<{
  data?: WizardResponse, 
  headerTextColor: string
}>();

const benefits = computed(() =>  {
  const arr = props.data?.agency_wizard.service_benefits || []
  const half = Math.ceil(arr.length/2);

  const arr1:ServiceBenefit[] = [];
  const arr2:ServiceBenefit[] = [];

  arr.forEach((el, i) => {
    if (i >= half) {
      arr2.push(el);
      return;
    }
    arr1.push(el);
  })

  return {one: arr1, two: arr2, half}
})


const benefitsOne = ref([
  {
    header: "Expertise",
    desc: "Our seasoned professionals bring 15years+ of industry experience to the table.",
  },
  {
    header: "Tailored Solutions",
    desc: "We customize unique business strategies to meet your unique business goals.",
  },
  {
    header: "Comprehensive Services",
    desc: "We cover all your online marketing assets needs like Sales copies, video scripts, Youtube channel scripts, in one place in .",
  },
  {
    header: "Cutting-edge Strategies",
    desc: "We stay ahead with the latest trends and technologies.",
  },
  {
    header: "Increased Visibility",
    desc: "We boost your brand's online presence, help you reach a wider audience and ensure that you stay profitable.",
  },
]);
const benefitsTwo = ref([
  {
    header: "Targeted Engagement",
    desc: "With our unique voice, we connect with your audience, driving loyalty and relationships from your customers so they keep coming back.",
  },
  {
    header: "Compelling Content",
    desc: "Our skilled writers create captivating content that resonates with your customers .",
  },
  {
    header: "Result Driven",
    desc: "We focus on achieving tangible outcomes and continuously optimize.",
  },
  {
    header: "Time and Cost Efficiency",
    desc: "Outsource your Content Marketing to us, let's save you time and resources.",
  },
  {
    header: "Long-Term Partnership",
    desc: "We aim to become your trusted long-term marketing partner.",
  },
]);
</script>

<style scoped></style>
