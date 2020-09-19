<template>
   <div class='TabControl'>
     <div v-for="(item,index) in controltitles" :key="item"  @click="showAc(index)">
       <span :class="[index==temp? 'active':'']">{{item}}</span>
     </div>
   </div>
</template>

<script>
export default {
  components: {},
  props:['controltitles'],
  data() {
   return {
     temp:'0'
   };
},
methods:{
  showAc(index){
    this.temp = index;
  }
}

}
</script>
<style lang='less' scoped>
.TabControl {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px 0;
    font-size: 20px;
    height:40px;
    line-height: 40px;
    position:sticky;
    top:44px;
    & div{
      width: 30%;
      text-align:center;
      & span{
        padding:4px;
      }
    }
}
.active{
      border-bottom: 2px solid #b28aaf;
}
</style>