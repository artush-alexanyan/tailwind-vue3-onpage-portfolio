<template>
  <div id="app" class="poppins max-w-7xl mx-auto">
    <AppHeader />
    <div class="main">
      <router-view/>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue"
import AppHeader from "./app/AppHeader.vue"

export default defineComponent({
  name: "App",
  components: { AppHeader }
})

</script>

<style>
.poppins {
 font-family: 'Poppins', sans-serif;
}

</style>
