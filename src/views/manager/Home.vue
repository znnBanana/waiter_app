<template>
  <div class="home">
    <!-- 顶部导航栏 -->
    <div class="title">
      <van-row>
        <van-col span="4">
          <van-icon size="30" @click="CloseHome" style="padding:16px" name="cross" color="#333333"/>
        </van-col>
        <van-col :offset="2" span="18" style="font-size:20px;color:#333333;padding:16px;text-align:left">e洁家政服务平台</van-col>
      </van-row>
    </div>
    <!-- /顶部导航栏 -->
    {{earn}}
    
    {{IncomeTotal}}
  </div>
</template>

<script>
import {mapActions,mapGetters,mapState} from 'vuex'
export default {
  data() {
    return {

    }
  },
  created() {
    this.EarningWaiter(this.info.id)
  },
  computed: {
    ...mapState('user',['info','earn']),
    ...mapGetters('user',['IncomeTotal'])
  },
  methods: {
    ...mapActions('user',['EarningWaiter']),
    // 返回到登录页面
    CloseHome(){
      this.$router.push({path:'/login'})
    }
  }
}
</script>

<style scoped>
.home {
  padding-bottom: 50px;
}
.header {
  height: 300px;
  overflow: hidden;
}
.header img {
  width: 100%;
}
</style>