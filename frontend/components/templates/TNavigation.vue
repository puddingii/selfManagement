<template>
  <v-navigation-drawer
    permanent
    expand-on-hover
    app
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