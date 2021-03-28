<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#efbbcf" class="main-header-color">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 main-header-color" medium
            >mdi-calendar-heart
          </v-icon>
          &nbsp; การบำบัดฟื้นฟู
        </v-card-title>
      </v-toolbar>
    </v-col>

    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-list-item-title class="headline mb-1">
              การบำบัดฟื้นฟู
            </v-list-item-title>
            <v-list-item-subtitle>การบำบัดฟื้นฟู</v-list-item-subtitle>

            <div v-blur="blurConfig" class="text-center">
              <youtube
                video-id="JzRMxbTf-bc"
                ref="youtube"
                width="80%"
                height="700px"
                disabled
              ></youtube>

              <!-- <button @click="playVideo">play</button> -->
            </div>
            <v-checkbox
              v-model="seevideo"
              @change="noblur"
              label="ดูคลิปวีดีโอ"
              color="#efbbcf"
            ></v-checkbox>
          </v-list-item-content>
        </v-list-item>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'class2',

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
    }
  },
  methods: {
    noblur() {
      this.blurConfig.isBlurred = !this.blurConfig.isBlurred
      this.isBlurred = !this.isBlurred
    },
    // playVideo() {
    //   this.$refs.youtube.player.playVideo()
    // },
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
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
</style>
