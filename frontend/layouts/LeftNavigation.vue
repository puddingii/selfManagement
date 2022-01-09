<template>
  <v-app id="inspire">
    <TLeftNavigation />

    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
import TLeftNavigation from '~/components/templates/TLeftNavigation.vue';

export default {
  name: 'LeftNavigation',
  components: {
    TLeftNavigation,
  },
  
}
</script>

<style>

</style>