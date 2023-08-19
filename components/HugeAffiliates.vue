<template>
  <main class="mt-[36px] mb-[107px]">
    <div class="d-container">
      <div class="text-center">
        <h3 class="ht-header lg:text-[72px] md:text-[65px] text-[40px] font-[700] leading-[99px]">
          Huge Affiliate Resources
        </h3>
        <p class="text-[#000] md:text-[30px] text-[20px] mt-[34px] leading-[41px]">
          We have Put together a Comprehensive list of Affiliate Resources to
          provide everything single thing you need to make this a successful
          Promotion
        </p>
      </div>

      <div class="mt-[93px] flex items-start justify-center flex-wrap">
        <div
          v-for="(affiliateResource, i) in affiliateResources"
          :key="i"
          class=""
        >
          <div
            class="aff-resource-card px-[24px] py-[29px] mr-[24px] mb-[58px]"
          >
            <img :src="affiliateResource.icon" alt="resource icon" />
            <h6 class="mt-[30px] text-[#3B57F4] text-[26px]">
              {{ affiliateResource.name }}
            </h6>
            <div class="h-[100px]">
              <p class="mt-[17px] text-[16px]">{{ affiliateResource.desc }}</p>
            </div>
            <button class="mt-[15px] action-layout capitalize" :class="affiliateResource.action === 'view' ? 'view-action bg-[#d8deff]' : 'download-action bg-[#3B57F4]'">
              <img v-if="affiliateResource.action === 'view'" src="/icons/view_icon.svg" alt="view icon">
              {{ affiliateResource.action }}
              <img class="w-[24px]" v-if="affiliateResource.action === 'download'" src="/icons/download-white.svg" alt="download icon">
            </button>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
const affiliateResources = ref([
  {
    name: "Email Swipes",
    desc: "Use our high converting email swipes to make sure your promotion pops off!",
    icon: "/icons/email_swipes.svg",
    action: "view",
  },
  {
    name: "Graphics",
    desc: "Use our professionally designed graphics in your promos for your websites and ads.",
    icon: "/icons/graphics_icon.svg",
    action: "view",
  },
  {
    name: "JV Launch Sheet",
    desc: "See the entire Launch Info at a glance with our JV Launch Sheet",
    icon: "/icons/jv_launch_sheet.svg",
    action: "download",
  },
  {
    name: "PDF Report",
    desc: "Use our high converting email swipes to make sure your promotion pops off!",
    icon: "/icons/pdf_report.svg",
    action: "download",
  },
  {
    name: "Bonuses",
    desc: "Use our professionally designed graphics in your promos for your websites and ads.",
    icon: "/icons/bonuses.svg",
    action: "download",
  },
]);
</script>

<style scoped>
.ht-header {
  background: linear-gradient(90deg, #ab3add 0%, #3b57f4 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.aff-resource-card {
  border-radius: 20px;
  background: #f8f8f8;
  width: 100%;
  max-width: 280px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.action-layout {
  width: 100%;
  display: flex;
  padding: 12px 27px;
  justify-content: center;
  align-items: center;
  gap: 5.606px;
  border-radius: 41.488px;
}
.view-action {
  color: #3b57f4;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 11.431px;
  letter-spacing: -0.5px;
}
.download-action {
  color: #fff;
  font-size: 20px;
  font-weight: 500;
  line-height: 11.431px;
  letter-spacing: -0.5px;
}
</style>
