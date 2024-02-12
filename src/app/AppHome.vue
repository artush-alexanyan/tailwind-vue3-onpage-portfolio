<template>
<div>
	<div class="text-center">
		<ProductDetails />
	</div>
</div>
</template>

<script>
import { defineComponent } from "vue"
import ProductDetails from "@/shop/ProductDetails.vue"

export default defineComponent({
	name: "AppHome",
	components: { ProductDetails },
})

</script>