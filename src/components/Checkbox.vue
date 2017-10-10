<template>
  <div>
    <h3>复选框</h3>
    <div>
      1、基础用法和禁用状态
      <br>
      <el-checkbox v-model="checked">备选项</el-checkbox>
      <el-checkbox v-model="checked1" disabled>备选项1</el-checkbox>
      <el-checkbox v-model="checked2" disabled>备选项</el-checkbox>
    </div>
    <br>
    <div>
      2、多选框组
      <br>
      <el-checkbox-group v-model="checkList">
        <el-checkbox label="复选框A"></el-checkbox>
        <el-checkbox label="复选框B"></el-checkbox>
        <el-checkbox label="复选框C"></el-checkbox>
        <el-checkbox label="复选框D"></el-checkbox>
        <el-checkbox label="禁用" disabled>禁用选项</el-checkbox>
        <el-checkbox label="禁用且选中" disabled>禁用且选中</el-checkbox>
      </el-checkbox-group>
    </div>
    <br>
    <div>
      3、可选项目数量的控制
      <br>
      <el-checkbox-group v-model="checkedCities1" :min="1" :max="3">
        <el-checkbox v-for="city in cities" :label="city" :key="city">{{ city }}</el-checkbox>
      </el-checkbox-group>
    </div>
    <br>
    <div>
      4、indeterminate状态
      <br>
      <el-checkbox :indeterminate="isIndeterminate" v-model="checkAll" @change="handleCheckAllChange">全选</el-checkbox>
      <br>
      <el-checkbox-group v-model="checkedCities2" @change="handleCheckedCitiesChange">
        <el-checkbox v-for="city in cities" :label="city">{{ city }}</el-checkbox>
      </el-checkbox-group>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cities: {
      type: Array,
      default: ['北京']
    }
  },
  data () {
    return {
      checked: true,
      checked1: false,
      checked2: true,

      checkList: ['复选框A', '禁用且选中'],

      checkedCities1: [this.cities[0]],
      checkedCities2: [this.cities[0]],
      checkAll: true,
      isIndeterminate: true
    }
  },
  methods: {
    handleCheckAllChange (event) {
      this.checkedCities2 = event.target.checked ? this.cities : []
      this.isIndeterminate = false
    },
    handleCheckedCitiesChange (value) {
      console.log(value)
      let checkedCount = value.length
      this.checkAll = checkedCount === this.cities.length
      this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length
    }
  }
}
</script>

<style>

</style>
