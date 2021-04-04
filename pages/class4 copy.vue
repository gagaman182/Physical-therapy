<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#efbbcf" class="main-header-color">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 main-header-color" medium
            >mdi-airballoon
          </v-icon>
          &nbsp; การฝึกหายใจและการฝึกไอ
        </v-card-title>
      </v-toolbar>
      <v-alert
        border="bottom"
        colored-border
        class="header-color"
        color="#efbbcf"
        elevation="2"
        ><h3>Breathing Exercise2 and Cough Training</h3>
      </v-alert>
    </v-col>
    <!-- video1 -->
    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                  Cough Training (ท่าฝึกการไอสำหรับผู้ป่วยกลืนลำบาก)
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  ระบบหายใจที่ดี สัมพันธ์กับการกลืนที่ดีเช่นเดียวกัน
                </div></v-col
              >

              <v-col cols="2">
                <v-icon size="85px" color="#ffe78f"
                  >mdi-video-high-definition
                </v-icon>
                <v-checkbox
                  v-model="seevideo1"
                  @change="noblur1"
                  label="ดูคลิปวีดีโอ"
                  color="#efbbcf"
                ></v-checkbox>
              </v-col>
            </v-row>

            <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

            <div v-blur="blurConfig1" class="text-center">
              <youtube
                video-id="Drz3xtM_MMc"
                ref="youtube"
                width="80%"
                height="700px"
                disabled
              ></youtube>

              <!-- <button @click="playVideo">play</button> -->
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-card>
    </v-col>
    <!-- video2 -->
    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                  Breathing Exercise2 การฝึกการหายใจท่าที่ 2
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  การหายใจกับการกลืนมีความสัมพันธ์กัน การฝึกหายใจเป็นจังหวะที่ดี
                  จะช่วยให้การกลืนปลอดภัยเช่นเดียวกัน
                </div></v-col
              >

              <v-col cols="2">
                <v-icon size="85px" color="#ffe78f"
                  >mdi-video-high-definition
                </v-icon>
                <v-checkbox
                  v-model="seevideo2"
                  @change="noblur2"
                  label="ดูคลิปวีดีโอ"
                  color="#efbbcf"
                ></v-checkbox>
              </v-col>
            </v-row>

            <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

            <div v-blur="blurConfig2" class="text-center">
              <youtube
                video-id="HsOzr8sIxHs"
                ref="youtube"
                width="80%"
                height="700px"
                disabled
              ></youtube>

              <!-- <button @click="playVideo">play</button> -->
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'class4',

  data() {
    return {
      blurConfig1: {
        isBlurred: true,
        opacity: 0.1,
        filter: 'blur(1.8px)',
        transition: 'all .3s linear',
      },
      blurConfig2: {
        isBlurred: true,
        opacity: 0.1,
        filter: 'blur(1.8px)',
        transition: 'all .3s linear',
      },

      seevideo1: false,
      seevideo2: false,
    }
  },
  methods: {
    noblur1() {
      this.blurConfig1.isBlurred = !this.blurConfig1.isBlurred
    },
    noblur2() {
      this.blurConfig2.isBlurred = !this.blurConfig2.isBlurred
    },
  },
  computed: {
    player() {
      return this.$refs.youtube.player
    },
  },
}
</script>

<style scoped>
.main-header-color {
  color: #ef4f4f;
}
.header-color {
  color: #be5683;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
</style>
