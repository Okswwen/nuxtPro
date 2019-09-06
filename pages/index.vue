<template>
  <div class="container">
    <div>
      <logo />
      <!-- 路由导航链接 -->
      <template>
        <nuxt-link to="/users">用户列表</nuxt-link>
        <el-button @click="$router.push('/users')">用户列表</el-button>
        <el-button
          @click="$router.push({ name: 'users-detail', query: { id: 1 } })"
          >用户列表id</el-button
        >
        <el-button
          @click="$router.push({ name: 'users-id', params: { id: 2 } })"
          >用户详情id</el-button
        >
      </template>
      <h1 class="title">
        nuxtPro
      </h1>
      <h2 class="subtitle">
        my first nuxt.js project!
      </h2>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
