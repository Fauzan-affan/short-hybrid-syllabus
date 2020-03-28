<template>
  <div id="app" class="flex bg-gray-900 text-white min-h-screen">

    <SidebarNavigation />

    <div class="w-full ml-24">
      <transition name="page">
        <router-view/>
      </transition>
    </div>
  </div>
</template>

<script>
import SidebarNavigation from "@/components/SidebarNavigation.vue";

export default {
  components: {
    SidebarNavigation
  }
}
</script>

<style src="./css/main.css"/>
