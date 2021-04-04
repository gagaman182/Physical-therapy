<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#efbbcf" class="main-header-color">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 main-header-color" medium
            >mdi-food
          </v-icon>
          &nbsp; อาหารฝึกกลืน
        </v-card-title>
      </v-toolbar>
      <v-alert
        border="bottom"
        colored-border
        class="header-color"
        color="#efbbcf"
        elevation="2"
        ><h3>Functional Oral Intake Score</h3>
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
  name: 'class3',
  components: {
    videos,
  },
  data() {
    return {
      items: [
        {
          classes: '1',
          videoid: '4kb2E-8OeHw',
          icon: 'mdi-video-high-definition',
          title: '   Food Modification อาหารระดับที่ 1',
          subtitle: 'No oral intake งดอาหารทางปาก',
        },
        {
          classes: '2',
          videoid: '5LQAxhq7Vsc',
          icon: 'mdi-video-high-definition',
          title: 'Food Modification อาหารระดับที่ 2',
          subtitle:
            ' Tube dependence with minimal/inconsistent oral intake รับประทานอาการทางสายยางและรับประทานอาหารทางปากได้เล็กน้อย',
        },
        {
          classes: '3',
          videoid: 'j-12oXZ6ZQE',
          icon: 'mdi-video-high-definition',
          title: ' Food Modification อาหารระดับที่ 3',
          subtitle:
            ' Tube supplement with consistence oral intake รับประทานอาการทางสายเสริมจากอาหารทางปาก',
        },
        {
          classes: '4',
          videoid: '8LcY_nalfs0',
          icon: 'mdi-video-high-definition',
          title: 'Food Modification อาหารระดับที่ 4',
          subtitle:
            'Total oral intake a single consistency รับประทานอาการทางปากด้วยอาหารอ่อนเนื้อเดียว',
        },
        {
          classes: '5',
          videoid: '_UX4ZlRxA_o',
          icon: 'mdi-video-high-definition',
          title: 'Food Modification อาหารระดับที่ 5',
          subtitle:
            'Total oral intake of multiple consistencies requiring special preparation รับประทานอาการทางปากด้วยอาหารหลายประเภทที่ต้องบด/สับก่อน',
        },
        {
          classes: '6',
          videoid: 'G0YBxl5W35Y',
          icon: 'mdi-video-high-definition',
          title: 'Food Modification อาหารระดับที่ 6',
          subtitle:
            'Total oral intake with no special preparation but must avoid specific food or liquid items รับประทานอาการทางปากปกติแต่หลีกเลี่ยงอาหารแข็งและน้ำ ',
        },
      ],
    }
  },
  methods: {},

  mounted() {},
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
