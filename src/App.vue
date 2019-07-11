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
          <!--<el-scrollbar wrap-style="max-height: 200px;" view-style="font-weight: bold;" view-class="view-box" :native="false">-->
            <router-view></router-view>
          <!--</el-scrollbar>-->
        </el-main>
        <el-footer height="20">
          <el-divider></el-divider>
          <el-row type="flex" class="row-bg" justify="center">
          <el-col :span="12">
              <div>
                <span><el-link :underline="false" type="primary" href="#">Copyright &copy; 2019 T0UGH </el-link></span>
                      <el-divider direction="vertical"></el-divider>
                <span><el-link :underline="false" type="primary" href="#">Powered by HOSO</el-link></span>
              </div>
            </el-col>
          </el-row>
        </el-footer>
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
