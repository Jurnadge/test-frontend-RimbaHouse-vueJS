<script>
export default {
  name: "ModalLogin",
  props: {
    showModalLogin: Boolean,
    closeModalLogin: Function,
  },
  methods: {
    closeModal() {
      this.closeModalLogin();
    },
  },
};
</script>

<template>
  <div
    v-if="showModalLogin"
    class="absolute flex justify-center items-center backdrop-blur-sm top-0 right-0 -left-0 -bottom-0 z-50"
  >
    <div class="w-72 h-72 border-2 grid items-center mx-8 bg-white rounded-md">
      <form class="mx-5">
        <h1 class="text-center text-2xl mb-4 -mt-3">Login</h1>
        <div class="flex flex-col gap-6">
          <div class="relative">
            <input
              type="text"
              id="email"
              class="block px-2 pb-2 pt-3 w-full text-sm text-gray-900 bg-transparent rounded-lg border-1 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
              placeholder=" "
            />
            <label
              for="email"
              class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-2 z-10 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1"
              >Email</label
            >
          </div>

          <div class="relative">
            <input
              type="password"
              id="password"
              class="block px-2 pb-2 pt-3 w-full text-sm text-gray-900 bg-transparent rounded-lg border-1 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
              placeholder=" "
            />
            <label
              for="password"
              class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-2 z-10 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1"
              >Password</label
            >
          </div>

          <div class="flex gap-3">
            <button
              class="px-2 py-1 bg-[#E50914] text-white rounded-md lg:hover:scale-125 lg:duration-200"
            >
              Login
            </button>
            <button
              @click="closeModalLogin"
              class="px-2 py-1 bg-gray-700 text-white rounded-md lg:hover:scale-125 lg:duration-200"
            >
              Cancel
            </button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>
