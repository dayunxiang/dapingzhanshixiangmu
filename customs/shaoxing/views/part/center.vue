    <template>
          <div class="part-center">
              <!-- <my-map></my-map> -->
            <!-- 扫描 -->
            <div style="  width:100%; height:100%;position: absolute; margin:0 auto; background:url(../static/images/saomiao/wangge03.png);background-repeat:repeat; 
               z-index:2; overflow:hidden;" >
               <div class="beijing01" style="  width:1036px; height:278px; margin:0 auto; background:url(../static/images/saomiao/扫描01.png);background-repeat:repeat-x; 
               z-index:3;"></div>
            </div>
            <!-- 扫描 -->
            <!-- 闪烁图标 -->
            <div style="position:absolute; top:570px; left:796px;z-index:10; ">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:400px; left:600px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_02.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:460px; left:1074px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_03.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:450px; left:620px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_02_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:360px; left:998px;z-index:10; ">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:684px; left:740px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_02.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:661px; left:904px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_03.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:600px; left:1140px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_02_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:400px; left:1154px;z-index:10; ">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:610px; left:968px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_02.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:280px; left:1280px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_01_03.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <div style="position:absolute; top:415px; left:920px;z-index:10;">
              <embed height="30px" width="30px" src="../static/images/saomiao/yali_02_01.swf" type="application/x-shockwave-flash" wmode="transparent"  >
            </div>
            <!-- 闪烁图标 -->
            <div style="height:100%;position:relative;">
              <div class="map-switch" v-if="theme == 'check'||theme == 'applypump'" :style="{top:theme=='applypump'?'-4px':'171px'}">
                <span class="map-click" id="map_1" :class="{'active':selectId==1}">
                  <a @click="switchMap(1)">管网压力变化</a>
                </span>
                <span class="map-click" id="map_2" :class="{'active':selectId==2}">
                  <a @click="switchMap(2)">管网流量分布</a>
                </span>
                <span class="map-click" id="map_3" :class="{'active':selectId==3}">
                  <a @click="switchMap(3)">管网事件分布</a>
                </span>
              </div>
            
                <!-- <iframe src="http://121.40.242.176:8091/#/pressuremap" width="100%" height="100%;" style="border-width: 0px!important;" id="m_map"></iframe> -->
            </div>
            <div class="map-warp">
              <iframe name="m_map2"  :style="{zIndex:selectId==1?10:1}" src="../../../../static/images/map1.jpg" width="100%" height="100%;" style="border-width: 0px!important;position:absolute;z-index:20;" id="m_map2"></iframe>
              <!-- <iframe name="m_map2"  :style="{zIndex:selectId==1?10:1}" src="http://121.40.242.176:8091/#/pressuremap" width="100%" height="100%;" style="border-width: 0px!important;position:absolute;z-index:20;" id="m_map2"></iframe> -->
              <!-- <iframe name="m_map1" :style="{zIndex:selectId==2?10:1}" src="http://121.40.242.176:8091/#/flowmap" width="100%" height="100%;" style="border-width: 0px!important;position:absolute;z-index:10;" id="m_map1"></iframe>
                
              <iframe name="m_map3" :style="{zIndex:selectId==3?10:1}" src="http://121.40.242.176:8091/#/eventmap" width="100%" height="100%;" style="border-width: 0px!important;position:absolute;z-index:30;" id="m_map3"></iframe> -->
            </div>
          </div>
           
    </template>

    <script>
    import partRight from './right.vue'
    import partTop from './top.vue'
    // import MyMap from '../components/myMap.vue'

    export default {
      props: {
        theme: String
      },
      data(){
        return {
          selectId:1
        }
      },
      created() {
        },
      computed:{},
      methods: {
        switchMap(key){
          this.selectId = key
        }
      },
      watch: {},
      components:{
          partRight,
          partTop,
        //   MyMap
      }
    };
    </script>
    <style lang="less" >
    #map_1{
      display: inline-block;
       width: 100px;
              height:30px;
              text-align: center;
              line-height: 30px;
             /*  border-radius: 2px;
              border: 1px solid #1d81b3;
              margin-bottom: 10px; */
    }
    .part-center{
        float: left;
        width: 54%;
        height: 100%;
        box-sizing: border-box;
        // position: relative;
        .map-switch{
          z-index: 2000;
          width: 100%;
          height: 40px;
          box-sizing: border-box;
          position: absolute;
    	    background-color: #06161f;
         /*  border: solid 2px rgba(89, 90, 90, 0.8); */
          font-family: MicrosoftYaHei-Bold;
          font-size: 12px;
        /*   font-weight: 600; */
          line-height: 29px;
          color: #747474;
          .map-click{
            margin-left: 9px;
            margin-right: 30px;
            a{
              cursor: pointer;
            }
            &.active{
            /*   display: inline-block; */
              color: #d2d6d9;
              background-color: rgba(13,54,75,0.8);
              display: inline-block;
               width: 100px;
              height:30px;
              text-align: center;
              line-height: 30px;
              border-radius: 2px;
              border: 1px solid #1d81b3;
              margin-bottom: 10px;
            }
          }
          
        }
        .map-warp{
          position: absolute;
          width: 100%;
          height: 100%;
          background-color: transparent;
          top: 0;
          left: 0;
          z-index: 0;
          iframe{
            background-color: transparent;
          }
        }
    }

.beijing01
{  
  position:absolute; 
	animation:mymove 10s infinite;
	-webkit-animation:mymove 10s infinite; /* Safari and Chrome */
}

@keyframes mymove
{
	0% { top:-60px;}
	100%{ top:700px;}
}

@-webkit-keyframes mymove /* Safari and Chrome */
{
	0% { top:-60px;}
	100% { top:700px;}
}

    </style>
