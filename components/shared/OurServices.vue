<template>
  <main class="d-container">
    <section id="our-services">
        <h1
          :class="`relative ${titleColor} sm:pb-[70px] pb-[35px] lg:text-[48px] sm:text-[32px] text-[26px] font-bold text-center`"
        >
          Our Services
        </h1>
        <div
          :class="`text-wrapper grid lg:grid-cols-3 sm:grid-cols-2 grid-cols-1 sm:gap-x-[60px] gap-x-[10px] sm:gap-y-[80px] gap-y-[40px]`"
        >
          <div
            v-for="(service, i) in ourServices"
            :key="i"
            class="mx-w-[300px] w-full"
          >
            <img
              class="w-full rounded-t-[10px] mx-auto"
              :src="service.icon"
              alt="icon"
            />
            <h1
              :class="`sm:text-[20px] text-[16px] sm:pt-[30px] pt-[10px] ${headerTextColor} pb-2 font-bold`"
            >
              {{ service.header }}
            </h1>
            <p class="sm:text-[16px] text-[14px]">{{ service.desc }}</p>
          </div>
        </div>
        <div
          class="flex flex-col items-center justify-center w-full sm:mb-[200px] mb-[50px] sm:mt-[100px] mt-[25px]"
        >
          <button
            class="mx-auto border border-black text-black bg-white px-4 py-3 rounded-[10px] font-bold"
          >
            And Others
          </button>
          <button
            class="mx-auto mt-[38px] text-[#fff] bg-[#AB3ADD] px-[50px] py-3 rounded-[133px]"
          >
            Lets Talk
          </button>
        </div>
      </section>
  </main>
</template>

<script setup lang="ts">
defineProps({
  headerTextColor: {
    type: String,
    default: 'text-[#333]'
  },
  titleColor: {
    type: String,
    default: 'text-[#333]'
  }
})
const ourServices = ref([
  {
    header: "Copywriting",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img1.svg",
  },
  {
    header: "Scriptwriting",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img2.svg",
  },
  {
    header: "SEO",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img3.svg",
  },
  {
    header: "Social Media Marketing and Management",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img4.svg",
  },
  {
    header: "Business Development and Consulting Agency",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img5.svg",
  },
  {
    header: "Email Marketing Services",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img6.svg",
  },
  {
    header: "Branding Services",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img3.svg",
  },
  {
    header: "Research & Development Service",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img8.svg",
  },
  {
    header: "Content Creation Services",
    desc: "At [COMPANY NAME], we understand that navigating the complexities of the digital age can be daunting.",
    icon: "/icons/services_img9.svg",
  },
]);
</script>

<style scoped></style>