<template>
<div>
  <div>{{ msg }} 年龄{{ age }}</div>
  <div>小明的爸爸年龄{{parent}}</div>
  <a-button type="primary" @click="add">
    添加
  </a-button>
</div>
</template>

<script>
import {
  ref,
  computed
} from 'vue';
export default {
  name: 'App',
  setup() {
    const msg = ref('小明');
    const age = ref(18);
    const parent = computed(() => (age.value * 2))
    const add = () => {
      age.value += 1;
    };
    return {
      msg,
      age,
      add,
      parent
    };
  },
};
</script>

<style></style>
