<template>
  <main :class="[$route.name]" class="main px-4 md:px-0">
    <div class="container mx-auto">
      <site-header />
      <nuxt class="nuxt" />
    </div>

    <svg class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1">
      <polygon stroke="none" stroke-width="0" fill="#0b3765" points="0,0.6 0,1 10,1 10,0" />

    </svg>

    <svg class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1">
      <path fill="#4D09EB" d="M39.3,-62.6C50.7,-53.8,59.6,-42.5,66,-29.8C72.4,-17,76.3,-2.7,76,12.1C75.6,26.8,70.9,42.1,61.3,53C51.7,64,37.2,70.5,22,75.1C6.8,79.7,-9.1,82.3,-24.3,79.4C-39.6,76.5,-54.3,68.1,-64.7,56.1C-75.2,44,-81.4,28.3,-83.3,12.2C-85.2,-3.9,-82.8,-20.3,-75.6,-33.9C-68.4,-47.5,-56.4,-58.3,-43,-66.2C-29.6,-74.1,-14.8,-79.2,-0.4,-78.5C13.9,-77.9,27.9,-71.5,39.3,-62.6Z" transform="translate(100 100)" />
    </svg>

    <site-footer />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import SiteHeader from '@/components/partials/header.vue';
import SiteFooter from '@/components/partials/footer.vue';

@Component({
  components: {
    SiteHeader,
    SiteFooter,
  },
})
export default class DefaultLayout extends Vue {}
</script>

<style lang="scss">
.divider {
  position: relative;
  min-width: 100vw;
  margin-top: auto;
}

.nuxt {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}
</style>
