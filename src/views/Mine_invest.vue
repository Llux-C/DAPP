<template>
  <el-table
    :data="tableData"
    stripe
    height=:calc(100vh-140px)
    style="width: 100%">
    <!-- 注意这里，calc函数内部不能有空格，减号前后尤其不能有，不然会崩溃-->
    <el-table-column
      prop="name"
      label="项目名称"
      width="180">
    </el-table-column>
    <el-table-column
      prop="sum"
      label="众筹金额"
      width="180">
    </el-table-column>
    <el-table-column
      prop="introduction"
      label="项目介绍">
    </el-table-column>
    <el-table-column
      prop="date"
      label="截止时间"
      width="180">
    </el-table-column>
     <el-table-column
      fixed="right"
      label="操作"
      width="100">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="fault">投票确认</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
  export default {
    data() {
      return {
        tableData: [{
          name: '众筹',
          sum: '10ETH',
          introduction: '这是项目介绍',
          date: '2022.01.01'
        },
        {
          name: '众筹',
          sum: '10ETH',
          introduction: '这是项目介绍',
          date: '2022.01.01'
        },
        {
          name: '众筹',
          sum: '10ETH',
          introduction: '这是项目介绍',
          date: '2022.01.01'
        },
        {
          name: '众筹',
          sum: '10ETH',
          introduction: '这是项目介绍',
          date: '2022.01.01'
        }
        ]
      }
    }
  }
</script>