<template>
  <el-table
    :data="tableData"
    stripe
    height=550px
    style="width: 100%">
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
        tableData: []
      }
    },
    mounted(){
      fetch("test.json")
      .then(res=>{
      console.log(res)
      return res.json()
      })
      .then(data=>{
      console.log(data,this)
      this.tableData=data.filter(function(e){return e.status==1})
      })
    }
  }
</script>