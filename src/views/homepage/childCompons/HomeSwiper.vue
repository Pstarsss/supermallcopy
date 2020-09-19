<template>
   <div class='Swiper'>
     <swiper-box>
       <swiper-item class="s1"></swiper-item>
       
     </swiper-box>
     <!-- <div v-for="i in list" :key="i.link">
       {{i.image}}
       {{i.title}}
     </div> -->
   </div>
</template>

<script>
import {SwiperBox, SwiperItem} from '@/components/common/swiper/index.js'
export default {
  components: {
    SwiperBox,
    SwiperItem
  },
  props:{
    banners:{
      type:[Array],
      default(){
        return []
      }
    }
  },
  data() {
   return {
     list:this.banners
   };
  },
  created(){
    
  }

}
</script>
<style lang='less' scoped>
.Swiper{
  padding-top:44px;
}
.s1{
  background-color: red;
  width: 100%;
  height: 300px;
}
.s2{
  background-color: blue;
}
.s3{
  background-color: orange;
}
.s4{
  background-color: gray;
}
</style>