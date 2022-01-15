<template>
  <v-list nav dense>
    <MListItem
      v-for="(item, i) in naviItemList"
      :key="i"
      :link="true"
      :icon-src="item.icon"
      :text="item.text"
      class-name="px-2"
    />  
  </v-list>
</template>

<script>
import MListItem from '~/components/molecules/list/MListItem.vue';

export default {
  name: 'OVerticalNavigation',
  components: {
    MListItem
  },
  props: {
    naviItemList: {
      type: Array,
      default: new Array
    }
  },
  data() {
    return {
      
    }
  },
  methods: {
    onCard(event) {
      this.$emit('onCard', event);
    }
  }
}
</script>

<style>

</style>