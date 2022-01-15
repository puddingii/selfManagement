<template>
  <v-app-bar
    color="grey lighten-5"
    class=""
  >
    <v-toolbar-title>{{ pageTitle }}</v-toolbar-title>

    <v-spacer />

    <AButton v-for="(btnInfo, i) in iconBtnGroup" :key="i" @click="btnInfo.onBtn">
      <v-icon>{{ btnInfo.icon }}</v-icon>
      {{ btnInfo.text }}
    </AButton>

    <MDotMenu :item-group="dropdownItemGroup" />
  </v-app-bar>
</template>

<script>
import AButton from '~/components/atoms/button/AButton.vue';
import MDotMenu from '~/components/molecules/list/MDotMenu.vue';

export default {
  components: {
    AButton,
    MDotMenu,
  },
  props: {
    pageTitle: {
      type: String,
      default: 'Default Page'
    }
  },
  data() {
    return {
      dropdownItemGroup: [
        {
          text: 'hi',
          onBtn: () => {
            this.$router.push({ path: '/' });
          }
        },
        {
          text: 'hi2',
          onBtn: () => {
            this.$router.push({ path: '/' });
          }
        },
      ],
      iconBtnGroup: [
        {
          icon: 'mdi-heart',
          text: 'hi',
          onBtn: () => {
            this.$router.push({ path: '/' });
          }
        },
        {
          icon: 'mdi-magnify',
          onBtn: () => {
            this.$router.push({ path: '/' });
          }
        }
      ]
    }
  }
}
</script>

<style scoped>
.mainBar {
  margin-left: 56px;
}
</style>