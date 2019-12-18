<!-- Vue 3.0 버전 -->
<template>  
<div class="child">
  X : <input type="text" v-model="x"><br>
  Y : <input type="text" v-model="y"><br>
  <slot name="slot1" :slotX="x" :slotY="y"></slot>
  <slot name="slot2" :slotX="x" :slotY="y"></slot>
</div>
</template>
<script>
export default{
  // name 생략 시 파일 이름 앞에 소문자로 되서  default 
  data(){
    return {
      x : 0, y : 0
    }
  }
//
}
</script>
<style scoped>
.child{
  padding : 5px; border : 1px solid black
}
</style>