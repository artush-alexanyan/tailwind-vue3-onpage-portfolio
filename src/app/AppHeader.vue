<template>
  <div>
    <div class="md:px-10 px-3">
      <div class="flex items-center justify-between w-full py-5">
        <div class="brand">
          <a class="uppercase text-2xl font-semibold" href="#">
            <span>BR.</span>
            <span class="text-gray-400">F</span>
          </a>
        </div>
        <div class="search">
          <form>
            <div class="md:min-w-80 md:block hidden">
              <input
                class="rounded-full py-2 bg-gray-50 w-full text-gray-500 text-sm px-3 border border-gray-300 outline-0 focus:border-2 focus:border-gray-400"
                placeholder="Search"
                type="text"
                name="search"
              />
            </div>
          </form>
        </div>
        <div class="flex items-center space-x-6">
          <div class="grid place-items-center space-y-1">
            <button type="button" class="relative">
              <img class="h-6" src="@/assets/svg/bag.svg" alt="bagIcon" />
              <span
                class="h-4 w-4 bg-yellow-600 text-white rounded-full flex items-center justify-center text-xs absolute -right-1 -top-1"
                >4</span
              >
            </button>
            <span class="text-xs">Cart</span>
          </div>
          <div class="grid place-items-center space-y-1">
            <button type="button">
              <img class="h-6" src="@/assets/svg/heart.svg" alt="bagIcon" />
            </button>
            <span class="text-xs">Favorites</span>
          </div>
          <button
            type="button"
            class="flex items-center justify-center rounded-full h-11 w-11 border border-gray-100"
          >
            <img
              src="https://i.pravatar.cc"
              class="rounded-full"
              alt="userAvatar"
            />
          </button>
        </div>
      </div>
    </div>

    <div class="md:px-10 px-3 py-5 border-b border-b-gray-100">
      <ul class="md:flex md:items-center md:space-x-6 grid grid-cols-3">
        <li>Women</li>
        <li>Man</li>
        <li>Kids</li>
        <li>Sports</li>
        <li>Brands</li>
        <li>New</li>
        <li class="text-orange-600">Sale</li>
      </ul>
    </div>

    <div class="breadcrumb md:px-10 px-3 pt-5 pb-10">
      <ul class="flex items-center space-x-2 text-sm text-gray-800">
        <li>Clothes and shoes</li>
        <span class="bg-gray-400 h-2 w-2 border rounded-full"></span>
        <li>Shoes</li>
        <span class="bg-gray-400 h-2 w-2 border rounded-full"></span>
        <li>Reebok</li>
      </ul>
    </div>

  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "AppHeader",
});
</script>
