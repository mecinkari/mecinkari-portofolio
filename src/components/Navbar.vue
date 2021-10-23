<template>
  <div
    class="
      z-50
      bg-white
      fixed
      top-0
      left-0
      w-full
      flex
      px-6
      sm:px-20
      md:px-40
      lg:px-60
      transition
      duration-200
      dark:bg-gray-800
      justify-between
      items-center
    "
  >
    <router-link
      class="
        outline-none
        block
        text-black
        transition-colors
        duration-200
        dark:text-gray-50
        p-3
        text-base
        font-semibold
      "
      to="/"
      >TAMCIN</router-link
    >
    <div
      class="
        transition
        duration-200
        divide-y
        md:mr-auto
        dark:divide-gray-900
        md:border-0
        border
        dark:border-gray-900
        absolute
        md:relative
        right-6
        md:right-0 md:divide-y-0
        sm:right-20
        top-16
        md:top-0 md:flex
        gap-x-2
        shadow
        md:shadow-none
      "
      :class="isHidden ? 'hidden' : ''"
    >
      <router-link
        exact-active-class=""
        class="
          w-48
          md:w-auto
          outline-none
          block
          text-black
          transition
          duration-200
          dark:text-gray-50
          p-3
          bg-white
          dark:bg-gray-800
          font-semibold
        "
        v-for="link in links"
        :key="link.title"
        :to="link.href"
        >{{ link.title }}</router-link
      >
    </div>
    <div class="flex gap-2">
      <div
        v-on:click="isHidden = !isHidden"
        class="
          text-base
          border
          dark:border-gray-900
          rounded
          font-semibold
          cursor-pointer
          transition
          md:hidden
          duration-200
          h-10
          w-10
          flex
          items-center
          justify-center
        "
        :class="!isHidden ? 'bg-gray-200 dark:bg-gray-900' : ''"
      >
        <i
          class="
            fa-solid
            transition
            duration-200
            fa-fw fa-bars
            dark:text-gray-50
          "
        ></i>
      </div>
      <button
        class="
          p-2
          text-base
          border
          dark:border-gray-900
          rounded
          font-semibold
          cursor-pointer
          transition
          duration-200
          relative
          flex
          w-10
          h-10
          items-center
          justify-center
        "
        @click="darkFunc"
      >
        <i
          class="
            fa-solid
            absolute
            transition
            duration-200
            fa-fw fa-moon
            dark:text-white
          "
          :class="isDark ? 'opacity-100' : 'opacity-0 transform translate-x-3'"
        ></i>
        <i
          class="
            fa-solid
            absolute
            fa-sun
            transition
            duration-200
            fa-fw
            dark:text-white
          "
          :class="isDark ? 'opacity-0 transform -translate-x-3' : 'opacity-100'"
        ></i>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isDark: eval(localStorage.getItem("dark")),
      test: eval(localStorage.getItem("dark")),
      isHidden: true,
      links: [
        {
          title: "Gallery",
          href: "/gallery",
        },
        {
          title: "Projects",
          href: "/projects",
        },
      ],
    };
  },
  methods: {
    darkFunc: function () {
      this.isDark = !this.isDark;
      localStorage.setItem("dark", this.isDark);
      console.log(this.isDark);
      console.log(eval(localStorage.getItem("dark")));
      console.log(this.test);
      this.test = eval(localStorage.getItem("dark"));
      if (eval(localStorage.getItem("dark"))) {
        document.querySelector("html").classList.remove("dark");
      } else {
        document.querySelector("html").classList.add("dark");
      }
    },
  },
  mounted() {
    if (eval(localStorage.getItem("dark"))) {
      document.querySelector("html").classList.remove("dark");
    } else {
      document.querySelector("html").classList.add("dark");
    }
  },
};
</script>