<template>
  <div class="container">
    <div class="nav">
      <ul class="nav-list">
        <li class="nav-item">
          <router-link to="/components/switch">switch 按钮切换</router-link>
        </li>
      </ul>
    </div>
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
.container {
  display: flex;
  .nav {
    width: 200px;
  }
}
</style>
