<template>
  <div>
    <span class="msg">hello world</span>
    <van-button type="primary" @click="jump">按钮</van-button>
  </div>
</template>

<script>
import { post } from "@/utils/request"
export default {
  methods:{
    jump(){
      post("https://www.baidu.com").then(response=>{
        console.log("handleResponse...")
      })
    }
  }
};
</script>

<style lang="scss" scoped>
.msg {
  color: red;
  font-size: 20px;
  font-weight: bold;
}
</style>
