<script>
  export default {

    data() {

      return {
        name: 'Mirza Junaid',
        status: 'pending',
        tasks:['Task-one','task-two','Task-three'],
        link:'https://google.com'
      };
    },
  };

</script>



<template>
  <h1>{{ name }}</h1>
  <p v-if="status==='active'">User is Active</p>
  <p v-else-if="status==='pending'">User is pending</p>
  <p v-else>User is InActive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" v-bind:key="task">{{ task }}</li>
    
  </ul>
  <a v-bind:href="link">Google</a>
</template>

<style scoped>

</style>
