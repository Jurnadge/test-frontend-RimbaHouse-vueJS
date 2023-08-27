<script>
export default {
  name: "Header",
};
</script>

<script setup>
import { Avatar } from "flowbite-vue";
import { ref } from "vue";
import ModalLogin from "./ModalLogin.vue";
import ModalRegister from "./ModalRegister.vue";

//dropdown avatar
const dropdownOpen = ref(false);
const toggleDropdown = () => {
  dropdownOpen.value = !dropdownOpen.value;
};

//modalLogin
const localShowModalLogin = ref(false);
const setShowModalLogin = () => {
  localShowModalLogin.value = !localShowModalLogin.value;
};

//modalRegister
const localShowModalRegister = ref(false);
const setShowModalRegister = () => [
  (localShowModalRegister.value = !localShowModalRegister.value),
];
</script>

<template>
  <nav class="bg-[#1F1F1F] px-10 flex items-center py-4 shadow-black shadow-lg">
    <div class="w-full flex justify-between">
      <!-- <div class="flex items-center justify-center text-white gap-2">
        <a href="#">Home</a>
        <a href="#">Tv Show</a>
        <a href="#">Movies</a>
      </div> -->

      <div class="grid items-center text-white">
        <img src="../assets/netflix.svg" alt="" class="w-[30px] h-[30px]" />
      </div>

      <div class="flex gap-3">
        <button
          class="bg-[#E50914] text-[#FFFF] px-2 py-1 rounded-md hover:scale-125 duration-200"
          @click="setShowModalLogin"
        >
          Login
        </button>
        <button
          class="bg-[#FFFF] text-[#E50914] px-2 py-1 rounded-md hover:scale-125 duration-200"
          @click="setShowModalRegister"
        >
          Register
        </button>

        <!-- <div
          class="relative flex flex-col cursor-pointer"
          @click="toggleDropdown"
        >
          <div>
            <Avatar
              rounded
              img="https://cdn-icons-png.flaticon.com/512/3135/3135715.png"
            />
          </div>
          <div
            v-if="dropdownOpen"
            class="flex flex-col absolute top-9 right-0 mt-2 w-24 bg-amber-700 text-white border border-gray-600 rounded-lg shadow-lg"
          >
            <a href="#" class="px-3 hover:bg-gray-600">Profile</a>
            <a href="#" class="px-3 hover:bg-gray-600">Testing</a>
            <a href="#" class="px-3 hover:bg-gray-600">Logout</a>
          </div>
        </div> -->
      </div>
    </div>
    <ModalLogin
      :showModalLogin="localShowModalLogin"
      :closeModalLogin="() => (localShowModalLogin = false)"
    />
    <ModalRegister
      :showModalRegister="localShowModalRegister"
      :closeModalRegister="() => (localShowModalRegister = false)"
    />
  </nav>
</template>
