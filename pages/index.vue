<template>
  <main class="flex-1">
    <SectionsHeroSection />
    <!-- <SectionsSocialProuf/> -->
    <!-- <SectionsLogoCloud/> -->
    <SectionsServices />
    <SectionsAllPosts />
    <SectionsAboutContent />
    <SectionsCta />
  </main>
</template>

<script lang="ts" setup>
useHead({
  title: 'Econify',
  meta: [
    {
      name: 'description',
      content: 'A sample landing page built using UnoCSS + NuxtJS and Unify UI blocks',
    },
  ],
  link: [
    {
      href: "https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
      rel: "stylesheet"
    }
  ],
})
</script>