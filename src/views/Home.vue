<template>
  <div class="px-6 flex flex-col gap-y-10 sm:px-20 md:px-40 lg:px-60 pt-24">
    <section class="hero transition duration-200">
      <div
        class="
          flex flex-col-reverse
          md:flex-row md:flex md:items-center
          mb-6
          justify-between
        "
      >
        <div>
          <p
            class="
              bg-gradient-to-r
              from-blue-500
              to-green-500
              text-4xl
              sm:text-5xl
              md:text-6xl
              font-black
              inline-block
              text-transparent
              bg-clip-text
              transition
              duration-200
              mt-6
              mb-3
            "
          >
            TAMCIN
          </p>
          <p
            class="
              text-md
              md:text-lg
              font-semibold
              text-gray-500
              transition
              duration-200
              dark:text-gray-300
            "
          >
            Digital Artist &amp; Web Programmer
          </p>
        </div>
        <img
          :src="logo"
          class="w-28 logo rounded-lg md:ml-auto transform sm:mx-0"
          alt="profile"
        />
      </div>
      <a
        href="#"
        class="
          mt-6
          inline-block
          px-4
          py-2
          font-semibold
          text-white
          outline-none
          bg-gradient-to-r
          from-red-500
          rounded-full
          to-yellow-500
        "
        >See Projects</a
      >
    </section>
    <about-section />
    <project-section />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutSection from "../components/AboutSection.vue";
import ProjectSection from "../components/ProjectSection.vue";

export default {
  name: "Home",
  components: {
    AboutSection,
    ProjectSection,
  },
  data() {
    return {
      logo: require("../assets/profile2.png"),
    };
  },
  mounted() {
    document.title = "Mecinkari Portofolio";
  },
};
</script>

