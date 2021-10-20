<template>
  <div class="hello">
    <ol>
      <li v-for="t in todos" :key="t.id">{{ t.title }}</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    todos: Array,
  },
};
</script>

<style scoped lang="scss">

</style>
