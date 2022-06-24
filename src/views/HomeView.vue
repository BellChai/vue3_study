<template>
  <div>
    <div style="margin: 10px 0">
      <el-button>新增</el-button>
      <el-button>按钮</el-button>
      <el-button>导入</el-button>
    </div>
    <!-- 搜索区域 -->
    <div style="margin: 10px 0">
      <el-input v-model="search" placeholder="请输入关键字" style="width: 20%"></el-input>
      <el-button>查询</el-button>
    </div>
    <!-- 表格 -->
    <el-table :data="tableData">
      <el-table-column prop="date" label="日期" />
      <el-table-column prop="name" label="姓名" />
      <el-table-column prop="address" label="地址" />
      <el-table-column fixed="right" label="操作">
        <template #default>
          <el-popconfirm confirm-button-text="确认" cancel-button-text="点错了" :icon="InfoFilled" icon-color="#626AEF"
            title="你确定要删除这一条信息？">
            <template #reference>
              <el-button @click="handleClick(scope.row)" type="text">删除</el-button>
            </template>
          </el-popconfirm>
          <el-button link type="primary">编辑</el-button>
        </template>
      </el-table-column>
    </el-table>

    <div class="demo-pagination-block">
      <!-- <div class="demonstration">到</div> -->
      <el-pagination v-model:currentPage="currentPage" v-model:page-size="pageSize" :page-sizes="[10, 100, 200, 300, 400]"
        :small="small" :disabled="disabled" :background="background" layout="sizes, prev, pager, next, total, jumper"
        :total="total" @size-change="handleSizeChange" @current-change="handleCurrentChange" />
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'
import { InfoFilled } from '@element-plus/icons-vue'

export default {
  name: 'HomeView',
  components: {
    ref,
    InfoFilled,
  },
  data() {
    return {
      currentPage: 1,
      total: 1000,
      search: ref(''),
      tableData: [
        {
          date: '2016-05-03',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-02',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-04',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
      ]
    }
  },
  methods: {
    handleClick: function (row) {
      // 
    },
    handleSizeChange: function (val) {
      console.log(`${val} items per page`)
    },
    handleCurrentChange: function (val) {
      console.log(`current page: ${val}`)
    },
  }
}
</script>

<style scoped>

</style>
