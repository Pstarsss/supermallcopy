<template>
   <div class='HomePage'>
     <nav-bar class="custom"><div slot="navcenter">商业街</div></nav-bar>
     <swiper :banners="banners"></swiper>
     <recommand :recs='recommands'></recommand>
     <feature-view/>
     <tab-control :controltitles="controlTitles2" @tabclick="jumptab"></tab-control>
     <goods :goodslist="showtab"></goods>
     <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
     <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
   </div>
</template>

<script>

import Swiper from './childCompons/HomeSwiper.vue'
import Recommand from './childCompons/HomeRecommand.vue'
import FeatureView from './childCompons/HomeFeatureView.vue'


import NavBar from '@/components/common/navbar/NavBar.vue'
import TabControl from '@/components/content/tabcontrol/TabControl.vue'
import Goods from '@/components/content/goods/GoodsList.vue'

import {getHomeMultidata,getHomeGoods} from  '@/network/home.js'

export default {
  components: {
   
    Swiper,
    Recommand,
    FeatureView,

    TabControl,
    NavBar,
    Goods,
  },
  data() {
   return {
      banners:[],
      recommands:[],
      controlTitles1:['pop','new','sell'],
      controlTitles2:['流行','新款','热卖'],
      Currenttype:'pop',
      goods:{
        'pop':{page:0,list:[]},
        'new':{page:0,list:[]},
        'sell':{page:0,list:[]}
      }
    };
  },
  computed:{
    showtab(){
      return this.goods[this.Currenttype].list;
    }
  },
  created(){
    this.getHomeMultidata1();
    this.getHomeGoods1('pop');
    this.getHomeGoods1('new');
    this.getHomeGoods1('sell');

  },
  methods:{
    //请求首页的上半部分数据
    getHomeMultidata1(){
      getHomeMultidata().then((res)=>{
        this.banners = res.data.banner.list;
        this.recommands = res.data.recommend.list;
      });
    },
    //请求首页的下半部分的数据
    getHomeGoods1(type){
      const page = this.goods[type].page + 1;
      getHomeGoods(type,page).then((res)=>{
          this.goods[type].list = [...this.goods[type].list,...res.data.list];
          this.goods[type].page++;
          console.log(this.goods[type].list);
      })
    },
    jumptab(val){
      this.Currenttype = this.controlTitles1[val];
    }
  }
}
</script>
<style lang='less' scoped>
.custom{
  background-color:var(--color-tint);
  color:#fff;
}
</style>