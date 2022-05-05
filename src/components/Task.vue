<template>
  <v-app>

    <li>
      <div><slot></slot>{{ index }}</div>
      <small>{{ task.dueDate }} @ {{task.dueTime}}</small>
<button @click="deleteTask(index)" >X</button>
    </li>

  </v-app>
</template>

<script>

export default {
props: ['task', 'index']
}
</script>
<style scoped>

</style>
