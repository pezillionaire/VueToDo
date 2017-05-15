<template>

    <li>
      <header>{{ todo.title }}</header>
      <section>{{ todo.project }}</section>
      <button v-bind:class="todo.done ? 'done' : 'not-done'" v-on:click="todo.done = !todo.done" > {{ todo.done ? "Done!" : "Complete?"}}</button>
    </li>

</template>

<script>
  export default {
    props: ['todo'],
  };
</script>
