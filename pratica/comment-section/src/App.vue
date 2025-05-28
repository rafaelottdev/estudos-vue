<template>
  <HeaderSection />

  <MainSection />
</template>

<script>
  import HeaderSection from "./components/HeaderSection.vue"
  import MainSection from "./components/MainSection.vue"

  export default {
    name: "App",
    components: {
      HeaderSection, MainSection
    }
  }
</script>
