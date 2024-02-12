<template>
<div>
    <div class="lg:px-10 px-3 text-left">
      <div class="grid md:grid-cols-2 grid-cols-1 lg:gap-32 md:gap-20 gap-0">
        <div>
          <div>
            <img
              src="@/assets/images/product2.webp"
              class="md:mx-0 mx-auto w-full"
              alt="productImage"
            />
          </div>
          <div class="mt-5 mb-20 md:block hidden">
            <div class="grid md:grid-cols-5 lg:gap-5 gap-2">
              <div
                :class="
                  item === 1
                    ? 'border-2 border-gray-400'
                    : 'border border-gray-200'
                "
                v-for="item in 4"
                :key="item"
                class="flex items-center justify-center rounded-lg"
              >
                <img
                  src="@/assets/images/product2.webp"
                  class="rounded-lg"
                  alt="productImage"
                />
              </div>
              <div
                class="flex items-center justify-center rounded-lg lg:text-base text-sm	 border border-gray-200"
              >
                <p>+ 4 more</p>
              </div>
            </div>
          </div>
        </div>
        <div>
          <div>
            <div class="flex items-center justify-between mb-5 md:mt-0 mt-5">
              <div class="flex items-center">
                <img
                  src="@/assets/images/reebok.png"
                  class="h-7 w-7 rounded-full"
                />
                <span class="ml-4 text-xs font-semibold">Reebok</span>
              </div>
              <span class="text-gray-400">HR7123634-0</span>
            </div>
            <div>
              <h2 class="text-2xl font-bold">Shoes Reebok Zig Kinetica 3</h2>
              <div class="flex items-center mt-4 mb-10">
                <button type="button" v-for="star in 5" :key="star">
                  <img src="@/assets/svg/star.svg" alt="starIcon" class="h-3" />
                </button>
                <span class="ml-2 text-gray-400 text-xs">42 reviews</span>
              </div>
              <h1 class="text-4xl font-bold">$199.00</h1>

              <div class="mt-10">
                <div class="flex items-center space-x-2 mb-4">
                  <span class="text-xs font-semibold">Color</span>
                  <span class="bg-gray-400 h-2 w-2 border rounded-full"></span>
                  <span class="text-gray-400 text-xs">White</span>
                </div>

                <div class="flex items-center md:space-x-4 space-x-2">
                  <div
                    v-for="item in 3"
                    :key="item"
                    class="flex items-center justify-center rounded-lg"
                  >
                    <img
                      :class="
                        item === 1
                          ? 'border-2 border-gray-400'
                          : 'border border-gray-200'
                      "
                      src="@/assets/images/product2.webp"
                      class="rounded-lg h-20"
                      alt="productImage"
                    />
                  </div>
                </div>
              </div>

              <div class="my-5">
                <div class="flex items-center space-x-2 mb-4">
                  <span class="text-xs font-semibold">Size</span>
                  <span class="bg-gray-400 h-2 w-2 border rounded-full"></span>
                  <span class="text-gray-400 text-xs">EU Men</span>
                </div>
                <div class="grid lg:grid-cols-6 grid-cols-3 gap-2">
                  <div
                  @click="selectSize(item)"
                    :class="{ 'bg-black text-white': item === currentSize }"
                    class="flex items-center justify-center border border-gray-200 py-2 rounded hover:cursor-pointer"
                    v-for="item in 9"
                    :key="item"
                  >
                    {{ 34 + item }}
                  </div>
                </div>
                <p class="mt-3 text-xs text-orange-300">Size guide</p>
              </div>
            </div>
            <div class="mt-10 mb-2 flex items-center justify-center">
              <button
                class="flex items-center justify-center py-2.5 px-4 rounded-lg w-full text-sm text-white bg-black"
              >
                Add to cart
              </button>
              <button class="bg-gray-100 rounded-lg border p-2.5 ml-4">
                <img src="@/assets/svg/heart.svg" class="h-4" alt="heartIcon" />
              </button>
            </div>
            <div class="flex items-center pb-10">
			<img src="@/assets/svg/delivery.svg" class="h-5">
			<span class="ml-2 text-xs font-semibold">Free delivery on orders over $30</span>
            </div>
          </div>
        </div>
      </div>
    </div>
</div>
</template>

<script>
import { defineComponent, ref } from "vue"

export default defineComponent({
	name: "ProductDetails",

	setup(){
		const currentSize = ref(3)
		const selectSize = (index) => {
			currentSize.value = index
		}	
		return{
			selectSize,
			currentSize
		}
	}
})

</script>