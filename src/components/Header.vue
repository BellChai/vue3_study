<template>
  <div style="height: 50px; line-height: 50px; border-bottom: 1px solid #ccc; display:flex">
    <div style="width: 200px; padding-left: 30px; font-weight: bold; color: dodgerblue;">后台管理</div>
    <div style="flex:1"></div>
    <div style="width: 200px; display: flex; align-items: center;">
      <el-dropdown>
        <span class="el-dropdown-link">
          柴艺函
          <el-icon class="el-icon--right">
            <arrow-down />
          </el-icon>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>Action 1</el-dropdown-item>
            <el-dropdown-item>Action 2</el-dropdown-item>
            <el-dropdown-item>Action 3</el-dropdown-item>
            <el-dropdown-item disabled>Action 4</el-dropdown-item>
            <el-dropdown-item divided>Action 5</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
  </div>

</template>

<!-- <script lang="ts" setup>
// import { ArrowDown } from '@element-plus/icons-vue';

</script> -->

<script>
import { ArrowDown } from '@element-plus/icons-vue';

export default {
  name: 'Header',
  components: {
    ArrowDown,
  },
  props: {
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.example-showcase .el-dropdown-link {
  cursor: pointer;
  color: var(--el-color-primary);
  display: flex;
  align-items: center;
}
</style>
