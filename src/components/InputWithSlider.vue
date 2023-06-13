<script setup>
import { ref, watch } from 'vue'

const props = defineProps(['modelValue'])

const value = ref(props.modelValue)

const emit = defineEmits(['update:modelValue'])

watch(
  () => props.modelValue,
  () => {
    value.value = props.modelValue
  }
)

function onInput(value) {
  emit('update:modelValue', parseInt(value))
}

function onSliderInput(value) {
  emit('update:modelValue', parseInt(value))
}
</script>
<template>
  <div>
    <el-input
      class="square-slider"
      v-model="value"
      @input="onInput"
      type="number"
      max="200"
      min="0"
    >
      <template #suffix>
        <span>м<sup>2</sup></span>
      </template>
    </el-input>
    <div class="slider-block">
      <el-slider v-model="value" @input="onSliderInput" :max="100" />
    </div>
  </div>
</template>

<style scoped>
.square-slider {
  height: 55px;
  width: 100%;
  border: 1px solid #818181;
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.17);
  border-radius: 60px;
  position: relative;

  color: #fff;
  text-align: center;

  --el-input-bg-color: transparent;
  --el-input-border-radius: 60px;
  --el-input-border-color: rgba(0, 0, 0, 0.17);
}
.slider-block {
  position: absolute;
  align-items: center;
  left: 0;
  right: 0;
  margin-left: 25px;
  margin-right: 25px;
  top: 100%;
  transform: translateY(-50%);
}

.slider-block ::v-deep(.el-slider) {
  --el-slider-runway-bg-color: transparent;
  --el-slider-height: 1px;
  --el-slider-button-wrapper-offset: -18px;
  --el-slider-button-size: 19px;
  --el-slider-main-bg-color: #2168de;
  --el-color-white: #2168de;
}

.slider-block ::v-deep(.el-slider__button) {
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.13);
  backdrop-filter: blur(7.5px);
  border: 4px solid rgb(75, 75, 75);
}

::v-deep(.el-input__wrapper) {
  justify-content: flex-start;
  padding-left: 18px;
}

::v-deep(.el-input__inner) {
  flex-shrink: 1;
  flex-grow: 0;
  width: fit-content;
  color: #fff;
  opacity: 0.7;
}

::v-deep(.el-input__suffix-inner > :first-child) {
  margin-left: 0;
  margin-top: -5px;
  color: #fff;
  opacity: 0.7;
}

/* Chrome, Safari, Edge, Opera */
.square-slider ::v-deep(input::-webkit-outer-spin-button),
.square-slider ::v-deep(input::-webkit-inner-spin-button) {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
.square-slider ::v-deep(input[type='number']) {
  -moz-appearance: textfield;
}
</style>
