<template class="bg-green-500 h-screen">
  <div
    class="bg-gray-900 text-gray-100 py-3.5 px-6 shadow md:flex justify-between items-center"
  >
    <div class="flex items-center cursor-pointer">
      <span class="text-green-500 text-xl mr-1"
        ><i class="fab fa-angellist"></i
      ></span>
      <h1 class="text-green-500 text-xl">Islombek</h1>
    </div>

    <spen
      @click="menuOpen()"
      class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl"
    >
      <i :class="[open ? 'fas fa-xmark ' : 'fas fa-bars']"></i>
    </spen>
    <ul
      :class="[open ? 'left-0' : 'left-[-100%]']"
      class="md:flex md:items-center md:px-0 px-3 md:pb-0 pb-10 md:static absolute bg-gray-900 justify-end w-[50%] duration-700 ease-in mt-3 md:mt-0"
    >
      <li class="ms-5 my-3"><a href="#">home</a></li>
      <li class="ms-5 my-3"><a href="#">about</a></li>
      <li class="ms-5 my-3"><a href="#">menu</a></li>
      <li class="ms-5 my-3"><a href="#">contact</a></li>
    </ul>
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  setup() {
    let open = ref(false);
    function menuOpen() {
      open.value = !open.value;
    }
    return { open, menuOpen };
  },
};
</script>
<style></style>
