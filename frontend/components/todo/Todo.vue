<template>
  <div class="d-flex justify-space-around mb-6">
    <DayTodo />
    <MonthTodo />
    <YearTodo />
  </div>
</template>

<script>
import DayTodo from '~/components/todo/dayTodo/DayTodo.vue';
import MonthTodo from '~/components/todo/monthTodo/MonthTodo.vue';
import YearTodo from '~/components/todo/yearTodo/YearTodo.vue';

export default {
  name: 'Todo',
  components: {
    DayTodo,
    MonthTodo,
    YearTodo
  }
}
</script>

<style>

</style>