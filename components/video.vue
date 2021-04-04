<template>
 <v-col cols="12">
 <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                 {{title}}
                </v-list-item-title>
                <!-- <div class="my-4 subtitle-1"  >
                   {{subtitle}}
                  </div> -->
                  
                  <div v-html="subtitle" class="my-4 subtitle-1" ></div></v-col
              ></br>
              

              <v-col cols="2">
                <v-icon size="85px" color="#ffe78f"
                  >{{icon}}
                </v-icon>
                <v-checkbox
                  v-model="seevideo"
                  @change="noblur"
                  label="ดูคลิปวีดีโอ"
                  color="#efbbcf"
                ></v-checkbox>
              </v-col>
            </v-row>
            <div class="title text-center text " v-bind:style="{ backgroundColor: statecolor}">สถานะการเล่นวิดีโอ: {{state}}</div>
            <div v-blur="blurConfig" class="text-center">
              
              <youtube
                id="youtube"
                :video-id="videoid"
                ref="youtube"
                width="80%"
                height="700px"
                @playing="playing"
                @paused="paused"
                @ended="ended"
              ></youtube>
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-card>
  </v-col>
  
</template>
<script>
export default {
  name: 'video',
   props: {
    videoid: {
      type: String,
      default: null,
    },
    title: {
      type: String,
      default: null,
    },
     subtitle: {
      type: String,
      default: null,
    },
  
    icon:{
      type:String,
      defalut:null
    },
    classes:{
      type:String,
      defalut:null
    }
  },

  data() {
    return {
      isBlurred: true,

      blurConfig: {
        isBlurred: true,
        opacity: 0.1,
        filter: 'blur(1.8px)',
        transition: 'all .3s linear',
      },
      seevideo: false,
      state:"ยังไม่เล่น",
      statecolor:'#fa1e0e'
    
    }
  },
  methods: {
    noblur() {
      alert(this.classes)
      this.blurConfig.isBlurred = !this.blurConfig.isBlurred
      this.isBlurred = !this.isBlurred

      if (this.blurConfig.isBlurred) {
        this.pauseVideos()
        this.statecolor = '#e97878'
        
      } else if (!this.blurConfig.isBlurred) {
        this.playVideos()
        this.statecolor = '#94ebcd'
      }
    },
    //ปุ่มให้เล่น
    playVideos() {
      this.$refs.youtube.player.playVideo()
       this.statecolor = '#94ebcd'
    },
    //ปุ่มให้หยุด
    pauseVideos() {
      this.$refs.youtube.player.pauseVideo()
      
    },
    //สถานะเล่น
    playing() {
      this.state = 'กำลังเล่น'
      this.statecolor = '#94ebcd'
      //alert('กำลังเล่น')
    },
    //สถานะหยุด
    paused() {
       this.state = 'หยุดเล่น'
      //alert('หยุดเล่น')
       this.statecolor = '#e97878'
    },
    //สถานะจบ
    ended() {
      this.state = 'จบการเล่น'
      //alert('จบการเล่น')
       this.statecolor = '#e97878'
    },
  },

  mounted() {
    if (this.blurConfig.isBlurred) {
      this.pauseVideos()
      this.statecolor = '#e97878'
      
    } else if (!this.blurConfig.isBlurred) {
      this.playVideos()
        this.statecolor = '#94ebcd'
    }
  },
}
</script>

<style scoped>
.main-header-color {
  color: #e97878;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
#youtube {
  pointer-events: none;
}


</style>
