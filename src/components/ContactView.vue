<script setup>
import axios from 'axios'
import { ref } from 'vue'
import { useToast } from 'vue-toast-notification'
import 'vue-toast-notification/dist/theme-sugar.css'

const name = ref(null)
const email = ref(null)
const message = ref(null)
const loading = ref(false)
const $toast = useToast()

const sendMail = () => {
  loading.value = true
  const data = {
    service_id: 'service_s0tf6g8',
    template_id: 'template_klbnvnf',
    user_id: 'rXU7jvemVMtSBpj2i',
    template_params: {
      name: name.value,
      email: email.value,
      message: message.value,
    },
  }

  axios
    .post('https://api.emailjs.com/api/v1.0/email/send', data)
    .then(
      (result) => {
        console.log('SUCCESS!', result.text)
        $toast.success('Message sent successfully')
        name.value = null
        email.value = null
        message.value = null
      },
      (error) => {
        console.log('FAILED...', error.text)
        $toast.error('An error occurred')
      },
    )
    .catch((error) => {
      console.log(error)
    })
    .finally(() => {
      loading.value = false
    })
}
</script>

<template>
  <section
    id="contact"
    class="scroll-mt-16 mb-8 md:mb-24 lg:mb-36 lg:scroll-mt-24"
    aria-label="Contact"
  >
    <div
      class="sticky top-0 z-20 -mx-6 mb-4 bg-[#00000026] px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0"
    >
      <h2 class="text-sm font-bold uppercase tracking-widest text-slate-200 lg:sr-only">Contact</h2>
    </div>

    <p class="mb-4">
      Do you have a project or a specific request? Feel free to reach out using the form below. I
      will get back to you as soon as possible.
    </p>

    <div>
      <form class="flex flex-col space-y-4 w-full font-lato" @submit.prevent="sendMail">
        <div class="w-full grid grid-cols-1 md:grid-cols-2 gap-4">
          <input
            id="name"
            type="text"
            placeholder="Your name"
            v-model="name"
            required
            class="border border-[#2F4858] rounded-2xl px-10 lg:px-8 py-4 focus:outline-none placeholder:text-[14px] text-[14px]"
          />
          <input
            id="email"
            type="email"
            v-model="email"
            required
            placeholder="Your email"
            class="border border-[#2F4858] rounded-2xl px-10 lg:px-4 py-4 focus:outline-none placeholder:text-[14px] text-[14px]"
          />
        </div>
        <textarea
          class="h-40 border border-[#2F4858] rounded-2xl px-10 lg:px-4 py-4 focus:outline-none placeholder:text-[14px] text-[14px] resize-none"
          required
          placeholder="Type your message"
          v-model="message"
        ></textarea>
        <div class="flex justify-center">
          <button
            class="px-6 py-3 text-start bg-transparent text-[#2F4858] cursor-pointer rounded-2xl border border-[#2F4858] hover:bg-[#2F4858] hover:text-white transition-colors duration-300 text-md"
          >
            <svg
              v-if="loading"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              class="animate-spin"
              style="fill: #ffffff"
            >
              <path
                d="M12 22c5.421 0 10-4.579 10-10h-2c0 4.337-3.663 8-8 8s-8-3.663-8-8c0-4.336 3.663-8 8-8V2C6.579 2 2 6.58 2 12c0 5.421 4.579 10 10 10z"
              ></path>
            </svg>
            <span v-else>Send</span>
          </button>
        </div>
      </form>
    </div>
  </section>
</template>
