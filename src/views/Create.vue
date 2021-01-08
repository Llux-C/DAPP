<template>
  <el-form ref="form" :model="form" label-width="80px">
    <el-form-item label="项目名称">
      <el-input v-model="form.name"></el-input>
    </el-form-item>
    <el-form-item label="众筹金额">
      <el-input v-model="form.sum"></el-input>
    </el-form-item>
    <el-form-item label="项目介绍">
      <el-input v-model="form.introduction"></el-input>
    </el-form-item>
    <el-form-item label="截止时间">
      <el-col :span="11">
        <el-date-picker
          type="date"
          placeholder="选择日期"
          v-model="form.date1"
          style="width: 100%"
        ></el-date-picker>
      </el-col>
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="onSubmit">立即创建</el-button>
      <el-button>取消</el-button>
    </el-form-item>
  </el-form>
</template>
<script>
export default {
  data() {
    return {
      form: {
        name: "",
        sum: "",
        introduction: "",
        date1: "",
      },
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    },
  },
};
</script>