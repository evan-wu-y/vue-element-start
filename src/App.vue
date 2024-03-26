<template>
  <el-config-provider namespace="es">
    <header class="flex items-center gap-5">
      <router-link to="/">home</router-link>
      <router-link to="/about">about</router-link>
    </header>
    <RouterView />
  </el-config-provider>
</template>

<style scoped></style>
