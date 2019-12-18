<template>
<div class="container">
  <div class="header">
    {{headerText}}
  </div>
  <div class="content">
    <slot></slot>
  </div>
  <div class="footer">
    {{footerText}}
  </div>
</div>
</template>
<script>
export default{
  props : [ 'headerText', 'footerText' ]
}
</script>
<style scoped>
.container{
  width : 300px; magin : 10px; padding : 2px;
  border : 1px solid gray; float:left
}
.header{
  padding : 4px 20px; background-color : orange;
  color : aqua; text-align : center
}
.content{
  padding : 10px; height : auto; min-height: 40px;
  text-align: left
}
.footer{
  padding : 4px 20px; background-color : yellow;
  color : blue; text-align : center
}
</style>