<script setup>
import iryka from '@/assets/img/iryka.png'
import panneauMobile from '@/assets/img/panneaumobile.png'
import aep from '@/assets/img/aep.png'

const projectList = [
  {
    name: 'Iryka',
    image: iryka,
    url: 'https://app.iryka.com/',
    company: 'TOK Services',
    description:
      'Iryka is a website creation platform currently in development, built on a modular template gallery. Each user can customize and deploy their site in just a few clicks without any technical knowledge. I designed and implemented the REST APIs for managing templates, users, and content. I also handled the majority of the front‑end development to ensure a smooth, responsive experience.',
  },
  {
    name: 'Panneau Mobile client portal',
    image: panneauMobile,
    url: 'https://pige.panneaumobile.co/',
    company: 'TOK Services',
    description:
      'The Panneau Mobile client portal is a web platform that enables each client to track campaigns and various activities launched by the agency in real time. The administrator inputs and updates all the information clients see on their personalized dashboard. Clients have a consolidated view of their performance metrics and receive alerts for key actions. The responsive interface ensures seamless access from both desktop and mobile.',
  },
  {
    name: 'AEP Parakou',
    image: aep,
    url: 'https://aep.parakou.bj',
    company: 'EUPHORBIA GROUP',
    description:
      'I contributed to the development of a management platform for drinking water supply facilities in the city of Parakou, Benin. The platform enables technical and administrative teams to monitor infrastructure in real time (water towers, boreholes, public fountains, etc.), centralize maintenance data, and support better decision-making. I worked on the backend development, the admin interface, and the integration of interactive maps for geospatial visualization of the facilities.',
  },
]
</script>

<template>
  <section
    id="projects"
    class="mb-16 scroll-mt-16 md:mb-24 lg:scroll-mt-24"
    aria-label="Selected projects"
  >
    <!-- lg:mb-36 -->
    <div
      class="sticky top-0 z-20 -mx-6 mb-4 bg-[#00000026] px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0"
    >
      <h2 class="text-sm font-bold uppercase tracking-widest text-slate-200 lg:sr-only">
        Projects
      </h2>
    </div>
    <div>
      <ul class="group/list">
        <li class="mb-12" v-for="(project, index) in projectList" :key="index">
          <div
            class="group relative grid gap-4 pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50"
          >
            <div
              class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg"
            ></div>
            <div class="z-10 sm:order-2 sm:col-span-6">
              <h3>
                <a
                  class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                  :href="project.url"
                  target="_blank"
                  rel="noreferrer noopener"
                  aria-label="Build a Spotify Connected App (opens in a new tab)"
                  ><span
                    class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                  ></span
                  ><span
                    >{{ project.name }} ·
                    <span class="inline-block"
                      >{{ project.company
                      }}<svg
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:-translate-y-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M5.22 14.78a.75.75 0 001.06 0l7.22-7.22v5.69a.75.75 0 001.5 0v-7.5a.75.75 0 00-.75-.75h-7.5a.75.75 0 000 1.5h5.69l-7.22 7.22a.75.75 0 000 1.06z"
                          clip-rule="evenodd"
                        ></path></svg></span></span
                ></a>
              </h3>
              <p class="mt-2 text-sm leading-normal">
                {{ project.description }}
              </p>
            </div>
            <img
              loading="lazy"
              width="200"
              height="48"
              decoding="async"
              data-nimg="1"
              class="aspect-video object-cover rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1"
              style="color: transparent"
              :src="project.image"
              alt=""
            />
          </div>
        </li>
      </ul>

      <div class="mt-12 py-4 flex items-start">
        <p class="text-sm leading-normal text-[#909090] w-full lg:w-1/2">
          There’s still much more to explore; please allow me a little time so that I can show you
          more.
        </p>
      </div>
      <!-- <div class="mt-12">
        <a
          class="inline-flex items-center leading-tight font-semibold text-slate-200 group"
          aria-label="View Full Project Archive"
          href="/archive"
          ><span
            ><span
              class="border-b border-transparent pb-px transition group-hover:border-teal-300 motion-reduce:transition-none"
              >View Full Project </span
            ><span class="whitespace-nowrap"
              ><span
                class="border-b border-transparent pb-px transition group-hover:border-teal-300 motion-reduce:transition-none"
                >Archive</span
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
                class="ml-1 inline-block h-4 w-4 shrink-0 -translate-y-px transition-transform group-hover:translate-x-2 group-focus-visible:translate-x-2 motion-reduce:transition-none"
                aria-hidden="true"
              >
                <path
                  fill-rule="evenodd"
                  d="M3 10a.75.75 0 01.75-.75h10.638L10.23 5.29a.75.75 0 111.04-1.08l5.5 5.25a.75.75 0 010 1.08l-5.5 5.25a.75.75 0 11-1.04-1.08l4.158-3.96H3.75A.75.75 0 013 10z"
                  clip-rule="evenodd"
                ></path></svg></span></span
        ></a>
      </div> -->
    </div>
  </section>
</template>
