<template>
  <div class="container">
    <user></user>
  </div>
</template>

<script>
import card from '@/components/card'
import User from '@/components/user/index'

export default {
  data () {
    return {
      motto: 'Hello World',
      userInfo: {}
    }
  },

  components: {
    card,
    User
  },

  methods: {

  },

  created () {
    // 调用应用实例的方法获取全局数据

  }
}
</script>

<style scoped>
</style>
