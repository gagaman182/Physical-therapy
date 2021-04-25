<template>
  <v-row>
    <v-col cols="12" class="text-center tex">
      <v-toolbar color="#ce1f6a" class="white--text">
        <v-card-title class="headline font-weight-bold white--text">
          <v-icon class="text--darken-2 white--text" medium>mdi-jabber </v-icon>
          &nbsp; ความรู้ทั่วไป
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
  name: 'class1',
  components: {
    videos,
  },
  data() {
    return {
      items: [
        {
          classes: '1',
          videoid: 'FKTDePIin1U',
          icon: 'mdi-video-high-definition',
          title: ' Dysphagia Introduction ภาวะกลืนลำบาก',
          subtitle: '',
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
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
#youtube {
  pointer-events: none;
}
</style>
