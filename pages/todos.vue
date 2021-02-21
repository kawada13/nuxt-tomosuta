<template>
  <div style="margin: 20px">
    <input type="text" placeholder="タスクの追加" @keyup.enter="addTodo">
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  methods: {
    addTodo(e) {
      this.$store.commit('todos/add', e.target.value)
    }
  }

}
</script>

<style>

</style>