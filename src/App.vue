<script>
  export default {
    data () {
      return {
        name: 'Ata',
        status: '',
        tasks: ['task 1', 'task 2', 'task 3'],
        link: 'https://www.google.com'
      }
    }
  }
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <h3>Tasks: </h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <a :href="link">Click for Google</a>
</template>