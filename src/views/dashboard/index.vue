<template>
  <div class="dashboard-container">

    
    <!-- <div class="dashboard-text">name: {{ name }}</div> -->
  <el-table :data="tableData" style="width: 100%">
   <el-table-column type="selection" width="55"> </el-table-column>

    <el-table-column label="序号" width="95" align="center">
      <template slot-scope="scope">
        <span style="margin-left: 10px">1</span>
      </template>
    </el-table-column>

    <el-table-column label="名称" width="150" align="center">
      <template slot-scope="scope">
        <span style="margin-left: 10px">{{ scope.row.date }}</span>
      </template>
    </el-table-column>

    <el-table-column label="角色" width="150" align="center">
      <template slot-scope="scope">
        <i class="el-icon-time"></i>
        <span style="margin-left: 10px">{{ scope.row.date }}</span>
      </template>
    </el-table-column>

    <el-table-column label="状态" width="130" align="center">
      <template slot-scope="scope">
        <i class="el-icon-time"></i>
        <span style="margin-left: 10px">{{ scope.row.date }}</span>
      </template>
    </el-table-column>

    <el-table-column label="创建时间" width="150" align="center">
      <template slot-scope="scope">
        <i class="el-icon-time"></i>
        <span style="margin-left: 10px">{{ scope.row.date }}</span>
      </template>
    </el-table-column>

    <el-table-column label="更新时间" width="150" align="center">
      <template slot-scope="scope">
        <i class="el-icon-time"></i>
        <span style="margin-left: 10px">{{ scope.row.date }}</span>
      </template>
    </el-table-column>

    <el-table-column label="操作" align="center">
      <template slot-scope="scope">
        <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
        <el-button size="mini" @click="">启用</el-button>
        <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
      data() {
      return {
        tableData:[{
          
        }]
      }
    },
  computed: {
    ...mapGetters([
      'name'
    ])
  },
    methods: {
      handleEdit(index, row) {
        console.log(index, row);
      },
      handleDelete(index, row) {
        console.log(index, row);
      }
    }
  
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
