<template>
  <div class="common-layout">
    <el-container style="height: 100vh;">
      <el-header height="15vh" style="background-color: #409EFF">Header顶栏</el-header>
      <el-container style="height: 100%">
        <el-aside width="200px" style="background-color: #337ecc; height: 100%">Aside侧边栏
          <el-menu default-active="page1"
                   active-text-color="red"
                   router
          >
            <el-menu-item index="page1">选项1</el-menu-item>
            <el-menu-item index="page2">选项2</el-menu-item>
            <el-menu-item index="page3">选项3</el-menu-item>
            <el-menu-item index="page4">测试区</el-menu-item>
          </el-menu>
        </el-aside>
        <el-main style="background-color: #a0cfff">
          Main内容区
          <RouterView/>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>
<script setup>
</script>