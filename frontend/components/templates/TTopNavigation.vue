<template>
  <v-app-bar
    color="grey lighten-5"
  >
    <v-toolbar-title>{{ pageTitle }}</v-toolbar-title>

    <v-spacer />

    <AButton v-for="(btnInfo, i) in iconBtnGroup" :key="i" @click="btnInfo.onBtn">
      <v-icon>{{ btnInfo.icon }}</v-icon>
      {{ btnInfo.text }}
    </AButton>

    <v-menu
      left
      bottom
    >
      <template #activator="{ on, attrs }">
        <v-btn
          icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="(itemInfo, i) in dropdownItemGroup"
          :key="i"
          @click="itemInfo.onBtn"
        >
          <v-list-item-title>{{ itemInfo.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script>
import AButton from "~/components/atoms/button/AButton.vue";

export default {
  components: {
    AButton
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

<style>

</style>