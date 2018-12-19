<template>
  <div class="part-top">
    <div><img src="../../../../static/images/top_bg_01.png" alt=""></div>
   <div class="bottomline">
     <div class="bottomline1"><div class="d1"></div> <div class="img1"></div><div class="d2"></div> </div>
    <div class="bottomline1"><div class="d1"></div><div class="img2"></div><div class="d2"></div> </div>
    <div class="bottomline3"><div class="d1"></div><div class="img3"></div><div class="d3"></div> </div>

   </div>
  </div>
</template>

<script>
import wheather from '../components/wheather.vue'
export default {
  components:{ wheather },
  props: {},
  data(){
    return {}
  },
  created() {},
  mounted() {},
  computed:{},
  methods: {},
  watch: {},
};
</script>
<style lang="less" >
.part-top{
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;

    height:80px;
    background-color: #06161f;

}
.bottomline{
   display: flex;
  flex-direction: row;
    justify-content: space-between;
  flex-wrap: nowrap;
  height:3px;
  width: 100%;

}
.bottomline1{
  display: flex;
  flex-direction: row;
    justify-content: space-between;
  flex-wrap: nowrap;
}
.bottomline2{
  display: flex;
  flex-direction: row;
    justify-content: space-between;
  flex-wrap: nowrap;
}
.bottomline3{
  display: flex;
  flex-direction: row;
    justify-content: space-between;
  flex-wrap: nowrap;
}
.d1{
 width: 2px;
  height: 2px;
  background-color: #60b8c6;
   margin-left: 21px;
}
.d2{
 width: 2px;
  height: 2px;
  background-color: #60b8c6;

}
.img1{
  width: 408px;
  height: 1px;
  background-color: #214751;

    margin-bottom: 5px
}
.img2{
  width: 1000px;
  height: 1px;
  background-color: #214751;
/*   margin-left: -355px; */
}
.img3{
 width: 408px;
  height: 1px;
  background-color: #214751;

}
.d3{
 width: 2px;
  height: 2px;
  background-color: #60b8c6;
margin-right: 15px;
}
</style>
