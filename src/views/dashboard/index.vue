<template>
  <div class="dashboard-container">
    <div class="dashboard-text">
      欢迎您，尊敬的<span v-for='permission in permissions' :key='permission'>{{permission}}</span> {{name}}！
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'dashboard',
  computed: {
    ...mapGetters([
      'avatar',
      'name',
      'permissions'
    ])
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
    text-align: center;
  }
}
</style>
