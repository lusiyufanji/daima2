<template>
  <div>
    <div class="mianMianBan">
      <div class="top-ban clearfix">
        <div class="sm-touxiang fl"></div>
        <div class="found">
          <i class="fa fa-search"></i>
        </div>
        <div class="test-box clearfix">
          <router-link to="/Message">
            <div class="test-tab fl" @click="message = 1,friends = 2,onLineWord =2" :class="{ 'test-tab':message === 2,'active':message === 1 }">
              <i class="test fa fa-wechat op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
          <router-link to="/Friends">
            <div class="test-tab fl" @click="message = 2,friends = 1,onLineWord =2" :class="{ 'test-tab':friends === 2,'active':friends === 1 }">
              <i class="test fa fa-address-card-o op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
          <router-link to="/onLineWord">
            <div class="test-tab fl" @click="message = 2,friends = 2,onLineWord =1" :class="{ 'test-tab':onLineWord === 2,'active':onLineWord === 1 }" >
              <i class="test fa fa-file-o op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
        </div>
        <div class="gongneng fl">
          <i class="fa fa-navicon"></i>
          <i class="fa fa-minus"></i>
          <i class="fa fa-square-o"></i>
          <i class="fa fa-times hover-red"></i>
        </div>
      </div>
    <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Firends from './Friends.vue'
import Message from './Message.vue'
import onLineWord from './onLineWord.vue'
  export default {
  data(){
    return{
      message:1,
      friends:2,
      onLineWord:2
    }
  },
    components:{
      Firends,
      Message,
      onLineWord,
    }
  }
</script>

<style scoped>
  .mianMianBan{
    margin-top: 5%;
    margin-left: auto;
    margin-right: auto;
    width: 800px;
  }
  .top-ban{
    height: 55px;
    background-image: url("../assets/banenr-logo.png");
    border-top-right-radius: 7px;
    border-top-left-radius: 7px;
    width: 800px;
    overflow: hidden;
    box-shadow: 0 -3px 9px #898989;
  }
  .sm-touxiang{
    width: 40px;
    height: 40px;
    border-radius: 40px;
    background-image: url("../assets/touxiang.jpg");
    background-size: cover;
    position: relative;
    border: 1px solid #2E9BE9;
    top: 7px;
    left: 7px;
  }
  .sm-touxiang:hover{
    border: 1px solid #D4EBFB ;
  }
  .found{
    width: 95px;
    height: 22px;
    border-radius: 22px;
    border: 1px solid #FFFFFF;
    color: #FFFFFF;
    opacity: 0.4;
    position: relative;
    left: 80px;
    top: 15px;
  }
  .found i{
    position: relative;
    left: -32px;
  }
  .found:hover{
    color: #FFFFFF;
    opacity: 1.0;
  }
  .test-box{
    margin-left: 195px;
    margin-top: -10px;
  }
  .test-tab{
    margin-right: 35px;
  }
  .test-tab .sanjiao{
    position: relative;
    color: #FFFFFF;
    top:0;
    left: 5px;
    opacity: 0;
  }
  .test-tab i{
    color: #FFFFFF;
    font-size: 25px;
    opacity: 0.7;
  }
  .test-box .active .op,.test-box .active .op{opacity: 1.0}
  .test-box .test:hover{opacity: 1.0}


  .gongneng{
    position: relative;
    left: 660px;
    top: -8px;
  }
  .gongneng i{
    color: #FFFFFF;
    opacity: 0.6;
    margin-right: 5px;
  }
  .gongneng i:hover{
    opacity: 1.0;
  }
  .hover-red{
    padding: 3px;
  }
  .hover-red:hover{
    background-color: red;
    padding: 3px;
  }
</style>
