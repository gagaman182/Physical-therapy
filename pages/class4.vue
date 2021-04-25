<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#ce1f6a" class="white--text">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 white--text" medium
            >mdi-airballoon
          </v-icon>
          &nbsp; การฝึกหายใจและการฝึกไอ (6)
        </v-card-title>
      </v-toolbar>
      <v-alert
        border="bottom"
        colored-border
        class="header-color text-center display-1"
        color="#ce1f6a"
        elevation="2"
        ><h3>Breathing Exercise2 and Cough Training</h3>
      </v-alert>
    </v-col>

    <v-col cols="12">
      <div class="columns is-mobile" v-for="item in items" :key="item.videoid1">
        <videos
          :videoid="item.videoid"
          :title="item.title"
          :content="item.content"
          :icon="item.icon"
          :classes="item.classes"
        ></videos>
      </div>
    </v-col>
  </v-row>
</template>
<script>
import videos from '@/components/video'
export default {
  name: 'class1',
  components: {
    videos,
  },
  data() {
    return {
      items: [
        {
          classes: '1',
          videoid: 'Drz3xtM_MMc',
          icon: 'mdi-video-high-definition',
          title: ' Cough Training (ท่าฝึกการไอสำหรับผู้ป่วยกลืนลำบาก)',
          subtitle: 'ระบบหายใจที่ดี สัมพันธ์กับการกลืนที่ดีเช่นเดียวกัน',
        },
        {
          classes: '2',
          videoid: 'HsOzr8sIxHs',
          icon: 'mdi-video-high-definition',
          title: ' Breathing Exercise2 การฝึกการหายใจท่าที่ 2',
          subtitle:
            '    การหายใจกับการกลืนมีความสัมพันธ์กัน การฝึกหายใจเป็นจังหวะที่ดีจะช่วยให้การกลืนปลอดภัยเช่นเดียวกัน',
        },
      ],
    }
  },
  methods: {},

  mounted() {},
}
</script>

<style scoped>
/* .main-header-color {
  color: #ef4f4f;
} */
.header-color {
  color: #ce1f6a;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
#youtube {
  pointer-events: none;
}
</style>
