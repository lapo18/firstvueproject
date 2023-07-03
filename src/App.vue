<template>
  <button @click="show = !show">Menu</button>
  <Transition name="fade">
    <VueMenu v-show="show"/>
  </Transition>
</template>

<script>
import VueMenu from "./components/VueMenu.vue"
export default {
  name: "App",
  components: { VueMenu },
  data() {
    return {
        show: false,
      }
  }
  }
</script>

<style>
.fade-enter-from,
.fade-leave-to{
  opacity: 0;
}
.fade-enter-active , 
.fade-leave-active{
  transition: opacity 0.3s ease;
}

</style>
