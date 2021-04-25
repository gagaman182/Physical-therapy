<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#ce1f6a" class="white--text">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 white--text" medium
            >mdi-toothbrush-paste
          </v-icon>
          &nbsp; การทำความสะอาดช่องปาก (5)
        </v-card-title>
      </v-toolbar>
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
  name: 'class5',
  components: {
    videos,
  },
  data() {
    return {
      items: [
        {
          classes: '1',
          videoid: 'RjorFPINfCc',
          icon: 'mdi-video-high-definition',
          title: ' Oral Hygiene การทำความสะอาดช่องปากผู้ป่วยโรคหลอดเลือดสมอง',
          subtitle:
            'ความสะอาดในช่องปากเป็นสิ่งสำคัญลำดับต้น ๆ สำหรับผู้ป่วยโรคหลอดเลือดสมอง ในระยะแรก ๆ โดยเฉพาะผู้ป่วยที่ยังไม่สามารถรับประทานทางปาก หรือมีภาวะกลืนลำบากได้ <br/> <p class="font-weight-black">วัตถุประสงค์ของการทำความสะอาดในช่องปาก</p><br/>- ป้องกันภาวะแทรกซ้อน ภาวะติดเชื้อในปอดจากการสำลักแบคทีเรียในช่องปาก<br /> - สร้างสุขลักษณะที่ดี<br/>- ส่งเสริมคุณภาพชีวิตที่ดี<br/>- เพิ่มโอกาสการฟื้นฟูภาวะกลืนลำบาก',
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
