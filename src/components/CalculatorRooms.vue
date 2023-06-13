<script setup>
import { ref } from 'vue'
const rooms = ref('1')
</script>
<template>
  <div class="calculator-radio">
    <div class="calculator-title">Количество комнат:</div>
    <el-radio-group v-model="rooms" size="large">
      <el-radio-button label="1" />
      <el-radio-button label="2" />
      <el-radio-button label="3" />
      <el-radio-button label="4+" />
    </el-radio-group>
  </div>
</template>

<style scoped>
::v-deep(.el-radio-button) .el-radio-button__inner {
  border-radius: 100%;
  border-left: var(--el-border);
  width: 55px;
  height: 55px;
  line-height: 27px;
}

::v-deep(.el-radio-group) {
  gap: 5px;

  --el-button-bg-color: transparent;
  --el-border: 1px solid #818181;
}

::v-deep(.el-radio-button__inner) {
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.17);
}

::v-deep(.el-radio-button__original-radio:checked + .el-radio-button__inner) {
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.17);
}

.calculator-title {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  color: #fff;
  padding-bottom: 10px;
}
</style>
