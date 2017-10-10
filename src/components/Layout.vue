<template>
  <div class="container">
    <h3>布局</h3>
    <el-row>
      <el-col :span="24"><div class="grid-content bg-purple-dark"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="12"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="12"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row :gutter="20">
      <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row :gutter="10">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row :gutter="10">
      <el-col :xs="8" :sm="6" :md="4" :lg="3"><div class="grid-content bg-purple"></div></el-col>
      <el-col :xs="4" :sm="6" :md="8" :lg="9"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :xs="4" :sm="6" :md="8" :lg="9"><div class="grid-content bg-purple"></div></el-col>
      <el-col :xs="8" :sm="6" :md="4" :lg="3"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row class="border-gray">
      <el-col>
        <div class="grid-content">
          <button-com></button-com>
        </div>
      </el-col>
    </el-row>
    <el-row class="border-gray">
      <el-col>
        <div class="grid-content">
          <radio-com></radio-com>
        </div>
      </el-col>
    </el-row>
    <el-row class="border-gray">
      <el-col>
        <div class="grid-content">
          <check-box :cities="cityList"></check-box>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import ButtonCom from './Button'
import RadioCom from './Radio'
import CheckBox from './Checkbox'
export default {
  components: {
    ButtonCom,
    RadioCom,
    CheckBox
  },
  data () {
    return {
      cityList: ['北京', '上海', '广州', '天津']
    }
  }
}
</script>

<style>
  .container {
    padding-bottom: 100px;
  }
  .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .border-gray {
    border: 1px solid #ccc;
    padding: 10px;
  }
</style>
