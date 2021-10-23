<template>
  <div
    id="app"
    class="
      font-sans
      transition
      min-w-full
      bg-white
      dark:bg-gray-800
      min-h-screen
      duration-200
      ease-in-out
    "
  >
    <!-- <button
      id="darkToggle"
      class="
        flex
        items-center
        justify-center
        h-10
        w-10
        outline-none
        bg-gray-800
        dark:bg-gray-100
        fixed
        z-10
        bottom-3
        right-3
        rounded-full
        cursor-pointer
      "
      v-on:click="darkFunc"
    >
      <i
        class="fa-solid text-gray-100 dark:text-gray-800 fa-fw"
        :class="test ? 'fa-moon' : 'fa-sun'"
      ></i>
    </button> -->
    <div class="relative">
      <Navbar> </Navbar>
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
  data() {
    return {
      isDark: eval(localStorage.getItem("dark")),
      test: eval(localStorage.getItem("dark")),
    };
  },
  // methods: {
  //   darkFunc: function () {
  //     this.isDark = !this.isDark;
  //     localStorage.setItem("dark", this.isDark);
  //     console.log(this.isDark);
  //     console.log(eval(localStorage.getItem("dark")));
  //     console.log(this.test);
  //     this.test = eval(localStorage.getItem("dark"));
  //     if (eval(localStorage.getItem("dark"))) {
  //       document.querySelector("html").classList.remove("dark");
  //     } else {
  //       document.querySelector("html").classList.add("dark");
  //     }
  //   },
  // },
  // mounted() {
  //   if (eval(localStorage.getItem("dark"))) {
  //     document.querySelector("html").classList.remove("dark");
  //   } else {
  //     document.querySelector("html").classList.add("dark");
  //   }
  // },
};
</script>

<style>
.fade-enter,
.fade-leave-to {
  opacity: 0;
  transform: translateX(-2rem);
}
.fade-enter-active,
.fade-leave-active {
  transition: all 300ms ease;
}
</style>