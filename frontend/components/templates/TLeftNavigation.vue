<template>
  <v-navigation-drawer
    permanent
    mini-variant
    app
    color="grey lighten-1"
  >
    <OVerticalNavigation :navi-item-list="naviItemList" />
  </v-navigation-drawer>
</template>

<script>
import OVerticalNavigation from '~/components/organisms/card/OVerticalNavigation.vue';

export default {
  name: 'TNavigation',
  components: {
    OVerticalNavigation
  },
  data() {
    return {
      naviItemList: [
        {
          icon: 'mdi-home',
          text: 'Home'
        },
        {
          icon: 'mdi-folder',
          text: 'Folder'
        },
        {
          icon: 'mdi-account-multiple',
          text: 'Account'
        }
      ]
    }
  }
}
</script>

<style>

</style>