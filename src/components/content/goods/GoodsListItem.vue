<template>
   <div class='goodslistitem' >
     <div class="showimg">
       <img :src="goodsitem.show.img" alt="">
     </div>
     <div class="showinfo">
       <h4>{{goodsitem.title}}</h4>
       <span class="price">{{goodsitem.price}}</span>
       <span class="iconfont-ali">&#xe509;</span>
       <span>{{goodsitem.cfav}}</span>
     </div>
   </div>
</template>

<script>
export default {
  components: {

  },
  props:{
    goodsitem:{
      type:[Object],
      default(){
        return {}
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
.goodslistitem{
  width:48vw;
  padding:1vw;
  text-align:center;
  &  img{
    width: 100%;
    border-radius:10px;
  }
  & h4{
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    padding:1vw 0;
  }
  & .price{
    color:var(--color-high-text);
  }
  & span{
    padding:0.8vw;
  }
  & .showinfo{
    width:96%;
    margin:0 auto;
  }
}
</style>