<!-- hide the footer from "cover" layout -->
<template>
  <footer
    v-if="$nav.currentLayout === 'default'"
    class="absolute bottom-0 left-0 right-0 p-2" style="font-size:small;font-weight: 100;"
  >
    {{ $nav.currentPage }} / {{ $nav.total }}
  </footer>
</template>