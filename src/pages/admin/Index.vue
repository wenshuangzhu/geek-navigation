<template>
  <el-container class="base-layout">
    <el-aside width="200px">
      <div class="title">
        <img class="icon-logo" src="/favicon.ico" />
        <span>猿梦极客导航后台</span>
      </div>
      <el-row>
        <el-col :span="24">
          <el-menu
            router
            class="el-menu-vertical-demo"
            background-color="#30333c"
            text-color="#6b7386"
            active-text-color="#fff"
            :default-active="$route.path"
          >
            <el-menu-item index="/admin">
              <span slot="title">用户提交</span>
            </el-menu-item>
            <el-menu-item index="/admin/list">
              <span slot="title">所有网站</span>
            </el-menu-item>
            <el-menu-item index="/admin/category">
              <span slot="title">分类管理</span>
            </el-menu-item>
          </el-menu>
        </el-col>
      </el-row>
    </el-aside>
    <el-container>
      <el-header><router-link class="el-icon-s-home"  to='/' style='font-size: 20px' /></el-header>
      <el-main><router-view></router-view></el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</template>

<script>
export default {
}
</script>

<style lang="scss">
.el-header,
.el-footer {
  background-color: #fff;
  color: #333;
  text-align: center;
  line-height: 60px;
}
.el-header {
  text-align: right;
}

.el-aside {
  background-color: #30333c;
  color: #6b7386;
  text-align: center;
  height: 100vh;
  overflow-y: scroll;

  .title {
    font-size: 16px;
    padding: 20px 0;
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
