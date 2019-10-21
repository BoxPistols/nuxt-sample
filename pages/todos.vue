<template name="component-name">
  <div>
    <el-row type="flex" justify="center">
      <el-col :span="12">
        <input placeholder="input" @keyup.enter="addTodo">
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  methods: {
    addTodo(e) {
      this.$store.commit('todos/add', e.target.value)
    }
  },
};
</script>


<style>
input{
  font-size: 24px
}
</style>
