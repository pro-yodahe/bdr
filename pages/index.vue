<template>
    <div>
      <h1>Employee Directory</h1>
      {{query}}
      <div  class="employee-list">
        <ul>
          <li v-for="employee in employees" :key="employee.id">
            <strong>{{ employee.name }}</strong> - {{ employee.position }}
            <br />
            Department: {{ employee.department }}
            <br />
            Email: {{ employee.email }}
          </li>
        </ul>
      </div>
    </div>
  </template>

<script setup>// Set up reactive state for employees, loading, and error
const query = await useAsyncQuery (gql`
query MyQuery {
  Employee {
    branch
    deparmtment
    email
    Id
  }
}


`)
console.log(query)

</script>

<style scoped>
/* Add your styles here */
</style>