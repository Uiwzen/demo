<template>
  <el-row class="tac">
    <el-col :span="12">
      <el-menu
        active-text-color="#ffd04b"
        background-color="#7C93C3"
        class="el-menu-vertical-demo"
        el-menu-item-group-title-color="black"
        default-active="$route.path"
        text-color="#fff"
        @open="handleOpen"
        @close="handleClose"
        router
      >
        <el-sub-menu index="1">
          <template #title>
            <el-icon><location /></el-icon>
            <span>首页</span>
          </template>
          <el-menu-item-group title="订单信息">
            <el-menu-item index="/backmain/goodsnote">订单记录</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <el-sub-menu index="2">
          <template #title>
            <el-icon><icon-menu /></el-icon>
           商品
          </template>
          <el-menu-item-group title="商品信息" >
            <el-menu-item index="/backmain/goodsranking">商品销售排行</el-menu-item>
            <el-menu-item index="/backmain/goodserchart">商品销售情况可视化</el-menu-item>
            <el-menu-item index="/backmain/goodssuggest">商品销售推荐</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <el-sub-menu index="3">
          <template #title>
            <el-icon><location /></el-icon>
            <span>我的</span>
          </template>
          <el-menu-item-group title="商户信息">
            <el-menu-item index="/backmain/mine2">商户信息</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <!-- <el-menu-item index="2">
          <el-icon><icon-menu /></el-icon>
          <span>购物车</span>
          <el-menu-item-group title="销售情况">
            <el-menu-item index="2-1">商品销售排行</el-menu-item>
            <el-menu-item index="2-2">商品销售情况可视化</el-menu-item>
            <el-menu-item index="2-2">商品销售推荐</el-menu-item>
          </el-menu-item-group>
        </el-menu-item>
        <el-menu-item index="3">
          <el-icon><icon-menu /></el-icon>
          <span>我的</span>
          <el-menu-item-group title="商户信息">
            <el-menu-item index="3-1">商户信息</el-menu-item>
          </el-menu-item-group>
        </el-menu-item> -->
      </el-menu>
    </el-col>
  </el-row>
</template>

<style scoped lang="less">
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
// 菜单高度和标题样式
.el-menu {
  height: 100vh;
  border-right: none;
  h3 {
    margin: 0;
    color: rgb(255, 255, 255);
    text-align: center;
    line-height: 48px;
    font-size: 16px;
    font-weight: 400;
  }
}

.is-active{
  color:#ffd04b;
  background-color: #295f986d;
}

a{
  text-decoration: none;
}

// .el-menu-item.is-active{
//   color:#295F98
// }

</style>

<style>
.el-menu-item-group__title{
  color:black !important;
}</style>

<script lang="ts" setup>
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue'
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}


</script>