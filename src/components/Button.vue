<template>
  <div>
    <h3>按钮</h3>
    <div>
      1、基础用法
      <div>
        <el-button>默认按钮</el-button>
        <el-button type="primary">主要按钮</el-button>
        <el-button type="text">文字按钮</el-button>
      </div>
    </div>
    <br>
    <div>
      2、禁用状态
      <div>
        <el-button :disabled="true">默认按钮</el-button>
        <el-button type="primary" :disabled="true">主要按钮</el-button>
        <el-button type="text" :disabled="true">文字按钮</el-button>
      </div>
    </div>
    <div>
      3、有颜色倾向
      <div class="block">
        <span class="demonstration">默认显示颜色</span>
        <br>
        <span class="wrapper">
          <el-button type="success">成功按钮</el-button>
          <el-button type="warning">警告按钮</el-button>
          <el-button type="danger">危险按钮</el-button>
          <el-button type="info">信息按钮</el-button>
        </span>
      </div>
      <div class="block">
        <span class="demonstration">hover 显示颜色</span>
        <br>
        <span class="wrapper">
          <el-button :plain="true" type="success">成功按钮</el-button>
          <el-button :plain="true" type="warning">警告按钮</el-button>
          <el-button :plain="true" type="danger">危险按钮</el-button>
          <el-button :plain="true" type="info">信息按钮</el-button>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
