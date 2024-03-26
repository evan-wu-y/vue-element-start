<script setup lang="ts">
import { ElMessage, ElMessageBox } from 'element-plus'

import { useToggleDark } from '@/composables'

const showMessage = () => {
  ElMessageBox.confirm('proxy will permanently delete the file. Continue?', 'Warning', {
    confirmButtonText: 'OK',
    cancelButtonText: 'Cancel',
    confirmButtonClass: 'es-button--danger'
  })
    .then(() => {
      ElMessage({
        type: 'success',
        message: 'Delete completed'
      })
    })
    .catch(() => {
      ElMessage({
        type: 'info',
        message: 'Delete canceled'
      })
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
