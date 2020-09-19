<template>
   <div class='nav-bar'>
     <div class='left'><slot name="navleft"></slot></div>
     <div class='center'><slot name="navcenter"></slot></div>
     <div class='right'><slot name="navright"></slot></div>
   </div>
</template>

<script>
export default {
  components: {},
  data() {
   return {
    };
  },
}
</script>
<style lang='less' scoped>
.nav-bar{
  text-align:center;
  display:flex;
  align-items: center;
  height:40px;
  position: fixed;
  top: 0;
  left:0;
  right:0;
  height:44px;
  justify-content: space-between;
}
.nav-bar .center{
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 100%;
  flex-grow:1;
}
.left,.right{
  width:60px;
  height:100%;
}
</style>