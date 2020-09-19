<template>
   <div class='HomePage'>
     <nav-bar class="custom"><div slot="navcenter">商业街</div></nav-bar>
     <swiper :banners="banners"></swiper>
     <recommand :recs='recommands'></recommand>
     <feature-view/>
     <tab-control :controltitles="controlTitles"></tab-control>

     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>
   </div>
</template>

<script>

import Swiper from './childCompons/HomeSwiper.vue'
import Recommand from './childCompons/HomeRecommand.vue'
import FeatureView from './childCompons/HomeFeatureView.vue'

import NavBar from '@/components/common/navbar/NavBar.vue'
import TabControl from '@/components/common/tabcontrol/TabControl.vue'

import {getHomeMultidata} from  '@/network/home.js'

export default {
  components: {
   
    Swiper,
    Recommand,
    FeatureView,

    TabControl,
    NavBar,

  },
  data() {
   return {
     banners:[],
     recommands:[],
     controlTitles:['流行','新款','精选'],
    
   };
},
created(){
  getHomeMultidata().then((res)=>{
    this.banners = res.data.banner.list;
    this.recommands = res.data.recommend.list;
  })
}
}
</script>
<style lang='less' scoped>
.custom{
  background-color:var(--color-tint);
  color:#fff;
}
</style>