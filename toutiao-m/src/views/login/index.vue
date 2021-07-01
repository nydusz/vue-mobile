<template>
  <div class="login-container">
    <van-nav-bar
      class="app-nav-bar"
      title="登录/注册"
      left-arrow
      @click-left="$router.back()"
    />
    <van-cell-group>
  <van-field
    v-model="user.mobile"
    left-icon="smile-o"
    right-icon="warning-o"
    placeholder="请输入手机号"
  />
  <van-field
    v-model="user.password"
    clearable
    left-icon="music-o"
    placeholder="请输入密码"
  >
      <template #button>
      <van-button size="small" round>发送验证码</van-button>
      </template>
  </van-field>
</van-cell-group>
      <div class="login-btn-wrap">
        <van-button class="login-btn" type="info" block>登录</van-button>
      </div>
  </div>
</template>

<script>
export default {
  name: 'LoginIndex',
  components: {},
  props: {},
  data () {
    return {
      user: {
        mobile: null,
        password: null
      }
    }
  },
  computed: {},
  watch: {},
  created () {},
  mounted () {},
  methods: {}
}
</script>

<style scoped lang="less">
  .login-container {
    .login-btn-wrap {
      padding: 26px 16px;
      .login-btn {
        background-color: #6db4fb;
      }
    }
  }
</style>
