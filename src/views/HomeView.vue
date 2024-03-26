<script setup lang="ts">
import { ElMessage } from 'element-plus'

import { useToggleDark } from '@/composables'

const showMessage = () => {
  ElMessage({
    message: 'Hello, ElMessage!',
    type: 'success',
    grouping: true
  })
}
</script>

<template>
  <main>
    <h1>Welcome</h1>
    <el-button type="primary" @click="showMessage">Click Me</el-button>
    <el-button type="primary" @click="useToggleDark">Click Me</el-button>
    <el-input>
      <template #prepend>
        <el-icon>
          <IEpSearch />
        </el-icon>
      </template>
    </el-input>
  </main>
</template>
