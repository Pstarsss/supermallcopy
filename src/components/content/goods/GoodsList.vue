<template>
   <div class='goodslist'>
     <goods-list-item v-for="i in goodslist" :key="i.clientUrl" :goodsitem="i">

     </goods-list-item>

   </div>
</template>

<script>
import GoodsListItem from './GoodsListItem.vue'
export default {
  components: {
    GoodsListItem,
  },
  props:{
    goodslist:{
      type:[Array],
      default(){
        return []
      }
    }
  },
  data() {
    return {
    };
  },
}
</script>
<style lang='less' scoped>
.goodslist {
    display: flex;
    align-items: center;
    flex-wrap:wrap;
    width:100vw;
    justify-content:space-around;
}
</style>