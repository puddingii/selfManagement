<template>
  <div>
    <v-alert class="todoTitle" text dense color="green">DayTodo</v-alert>
    <v-container>
      <v-text-field
        v-model="newTask"
        label="What are you working on?"
        solo
        @keydown.enter="create"
      >
        <template #append>
          <v-fade-transition>
            <v-icon
              v-if="newTask"
              @click="create"
            >
              add_circle
            </v-icon>
          </v-fade-transition>
        </template>
      </v-text-field>

      <v-progress-linear
        v-model="progress"
        color="teal lighten-3"
        height="25"
      >
        <template #default="{ value }">
          <strong>{{ Math.ceil(value) }}%</strong>
        </template>
      </v-progress-linear>

      <v-divider class="mt-4" />

      <v-row
        class="my-1"
        align="center"
      >
        <strong class="mx-4 info--text text--darken-2">
          Remaining: {{ remainingTasks }}
        </strong>

        <v-divider vertical />

        <strong class="mx-4 success--text text--darken-2">
          Completed: {{ completedTasks }}
        </strong>

        <v-spacer />
      </v-row>

      <v-divider class="mb-4" />

      <v-card v-for="(task, i) in tasks" :key="i">
        <v-divider v-if="i !== 0" />
      </v-card>

      <v-card v-if="tasks.length > 0">
        <v-slide-y-transition
          class="py-0"
          group
          tag="v-list"
        >
          <template v-for="(task, i) in tasks">
            <v-divider
              v-if="i !== 0"
              :key="`${i}-divider`"
            />
            <v-badge 
              :key="`${i}-${task.text}`" 
              left 
              overlap 
              icon="mdi-close" 
              color="red" 
              @click.native="onCloseBadge"
            >
              <v-list-item>
                <v-list-item-action>
                  <v-checkbox
                    v-model="task.done"
                    :color="task.done && 'grey' || 'primary'"
                  >
                    <template #label>
                      <div
                        :class="task.done && 'grey--text' || 'primary--text'"
                        class="ml-4"
                        v-text="task.text"
                      />
                      <AButton :icon="true">
                        <v-icon>mdi-pencil</v-icon>
                      </AButton>
                    </template>
                  </v-checkbox>
                </v-list-item-action>

                <v-spacer />

                <v-scroll-x-transition>
                  <v-icon
                    v-if="task.done"
                    color="success"
                  >
                    mdi-check
                  </v-icon>
                </v-scroll-x-transition>
              </v-list-item>
            </v-badge>
          </template>
        </v-slide-y-transition>
      </v-card>
    </v-container>
  </div>
</template>

<script>
import AButton from '~/components/atoms/button/AButton.vue';

export default {
  name: 'DayTodo',
  components: {
    AButton
  },
  data() {
    return {
      tasks: [],
      todoController: [
        {
          text: 'edit',
          onBtn: () => {
            console.log("edit");
          }
        },
        {
          text: 'delete',
          onBtn: () => {
            console.log("delete");
          }
        },
      ],
      newTask: null,
    }
  },
  computed: {
      completedTasks () {
        return this.tasks.filter(task => task.done).length
      },
      progress () {
        return this.completedTasks / this.tasks.length * 100
      },
      remainingTasks () {
        return this.tasks.length - this.completedTasks
      },
    },
    methods: {
      create () {
        this.tasks.push({
          done: false,
          text: this.newTask,
        })

        this.newTask = null
      },
      onCloseBadge() {
        console.log("close");
      }
    },
}
</script>

<style scoped>
.todoTitle{
  text-align: center;
}
</style>