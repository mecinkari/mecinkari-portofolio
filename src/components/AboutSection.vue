<template>
  <section class="about-section py-6">
    <p class="h1 dark:text-white" :class="transitionClass">About Me</p>
    <p class="font-medium text-lg dark:text-white" :class="transitionClass">
      My real name is <span class="italic">Muhammad Anugrah Pratama</span>, but
      the internet call me <span class="italic">Tamcin</span>. I'm a
      <code class="font-bold text-green-500">digital artist</code>
      and
      <code class="text-green-500 font-bold">web programmer</code>
      based in Depok, Indonesia. Start digital art at 16 while using a phone at
      that time, but now I'm using <span class="font-bold">HUION H430P</span>.
      Start to code at 16 years old while studied about Software Engineering at
      <code class="text-blue-500 font-bold underline"
        ><a
          href="http://smk.tarunabhakti.net/"
          target="_blank"
          rel="noopener noreferrer"
          >'SMK Taruna Bhakti'</a
        ></code
      >
    </p>
  </section>
</template>

<script>
export default {
  name: "AboutSection",
  data() {
    return {
      transitionClass: "transition duration-200",
    };
  },
};
</script>

<style>
</style>