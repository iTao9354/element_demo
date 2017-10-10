<template>
  <div>
    <h3>单选框</h3>
    <div>
      1、基础用法
      <div>
        <el-radio class="radio" v-model="radio" label="1">备选项</el-radio>
        <el-radio class="radio" v-model="radio" label="2">备选项</el-radio>
      </div>
    </div>
    <br>
    <div>
      2、禁用状态
      <div>
        <el-radio disabled v-model="radio1" label="禁用">备选项</el-radio>
        <el-radio disabled v-model="radio1" label="选中且禁用">备选项</el-radio>
      </div>
    </div>
    <br>
    <div>
      3、单选框组
      <div>
        <el-radio-group v-model="radio2">
          <el-radio :label="3">备选项</el-radio>
          <el-radio :label="6">备选项</el-radio>
          <el-radio :label="9">备选项</el-radio>
        </el-radio-group>
      </div>
    </div>
    <br>
    <div>
      4、按钮样式
      <div>
        <el-radio-group v-model="radio4">
          <el-radio-button label="bj">北京</el-radio-button>
          <el-radio-button label="sh">上海</el-radio-button>
          <el-radio-button label="gz">广州</el-radio-button>
          <el-radio-button label="tj">天津</el-radio-button>
        </el-radio-group>
        <el-radio-group v-model="radio5">
          <el-radio-button label="bj">北京</el-radio-button>
          <el-radio-button label="sh" disabled>上海</el-radio-button>
          <el-radio-button label="gz">广州</el-radio-button>
          <el-radio-button label="tj" :disabled="true">天津</el-radio-button>
        </el-radio-group>
        <el-radio-group v-model="radio6" disabled>
          <el-radio-button label="bj">北京</el-radio-button>
          <el-radio-button label="sh">上海</el-radio-button>
          <el-radio-button label="gz">广州</el-radio-button>
          <el-radio-button label="tj">天津</el-radio-button>
        </el-radio-group>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      radio: '1',

      radio1: '选中且禁用',

      radio2: 3,

      radio4: 'bj',

      radio5: 'bj',

      radio6: 'bj'
    }
  }
}
</script>

<style>

</style>
