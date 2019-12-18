<!-- Vue 2.6 버전 -->
<template>  
<div id="app">
  <child-from :headerText="header" :footerText="footer">
    <p>{{message}}</p>
  </child-from>
</div>
</template>
<script>
import ChildFrom from "@/components/Child.vue"
export default{
  name : "app",
  components : {
    ChildFrom
  },
  data(){
    return {
      header : "슬롯 헤드 테스트",
      footer : "슬롯 푸터 테스트",
      message : "APP 컨텐츠"
    }
  }

}
</script>
<style scoped>
p{
  text-align: center;
}
</style>