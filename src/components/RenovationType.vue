<script setup>
import { ref } from 'vue'
const renovationType = ref('1')

const select = ref()

const options = [
  {
    value: '1',
    label: 'Черновой'
  },
  {
    value: '2',
    label: 'Чистовой'
  },
  {
    value: '3',
    label: 'Дизайнерский'
  }
]

function onVisibleChange(show) {
  if (show) {
    select.value.$el.scrollIntoView({
      behavior: 'smooth',
      block: 'center'
    })
  }
}
</script>
<template>
  <div class="rennovation-type">
    <div class="calculator-title">Какой ремонт хотите?</div>
    <el-select
      v-model="renovationType"
      class="m-2"
      placeholder="Select"
      size="large"
      :teleported="false"
      popper-class="renovation-popper"
      :fit-input-width="true"
      @visible-change="onVisibleChange"
      ref="select"
    >
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value"
      />
    </el-select>
  </div>
</template>

<style scoped>
.rennovation-type > * {
  width: 100%;
}

::v-deep(.el-select) {
  --el-border-radius-base: 60px;
  --el-select-input-focus-border-color: #818181;
}

::v-deep(.el-select) .select-trigger {
  z-index: 3000;
}

::v-deep(.el-input__wrapper),
::v-deep(.el-input) {
  --el-input-bg-color: #3a3a3a;
  --el-input-text-color: #fff;
  --el-input-border-color: #818181;
  --el-input-hover-border-color: var(--el-input-border-color);
}
</style>
<style>
.el-popper.renovation-popper {
  border-bottom-left-radius: 28px;
  border-bottom-right-radius: 28px;
  position: absolute;
  margin-top: -32px;
}

.renovation-popper .el-scrollbar {
  padding-top: 24px;
  padding-bottom: 16px;
  background-color: #818181;
  border-bottom-left-radius: 28px;
  border-bottom-right-radius: 28px;
  --el-color-primary: #fff;
  --el-text-color-regular: #fff;
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.17);
}

.renovation-popper .el-select-dropdown__item {
  background: none;
}

.renovation-popper .el-popper__arrow {
  display: none;
  top: -40px;
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
