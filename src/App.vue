<template>
  <div class="common-layout">
    <el-container>
      <el-header class="border border-1">
        <div class="flex items-center h-full -mx-[20px]">
          <div class="flex items-center h-full justify-center w-[200px]">管理台</div>
        </div>
      </el-header>
      <el-container>
        <el-aside width="200px" class="border border-1 h-screen fixed top-0 left-0 pt-[58px]">
          <div class="flex justify-center py-[20px]">Aside</div>
        </el-aside>
        <el-main class="ml-[200px]">
          <el-form label-width="100px" >
            <el-form-item label="username">
              <el-input v-model="data.username"></el-input>
            </el-form-item>
            <el-form-item label="email">
              <el-input v-model="data.email"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary">submit</el-button>
            </el-form-item>
          </el-form>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script setup>
import { reactive } from "vue";
const data = reactive({
  username: '',
  email: ''
})
</script>