<script lang="ts" setup>
import { computed, defineProps, defineEmits } from 'vue'

const props = defineProps<{ modelValue: { name: string; school: string; } }>()

const emit = defineEmits(['update:modelValue'])

const value = computed({
  get() {
    return props.modelValue
  },
  set(value) {
    emit('update:modelValue', value)
  }
})
</script>

<template>
  <form action="/" method="post">
    <div>
      <label for="input0539a394">姓名</label>
      <input type="text" v-model="value.name" id="input0539a394" placeholder="请输入姓名">
    </div>
    <div>
      <label for="input736a7518">学校</label>
      <input type="text" v-model="value.school" id="input736a7518" placeholder="请输入学校">
    </div>
  </form>
</template>