<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#efbbcf" class="main-header-color">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 main-header-color" medium
            >mdi-jabber
          </v-icon>
          &nbsp; ความรู้ทั่วไป
        </v-card-title>
      </v-toolbar>
    </v-col>

    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                  Dysphagia Introduction ภาวะกลืนลำบาก
                </v-list-item-title></v-col
              ></br>

              <v-col cols="2">
                <v-icon size="85px" color="#ffe78f"
                  >mdi-video-high-definition
                </v-icon>
                <v-checkbox
                  v-model="seevideo"
                  @change="noblur"
                  label="ดูคลิปวีดีโอ"
                  color="#efbbcf"
                ></v-checkbox>
              </v-col>
            </v-row>

            <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

            <div v-blur="blurConfig" class="text-center">
              <youtube
                id="youtube"
                video-id="FKTDePIin1U"
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
  </v-row>
</template>
<script>
export default {
  name: 'class1',

  data() {
    return {
      isBlurred: true,

      blurConfig: {
        isBlurred: false,
        opacity: 0.1,
        filter: 'blur(1.8px)',
        transition: 'all .3s linear',
      },
      seevideo: true,
      state: null,
    }
  },
  methods: {
    noblur() {
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
