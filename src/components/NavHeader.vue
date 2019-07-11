<template>
    <el-row type="flex" class="row-bg" justify="space-between">
        <el-col :span="16" class="el-tabs__nav-wrap">
            <el-image
                    style="width: 180px; height: 60px;"
                    src="logo.svg"
                    fit="fill">
            </el-image>
        </el-col>
        <el-col :span="8" class="el-tabs__nav-wrap">
            <el-row type="flex" class="row-bg" justify="end">
                <el-col :span="20">
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :router="true" @select="handleSelect">
                        <el-menu-item index="home"><b>首页</b></el-menu-item>
                        <el-menu-item index="product"><b>产品</b></el-menu-item>
                        <el-menu-item index="contact"><b>联系</b></el-menu-item>
                        <el-menu-item>
                            <el-dropdown>
                                <el-avatar shape="square" :size="40" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png">
                                </el-avatar>
                                <el-dropdown-menu slot="dropdown">
                                    <el-dropdown-item>登出</el-dropdown-item>
                                    <el-dropdown-item>切换</el-dropdown-item>
                                    <el-dropdown-item>设置</el-dropdown-item>
                                </el-dropdown-menu>
                            </el-dropdown>
                        </el-menu-item>
                    </el-menu>
                </el-col>
            </el-row>
        </el-col>
    </el-row>
</template>
<script>
    export default {
        data() {
            return {
                activeIndex: '1',
                activeIndex2: '1'
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }
</script>