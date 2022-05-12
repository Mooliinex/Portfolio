<template>
  <section id="contact">
    <div class="flex flex-wrap justify-center py-12 mx-auto my-container">
      <div class="w-full lg:w-1/3 xl:w-1/2">
        <h1 class="text-3xl font-semibold tracking-widest text-white uppercase">Contact</h1>
        <p class="pr-16 mt-6 text-lg text-indigo-300">
         Mail : <a href="mailto:fabien.lefichoux@gmail.com">fabien.lefichoux@gmail.com</a> <br> Linkedin: <a href="https://www.linkedin.com/in/le-fichoux-fabien/">linkedin.com/in/le-fichoux-fabien</a>
        </p>
        <p class="pr-16 mt-6 text-lg text-indigo-300">

        </p>
      </div>
      <div class="w-full py-8 lg:w-2/3 xl:w-1/2">
        <transition leave-active-class="animated fadeOut" @afterLeave="showSubmitMessage = true">
          <form
            class="max-w-2xl p-10 -mb-48 bg-gray-100 rounded shadow-xl"
            @submit.prevent="handleSubmit"
            v-if="!submitDone"
            method="post"
            name="contact"
          >
            <input type="hidden" name="form-name" value="contact" />
            <div class="mb-4">
              <label class="block mb-2 text-sm font-bold text-gray-700" for="name">Full Name</label>
              <input
                @click="form.name.hasError = false"
                v-model="form.name.value"
                :class="{ 'border-red-500': form.name.hasError }"
                class="w-full px-3 py-2 text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
                id="name"
                name="name"
                type="text"
              />
              <p
                v-show="form.name.hasError"
                class="mt-2 text-xs italic text-red-500"
              >Name is required</p>
            </div>
            <div class="mb-4">
              <label class="block mb-2 text-sm font-bold text-gray-700" for="email">Email</label>
              <input
                @click="form.email.hasError = false"
                v-model="form.email.value"
                :class="{ 'border-red-500': form.email.hasError }"
                class="w-full px-3 py-2 text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
                id="email"
                name="email"
                type="text"
              />
              <p
                v-show="form.email.hasError"
                class="mt-2 text-xs italic text-red-500"
              >Email is required</p>
            </div>
            <div class="mb-4">
              <label class="block mb-2 text-sm font-bold text-gray-700" for="message">Message</label>
              <textarea
                @click="form.message.hasError = false"
                v-model="form.message.value"
                rows="5"
                :class="{ 'border-red-500': form.message.hasError }"
                class="w-full px-3 py-2 text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
                id="message"
                name="message"
                type="text"
              ></textarea>
              <p
                v-show="form.message.hasError"
                class="mt-2 text-xs italic text-red-500"
              >Message is required</p>
            </div>
            <div class="pt-4 ">
              <button
                type="button"
                :class="{ 'bg-gray-600 hover:bg-gray-600 ': submitting }"
                class="w-full text-center btn btn-primary"
              >{{ submitting ? "En cours d'envoie..." : "Envoyez" }}</button>
              </div>
          </form>
        </transition>
        <transition enter-active-class="animated fadeIn">
          <div
            v-if="submitDone && showSubmitMessage"
            class="flex justify-center p-10 border-2 border-indigo-500 rounded shadow-xl"
          >
            <div v-if="!submitError" class="flex">
              <span class="pr-4 text-3xl font-semibold text-white">Message sent!</span>
              <svg class="w-10 h-10 text-green-400 fill-current" viewBox="0 0 24 24">
                <defs />
                <path
                  d="M23 0l-4.5 16.5-6.097-5.43 5.852-6.175-7.844 5.421L5 9l18-9zM12 12.501V18l2.193-3.323L12 12.501zm-8.698 6.825l-1.439-.507 5.701-5.215L9 14l-5.698 5.326zm3.262 4.287l-1.323-.565 4.439-4.503L11 19l-4.436 4.613zM2.481 24L1 23.493l8-7.89 1.437.397-7.956 8z"
                />
              </svg>
            </div>
            <div v-else>
                <span class="text-xl font-semibold text-red-400">
                 Bug
                </span>
            </div>
          </div>
        </transition>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
export default {
  components: {

  },
  data() {
    return {
      form: {
        name: { value: null, hasError: false },
        email: { value: null, hasError: false },
        message: { value: null, hasError: false }
      },
      submitting: false,
      submitDone: false,
      showSubmitMessage: false,
      submitError: false,

    };
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join("&");
    },
    handleSubmit() {
      if (
        !this.form.name.value ||
        !this.form.email.value ||
        !this.form.message.value
      ) {
        this.form.name.hasError = !this.form.name.value;
        this.form.email.hasError = !this.form.email.value;
        this.form.message.hasError = !this.form.message.value;
        return;
      }
      if (process.env.NODE_ENV === "production") {
        this.submitting = true;
        const axiosConfig = {
          header: { "Content-Type": "application/x-www-form-urlencoded" }
        };
        axios
          .post(
            "/submit",
            this.encode({
              "form-name": "contact",
              name: this.form.name.value,
              email: this.form.email.value,
              message: this.form.message.value
            }),
            axiosConfig
          )
          .then(() => {
            this.submitting = false;
            this.submitDone = true;
          })
          .catch(err => {
            this.submitError = true;
          });
      } else {
        this.submitting = true;
        setTimeout(() => {
          this.submitting = false;
          this.submitDone = true;
          this.submitError = false;
        }, 2000);
      }
    }
  }
};
</script>

<style scoped>

</style>
