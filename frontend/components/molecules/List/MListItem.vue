<template>
  <v-list-item :link="link" :href="href" :class="className">
    <v-list-item-avatar v-if="imageSrc">
      <v-img :src="imageSrc" />
    </v-list-item-avatar>

    <v-list-item-icon v-if="iconSrc">
      <v-icon>{{ iconSrc }}</v-icon>
    </v-list-item-icon>

    <v-list-item-content>
      <v-list-item-title>{{ text }}</v-list-item-title>
    </v-list-item-content>
  </v-list-item>
</template>

<script>
export default {
  name: 'MListItem',
  props: {
    link: {
      type: Boolean,
      default: false
    },
    href: {
      type: [String, Object],
      default: undefined
    },
    className: {
      type: String,
      default: ''
    },
    imageSrc: {
      type: String,
      default: ''
    },
    iconSrc: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>

<style>

</style>