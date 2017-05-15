<template>
<div>
  <todo-list v-bind:todos="todos"></todo-list>
  <!--<div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
  </div>-->
  <ul>
    <todo v-bind:todo="todo" v-for="todo in todos"></todo>
  </ul>
</div>
</template>

<script>
  import TodoList from './components/TodoList';
  import Todo from './components/Todo';
  
  export default {
    name: 'app',
    components: {
      // Add a reference to the TodoList component in the components property
      TodoList,
      Todo,
    },
    data() {
      return {
        todos: [{
          title: 'Todo A',
          project: 'Project A',
          done: false,
        }, {
          title: 'Todo B',
          project: 'Project B',
          done: true,
        }, {
          title: 'Todo C',
          project: 'Project C',
          done: true,
        }, {
          title: 'Todo D',
          project: 'Project D',
          done: false,
        }],
      };
    },
  };

</script>

<style>
body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #222;
  /*margin-top: 60px;*/
}
</style>
