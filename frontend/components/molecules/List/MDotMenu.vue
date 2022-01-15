<template>
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
        v-for="(itemInfo, i) in itemGroup"
        :key="i"
        @click="itemInfo.onBtn"
      >
        <v-list-item-title>{{ itemInfo.text }}</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  props: {
    itemGroup: {
      type: Array,
      default: new Array()
    }
  },
}
</script>

<style>

</style>