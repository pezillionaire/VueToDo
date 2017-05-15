<template>
<div>
  <p>Completed Tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
  <p>Pending Tasks: {{todos.filter(todo => {return todo.done === false}).length}}</p>
  <ul>
    <todo v-for="todo in todos" v-bind:todo="todo"></todo>
  </ul>

</div>


</template>

<script>

  import Todo from './Todo';

  export default {
    props: ['todos'],
    components: {
      Todo,
    },
  };
</script>

<style>
  ul {
    margin: 0 auto;
    padding: 0;
    list-style: none;
    text-align: center;
    } 
  li {
    display: block;
    border: 1px solid black;
    border-radius: 0.5em;
    background: #f2f2f2;
    padding: 1em;
    margin: 0.5em;
    max-width: 20em;
  }
  header {
    text-align: center;
    font-weight: bold;
    font-size: 1.5em;
  }
  button {
    background: green;
    color: white;
    border: none;
    border-radius: 0.25em;
    padding: 0.5em;
    }
  .done { background: green; }
  .not-done { background: red; }
</style>
