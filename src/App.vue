<template>
  <el-container>
    <el-header>
      <nav-header></nav-header>
    </el-header>
    <el-container>
      <el-aside>
        <nav-aside></nav-aside>
      </el-aside>
      <el-container>
        <el-main>
            <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </el-container>
</template>
<script>
  import NavAside from './components/NavAside'
  import NavHeader from "./components/NavHeader";
  export default {
    name:'app',
    components:{
      'nav-aside':NavAside,
      'nav-header':NavHeader,
    }
  }
</script>
