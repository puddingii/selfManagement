<template>
  <v-container class="grey lighten-5">
    <v-row no-gutters class="todoContent">
      <v-col
        cols="12"
        sm="4"
      >
        <YearTodo />
      </v-col>
      <v-col
        cols="12"
        sm="4"
      >
        <MonthTodo />
      </v-col>
      <v-col
        cols="12"
        sm="4"
      >
        <DayTodo />
      </v-col>
    </v-row>
  </v-container>
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

<style scoped>
.todoArea {
  margin-top: 10px;
}
.todoContent {
  min-height: 100vh;
}
</style>