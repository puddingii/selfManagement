<template>
  <v-btn
    :absolute="absolute"
    :active-class="activeClass"
    :append="append"
    :block="block"
    :bottom="bottom"
    :color="color"
    :dark="dark"
    :depressed="depressed"
    :disabled="disabled"
    :elevation="elevation"
    :exact="exact"
    :exact-active-class="exactActiveClass"
    :exact-path="exactPath"
    :fab="fab"
    :fixed="fixed"
    :height="height"
    :href="href"
    :icon="icon"
    :input-value="inputValue"
    :large="large"
    :left="left"
    :light="light"
    :link="link"
    :loading="loading"
    :max-height="maxHeight"
    :max-width="maxWidth"
    :min-height="minHeight"
    :min-width="minWidth"
    :nuxt="nuxt"
    :outlined="outlined"
    :plain="plain"
    :replace="replace"
    :retain-focus-on-click="retainFocusOnClick"
    :right="right"
    :ripple="ripple"
    :rounded="rounded"
    :shaped="shaped"
    :small="small"
    :tag="tag"
    :target="target"
    :text="text"
    :tile="tile"
    :to="to"
    :top="top"
    :type="type"
    :value="value"
    :width="width"
    :x-large="xLarge"
    :x-small="xSmall"
    @click="onButton"
  >
    <slot />
  </v-btn>
</template>

<script>
export default {
  props: {
    absolute: {
      type: Boolean,
      default: false
    },
    activeClass: {
      type: String,
      default: ''
    },
    append: {
      type: Boolean,
      default: false
    },
    block: {
      type: Boolean,
      default: false
    },
    bottom: {
      type: Boolean,
      default: false
    },
    color: {
      type: String,
      default: undefined
    },
    dark: {
      type: Boolean,
      default: false
    },
    depressed: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: false
    },
    elevation: {
      type: [Number, String],
      default: undefined
    },
    exact: {
      type: Boolean,
      default: false
    },
    exactActiveClass: {
      type: String,
      default: undefined
    },
    exactPath: {
      type: Boolean,
      default: false
    },
    fab: {
      type: Boolean,
      default: false
    },
    fixed: {
      type: Boolean,
      default: false
    },
    height: {
      type: [Number, String],
      default: undefined
    },
    href: {
      type: [String, Object],
      default: undefined
    },
    icon: {
      type: Boolean,
      default: false
    },
    inputValue: {
      type: any,
      default: undefined
    },
    large: {
      type: Boolean,
      default: false
    },
    left: {
      type: Boolean,
      default: false
    },
    light: {
      type: Boolean,
      default: false
    },
    link: {
      type: Boolean,
      default: false
    },
    loading: {
      type: Boolean,
      default: false
    },
    maxHeight: {
      type: [Number, String],
      default: undefined
    },
    maxWidth: {
      type: [Number, String],
      default: undefined
    },
    minHeight: {
      type: [Number, String],
      default: undefined
    },
    minWidth: {
      type: [Number, String],
      default: undefined
    },
    nuxt: {
      type: Boolean,
      default: false
    },
    outlined: {
      type: Boolean,
      default: false
    },
    plain: {
      type: Boolean,
      default: false
    },
    replace: {
      type: Boolean,
      default: false
    },
    retainFocusOnClick: {
      type: Boolean,
      default: false
    },
    right: {
      type: Boolean,
      default: false
    },
    ripple: {
      type: [Boolean, Object],
      default: undefined
    },
    rounded: {
      type: Boolean,
      default: false
    },
    shaped: {
      type: Boolean,
      default: false
    },
    small: {
      type: Boolean,
      default: false
    },
    tag: {
      type: String,
      default: 'button'
    },
    target: {
      type: String,
      default: undefined
    },
    text: {
      type: Boolean,
      default: false
    },
    tile: {
      type: Boolean,
      default: false
    },
    to: {
      type: [String, Object],
      default: undefined
    },
    top: {
      type: Boolean,
      default: false
    },
    type: {
      type: String,
      default: 'button'
    },
    value: {
      type: any,
      default: undefined
    },
    width: {
      type: [Number, String],
      default: undefined
    },
    xLarge: {
      type: Boolean,
      default: false
    },
    xSmall: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    onButton(event) {
      this.$emit('onButton', event);
    }
  }
}
</script>

<style>

</style>