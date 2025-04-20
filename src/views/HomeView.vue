<script setup>
import AboutSection from '@/components/AboutSection.vue'
import ExperienceSection from '@/components/ExperienceSection.vue'
import HeaderSection from '@/components/HeaderSection.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
</script>

<template>
  <div
    class="bg-[#101010] text-white mx-auto max-w-screen-xl px-6 md:px-12 lg:px-16 min-h-svh p-px body"
  >
    <div class="lg:flex lg:justify-between lg:gap-4">
      <HeaderSection />

      <main id="content" class="lg:pt-24 lg:w-[52%] lg:py-24">
        <AboutSection />
        <ExperienceSection />
        <ProjectsSection />
      </main>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');

.body {
  font-family: 'Inter', sans-serif;
}
</style>
