<template>
  <v-container>
    <TNavigation />
    <Nuxt />
  </v-container>
</template>

<script>
import TNavigation from '~/components/templates/TNavigation.vue';

export default {
  name: 'LeftNavigation',
  components: {
    TNavigation
  }
}
</script>

<style>

</style>