<!-- Vue 3.0 버전 -->
<template>  
<div id="app">
  <child-from>  <!-- # : 자식의 있는 slot의 이름  -->
    <template #slot1="s1">  <!-- #slot1="s1" - 객체  -->
      <div>
        {{s1.slotX}} + {{s1.slotY}} = {{parseInt(s1.slotX) + parseInt(s1.slotY)}}
      </div>
    </template>
    <template #slot2="s2">
      <div>
        {{s2.slotX}} 더하기 {{s2.slotY}} 는 {{parseInt(s2.slotX) + parseInt(s2.slotY)}} 입니다.
      </div>
    </template>
  </child-from>
</div>
</template>
<script>
import ChildFrom from "@/components/CalcChild.vue"
export default{
  name : "calcApp",
  components : {
    ChildFrom
  }
}
</script>
<style scoped>

</style>