<script setup lang="ts">
import { ref } from "vue";
import { ElMessage } from "element-plus";

defineProps<{ msg: string }>();

const count = ref(0);
const input = ref("element-plus");

const curDate = ref("");

const toast = () => {
  ElMessage.success("Hello");
};
</script>

<template>
  <h2>未设置宽度 100%</h2>
  <el-date-picker
      class="m-2"
      v-model="curDate"
      type="date"
      placeholder="Pick a day"
  ></el-date-picker>
  <h2>宽度 100%</h2>
  <el-date-picker
      style="width: 100%"
      class="m-2"
      v-model="curDate"
      type="date"
      placeholder="Pick a day"
  ></el-date-picker>
</template>

<style>
.m-2{
  border: 1px solid #db2828;
}
.ep-button {
  margin: 4px;
}
.ep-button + .ep-button {
  margin-left: 0;
  margin: 4px;
}
</style>
