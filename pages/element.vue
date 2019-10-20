<template name="component-name">
  <div style="padding: 30px;">
    <el-button @click="visible = true">Open Dialog</el-button>
    <el-dialog :visible.sync="visible" title="確認">
    <p>Fix!!</p>
    </el-dialog>
  </div>
</template>


<script>
export default {
  data: function() {
    return {
      visible: false
    }
  }
};
</script>
