<template>

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
      state: null,
    }
  },
  methods: {
    noblur() {
      alert(this.classes)
      this.blurConfig.isBlurred = !this.blurConfig.isBlurred
      this.isBlurred = !this.isBlurred

      if (this.blurConfig.isBlurred) {
        this.pauseVideos()
      } else if (!this.blurConfig.isBlurred) {
        this.playVideos()
      }
    },
    //ปุ่มให้เล่น
    playVideos() {
      this.$refs.youtube.player.playVideo()
    },
    //ปุ่มให้หยุด
    pauseVideos() {
      this.$refs.youtube.player.pauseVideo()
    },
    //สถานะเล่น
    playing() {
      alert('กำลังเล่น')
    },
    //สถานะหยุด
    paused() {
      alert('หยุดเล่น')
    },
    //สถานะจบ
    ended() {
      alert('จบการเล่น')
    },
  },

  mounted() {
    if (this.blurConfig.isBlurred) {
      this.pauseVideos()
    } else if (!this.blurConfig.isBlurred) {
      this.playVideos()
    }
  },
}
</script>

<style scoped>
.main-header-color {
  color: #ef4f4f;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
#youtube {
  pointer-events: none;
}
</style>
