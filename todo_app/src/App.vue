<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <draggable element="ul" class="list-group">
          <li class="list-group-item" v-for="task in tasks" :key="task">
            {{ task }}
          </li>
        </draggable>
      </div>
      <div class="col">
        <draggable element="ul" class="list-group">
          <li class="list-group-item" v-for="urgentTask in urgentTasks" :key="urgentTask">
            {{ urgentTask }}
          </li>
        </draggable>
      </div>
    </div>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import draggable from "vuedraggable";
export default {
  name: "app",
  components: {
    draggable,
  },
  data() {
    return {
      tasks: ["task1", "task2", "task3", "task4"],
      urgentTasks: ["urgentTask1", "urgentTask2", "urgentTask3", "urgentTask4"],
    };
  },
};
</script>