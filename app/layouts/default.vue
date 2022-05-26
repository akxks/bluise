<template>
  <main :class="[$route.name]" class="main px-4 md:px-0">
    <div class="container mx-auto">
      <site-header />
      <nuxt class="nuxt" />
    </div>
 
    <svg  class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1" xmlns="http://www.w3.org/2000/svg">
  <path fill="#FF0066" d="M34.7,-48C48.5,-37.8,65.7,-32.3,75.3,-20.3C84.9,-8.3,87.1,10.4,82.3,27.3C77.5,44.1,65.8,59.3,50.9,65.2C36.1,71.2,18,67.9,-0.1,68C-18.2,68.1,-36.4,71.7,-50.4,65.4C-64.3,59.2,-74,43.2,-79.9,25.8C-85.9,8.3,-88.1,-10.5,-81.4,-25C-74.6,-39.5,-59,-49.6,-44,-59.4C-28.9,-69.2,-14.5,-78.7,-2,-75.9C10.5,-73.2,20.9,-58.2,34.7,-48Z" transform="translate(100 100)" />
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
