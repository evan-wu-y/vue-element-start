<script setup lang="ts">
import { ElNotification } from 'element-plus'

const showMessage = () => {
  ElNotification({
    title: 'Hello',
    type: 'success',
    message: 'This is a notification message'
  })
}
const visible = ref(false)
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <el-button type="primary" @click="showMessage">Click Me</el-button>
    <el-button type="primary" @click="visible = !visible">Click Me</el-button>
  </div>
  <div>
    <el-dialog v-model="visible">
      <p>Some contents...</p>
    </el-dialog>
  </div>
</template>

<style></style>
