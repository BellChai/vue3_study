<template>
  <el-config-provider :locale="locale">
    <nav>
      <!-- 头部 -->
      <Header></Header>
      <div style="display: flex;">
        <!-- 侧边栏 -->
        <Aside></Aside>
        <!-- 主体 -->
        <router-view style="flex: 1;" />
      </div>
    </nav>
  </el-config-provider>

</template>

<style>
nav {
  padding: 0px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import Header from "@/components/Header"
import Aside from "./components/Aside.vue"
import { defineComponent } from 'vue'
import { ElConfigProvider } from 'element-plus'

import zhCn from 'element-plus/lib/locale/lang/zh-cn'


export default defineComponent({
  name: "Layout",
  components: {
    Header,
    Aside,
    ElConfigProvider,
  },
  setup() {
    return {
      locale: zhCn,
    }
  }
})
</script>
