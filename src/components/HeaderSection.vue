<script setup>
import { onMounted } from 'vue'

const navLinks = [
  { name: 'About', path: '#about' },
  { name: 'Experience', path: '#experience' },
  { name: 'Projects', path: '#projects' },
  // { name: 'Contact', path: '#contact' },
]

const socialMediaLinks = [
  {
    name: 'GitHub',
    link: 'https://github.com/simeonaz',
    svg: `<svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 16 16"
                  fill="currentColor"
                  class="h-6 w-6"
                  aria-hidden="true"
                >
                  <path
                    d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
                  ></path></svg
              >`,
  },
]

function smoothScroll(event, selector) {
  event.preventDefault()
  const target = document.querySelector(selector)
  if (target) {
    target.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}

onMounted(() => {
  if (window.location.hash) {
    const el = document.querySelector(window.location.hash)
    if (el) el.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
})
</script>

<template>
  <header
    class="lg:sticky lg:top-0 lg:flex lg:flex-col lg:max-h-screen lg:w-[48%] lg:justify-between py-12 lg:py-24"
  >
    <h1 class="text-slate-200 tracking-tight font-bold text-4xl sm:text-5xl" aria-label="Name">
      <a href="#">Siméon Azogbonon</a>
    </h1>
    <h2
      class="mt-3 text-lg font-medium tracking-tight text-slate-200 sm:text-xl"
      aria-label="Title"
    >
      Full Stack Engineer
    </h2>
    <p class="mt-4 max-w-xs leading-normal" aria-label="Description">
      I architect and build end-to-end digital solutions.
      <!-- , crafting both elegant user interfaces
          and robust backend systems that work seamlessly together -->
    </p>

    <nav aria-label="Main navigation">
      <ul class="hidden lg:block w-max mt-6 space-y-2" aria-label="Main navigation">
        <li v-for="(link, index) in navLinks" :key="index">
          <a
            class="group flex items-center py-2"
            :href="link.path"
            @click="smoothScroll($event, link.path)"
          >
            <span
              class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-12 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
            ></span>
            <span
              class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200"
              >{{ link.name }}</span
            >
          </a>
        </li>
      </ul>

      <ul class="ml-1 mt-8 flex items-center" aria-label="Social media">
        <li class="mr-5 shrink-0 text-xs" v-for="link in socialMediaLinks" :key="link.name">
          <a
            class="block hover:text-slate-200"
            :href="link.link"
            target="_blank"
            rel="noreferrer noopener"
            :aria-label="link.name"
            :title="link.name"
            ><span class="sr-only">{{ link.name }}</span>
            <div v-html="link.svg"></div
          ></a>
        </li>
      </ul>
    </nav>
  </header>
</template>
