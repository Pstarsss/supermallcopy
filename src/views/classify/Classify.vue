<template>
   <div class='wrapper' ref="sd">
       <ul class="content" >
         <button @click="btnclick()">地晚安喔</button>
         <li>我的分分1</li>
         <li>我的分分2</li>
         <li>我的分分3</li>
         <li>我的分分4</li>
         <li>我的分分5</li>
         <li>我的分分6</li>
         <li>我的分分7</li>
         <li>我的分分8</li>
         <li>我的分分9</li>
         <li>我的分分10</li>
         <li>我的分分11</li>
         <li>我的分分12</li>
         <li>我的分分13</li>
         <li>我的分分14</li>
         <li>我的分分15</li>
         <li>我的分分16</li>
         <li>我的分分17</li>
         <li>我的分分18</li>
         <li>我的分分19</li>
         <li>我的分分20</li>
         <li>我的分分21</li>
         <li>我的分分22</li>
         <li>我的分分23</li>
         <li>我的分分24</li>
         <li>我的分分25</li>
         <li>我的分分26</li>
         <li>我的分分27</li>
         <li>我的分分28</li>
         <li>我的分分29</li>
         <li>我的分分30</li>
         <li>我的分分31</li>
         <li>我的分分32</li>
         <li>我的分分33</li>
         <li>我的分分34</li>
         <li>我的分分35</li>
         <li>我的分分36</li>
         <li>我的分分37</li>
         <li>我的分分38</li>
         <li>我的分分39</li>
         <li>我的分分40</li>
         <li>我的分分41</li>
         <li>我的分分42</li>
         <li>我的分分43</li>
         <li>我的分分44</li>
         <li>我的分分45</li>
         <li>我的分分46</li>
         <li>我的分分47</li>
         <li>我的分分48</li>
         <li>我的分分49</li>
         <li>我的分分50</li>
         <li>我的分分51</li>
         <li>我的分分52</li>
         <li>我的分分53</li>
         <li>我的分分54</li>
         <li>我的分分55</li>
         <li>我的分分56</li>
         <li>我的分分57</li>
         <li>我的分分58</li>
         <li>我的分分59</li>
         <li>我的分分60</li>
         <li>我的分分61</li>
         <li>我的分分62</li>
         <li>我的分分63</li>
         <li>我的分分64</li>
         <li>我的分分65</li>
         <li>我的分分66</li>
         <li>我的分分67</li>
         <li>我的分分68</li>
         <li>我的分分69</li>
         <li>我的分分70</li>
         <li>我的分分71</li>
         <li>我的分分72</li>
         <li>我的分分73</li>
         <li>我的分分74</li>
         <li>我的分分75</li>
         <li>我的分分76</li>
         <li>我的分分77</li>
         <li>我的分分78</li>
         <li>我的分分79</li>
         <li>我的分分80</li>
         <li>我的分分81</li>
         <li>我的分分82</li>
         <li>我的分分83</li>
         <li>我的分分84</li>
         <li>我的分分85</li>
         <li>我的分分86</li>
         <li>我的分分87</li>
         <li>我的分分88</li>
         <li>我的分分89</li>
         <li>我的分分90</li>
         <li>我的分分91</li>
         <li>我的分分92</li>
         <li>我的分分93</li>
         <li>我的分分94</li>
         <li>我的分分95</li>
         <li>我的分分96</li>
         <li>我的分分97</li>
         <li>我的分分98</li>
         <li>我的分分99</li>
         <li>我的分分100</li>     
       </ul>
    
     

   </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  components: {},
  data() {
    return {
      besc:''
    };
  },
  methods:{
    btnclick(){
      console.log("wowo");
    }
  },     
  mounted(){
    this.besc = new BScroll(this.$refs.sd,{
      movable: true,
      zoom: true,
      probeType:2,
      pullUpLoad:true,

    });
    this.besc.on('scroll',(position)=>{
      // console.log(position);
    });
    this.besc.on('pullingUp',()=>{
      console.log("312312");
      setTimeout(()=>{
        this.besc.fin
      },750);
    })
  }
}
</script>
<style lang='less' scoped>
.wrapper{
  height:200px;
  border:1px solid red;
  overflow: hidden;
}
</style>