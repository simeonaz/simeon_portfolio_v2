<script setup>
const experiences = [
  {
    year: 'June 2024 — June 2025',
    title: 'Full Stack Engineer, Team Lead',
    company: 'TOK Services',
    description:
      'As a Full Stack Developer and Team Lead, I have designed, developed, and maintained critical frontend components, ensuring product-wide consistency and high performance. I have also led a cross-functional team of front‑end and back‑end engineers, working closely with designers and product managers to define and advocate for web accessibility best practices (WCAG).',
    technologies: [
      'JavaScript',
      'TypeScript',
      'Node.js',
      'Vue.js',
      'Nest.js',
      'SQL',
      'NoSql',
      'Git',
    ],
    link: 'https://tok-services.web.app/',
  },
  {
    year: 'march 2023 — april 2024',
    title: 'Internship Experience',
    company: 'Euphorbia Group',
    description:
      'As an intern, I developed internal tools to optimize business workflows and contributed to building SaaS solutions for various clients, collaborating with the technical team on architecture, testing, and deployment.',
    technologies: [
      'JavaScript',
      'TypeScript',
      'Node.js',
      'Vue.js',
      'Nest.js',
      'PHP',
      'CodeIgniter',
      'SQL',
      'NoSql',
      'Git',
    ],
    link: 'https://euphorbiagroup.com/',
  },
]
</script>

<template>
  <section
    id="experience"
    class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24"
    aria-label="Work experience"
  >
    <div
      class="sticky top-0 z-20 -mx-6 mb-4 bg-[#00000026] px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0"
    >
      <h2 class="text-sm font-bold uppercase tracking-widest text-slate-200 lg:sr-only">
        Experience
      </h2>
    </div>
    <div>
      <ol class="group/list">
        <li class="mb-12" v-for="(experience, index) in experiences" :key="index">
          <div
            class="group relative grid pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50"
          >
            <div
              class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg"
            ></div>
            <header
              class="z-10 mb-2 mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500 sm:col-span-2"
              :aria-label="experience.year"
            >
              {{ experience.year }}
            </header>
            <div class="z-10 sm:col-span-6">
              <h3 class="font-medium leading-snug text-slate-200">
                <div>
                  <a
                    class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                    :href="experience.link"
                    target="_blank"
                    rel="noreferrer noopener"
                    aria-label="Senior Frontend Engineer, Accessibility at Klaviyo (opens in a new tab)"
                    ><span
                      class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                    ></span
                    ><span
                      >{{ experience.title }} ·
                      <span class="inline-block"
                        >{{ experience.company
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
                </div>
              </h3>
              <p class="mt-2 text-sm leading-normal">
                {{ experience.description }}
              </p>
              <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                <li
                  class="mr-1.5 mt-2"
                  v-for="(technology, index) in experience.technologies"
                  :key="index"
                >
                  <div
                    class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                  >
                    {{ technology }}
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </li>
      </ol>

      <div class="mt-12">
        <a
          class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 font-semibold text-slate-200 group/link text-base"
          href="https://drive.google.com/file/d/1bvW63Ggdg1U_4GH9w-rv476JhjdlgyFL/view?usp=sharing"
          target="_blank"
          rel="noreferrer noopener"
          aria-label="View Full Résumé (opens in a new tab)"
          ><span
            >View
            <span class="inline-block"
              >Résumé<svg
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
      </div>
    </div>
  </section>
</template>
