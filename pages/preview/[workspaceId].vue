<template>
  <transition name="fade" mode="out-in"> 
    <div class="w-full h-screen flex items-center justify-center" v-if="!state">
      <div> Loading.... </div>
    </div>
    <main v-else>
      <BaseMainHeaderTwo 
        :data="state"/>
      <Type1HeroT1 
        :data="state" />
      <Type1HelpYouT1 
        :data="state" />
      <SharedOurServices 
        :data="state"
        :header-text-color="'bg-clip-text text-transparent bg-gradient-to-b from-[#AB3ADD] via-[#AB3ADD] to-[#3B57F4]'"
        titleColor="text-[#3B57F4]"
      />
      <SharedBenefits
        :data="state"
        :header-text-color="'bg-clip-text text-transparent bg-gradient-to-b from-[#AB3ADD] via-[#AB3ADD] to-[#3B57F4]'"
      />
      <SharedAboutUs
        :data="state"
        showEclipse
        bgColor="bg-[#F5F7FF]"
        :image="'/images/about_team.png'"
        :header-text-color="'bg-clip-text text-transparent bg-gradient-to-b from-[#AB3ADD] via-[#AB3ADD] to-[#3B57F4]'"
        :button-bg="'bg-[#AB3ADD]'"
      />
      <SharedReviews 
        :data="state" 
        :header-text-color="'text-[#AB3ADD]'" />
      <BaseMainFooter 
        :data="state" 
      />
    </main>
  </transition>
</template>

<script setup lang="ts">
definePageMeta({
  layout: false,
});

import axios from "axios";
import { WizardResponse } from "../../type";

const state = ref<WizardResponse>();
const config = useRuntimeConfig();
const route = useRoute();

onBeforeMount(async () => {
  try {
    const result = await axios.get(`${config.public.baseURL}/d/${route.params.workspaceId}/wizard`);
    const data = result.data as WizardResponse;
    state.value = data;
  } catch (error) {
    navigateTo("/")
  }
})

useHead(() => ({
  title: state.value?.agency_wizard.seo.title || "Welcome to Agency Pages",
  link: [ 
    { 
      rel: "icon", 
      type: "image/png", 
      href: state.value?.agency_wizard.website_details.favIcon 
    } 
  ],
  script: [
    { 
      innerHTML: state.value?.agency_wizard.website_details.customJavascript || 'null', 
      type: "text/javascript" 
    },
  ]
}))

</script>

<style></style>
