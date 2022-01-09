<template>
  <div>
    <TTopNavigation :page-title="pageTitle" />
    <Todo />
  </div>
</template>

<script>
import TTopNavigation from '~/components/templates/TTopNavigation.vue';
import Todo from '~/components/todo/Todo.vue';

export default {
  components: {
    TTopNavigation,
    Todo
  },
  layout: 'LeftNavigation',
  data () {
    return {
      pageTitle: 'Home'
    }
  },
}
</script>

<style>

</style>
