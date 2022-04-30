<!-- an example footer for pages -->
<template>
  <footer
    v-if="$slidev.nav.currentLayout !== 'cover'"
    class="absolute bottom-0 left-0 right-0 p-1"
  >
    <logos-twitter /> alliwene
    <logos-github-octocat /> alliwene
  </footer>
</template>