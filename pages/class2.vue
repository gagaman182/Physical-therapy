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
      <v-alert
        border="bottom"
        colored-border
        class="header-color"
        color="#efbbcf"
        elevation="2"
        ><h3>การบำบัดฟื้นฟูการกลืน</h3>
      </v-alert>
    </v-col>
    <v-col cols="12">
      <div class="columns is-mobile" v-for="item in items" :key="item.videoid1">
        <videos
          :videoid="item.videoid"
          :title="item.title"
          :subtitle="item.subtitle"
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
  name: 'class2',
  components: {
    videos,
  },
  data() {
    return {
      items: [
        {
          classes: '1',
          videoid: 'JzRMxbTf-bc',
          icon: 'mdi-video-high-definition',
          title: ' 1. Pre Speech Training ท่าฝึกออกเสียง',
          subtitle:
            'ท่าออกกำลังกายและบริหารอวัยวะที่ช่วยในการออกเสียง (Pre Speech Training) สำหรับผู้ป่วย "กลืนลำบาก" (Dysphagia) และ "บกพร่องการสื่อสาร" (Aphasia)<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะบกพร่องการสื่อสาร  ภาวะกลืนลำบากระยะปาก (Oral Dysphagia)<br/>- มีน้ำลายไหลมุมปาก (Drooling)<br/>- มุมปากตกข้างหนึ่งหรือสองข้าง (Asymmetry of Lips)<br/>- ไม่สามารถสื่อสารเป็นคำได้ นึกคำออกแต่สื่อสารออกมาไม่ได้ หรือสื่อสารไม่ได้',
        },
        {
          classes: '2',
          videoid: 'RYL_TBY5OSw',
          icon: 'mdi-video-high-definition',
          title: ' 2. Tongue Exercise ท่าออกกำลังกล้ามเนื้อลิ้น',
          subtitle:
            '   ท่าออกกำลังกายและบริหารกล้ามเนื้อลิ้น (Tongue Exercise) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะปาก (Oral Dysphagia) ที่มีปัญหาดังนี้<br/>- การเคลื่อนไหวลิ้นไม่ดี (Poor Tongue Control)<br/>- มีอาหารค้างบริเวณกระพุ้งแก้ม (Pocketing)<br/>- อาหารไม่ค่อยลงไปในหลอดอาหาร กลืนเบาที่เกิดจากการดันอาหารได้เบา (Base of Tongue Weakness)<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
        },
        {
          classes: '3',
          videoid: 'zSjjmLNH-Qg',
          icon: 'mdi-video-high-definition',
          title: ' 3. Vocal Cord Adduction ท่าบริหารเส้นเสียง',
          subtitle:
            'ท่าออกกำลังกายและบริหารเส้นเสียง (Vocal Cord Adduction) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) หรือเส้นเสียงออกแรง (Vocal Fold Weakness)<br/><p class="font-weight-black">วิธีการ</p><br/>1. ประสานมือ หรือดันเบาะเก้าอี้ หรือดันมือกับผู้ช่วย<br/>2. ออกแรงดัน ต้านแรง พร้อมออกเสียง "อะ" ดัง ๆ <br/>(ให้เสียงออกมาจากช่องท้อง)<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากที่มีภาวะเส้นเสียงอ่อนแรง (Vocal Fold Paralysis) ที่มีปัญหาดังนี้<br/>- มีเสียงแหบพร่า (Hoarseness Voice) หรือ เสียงเครือ (Wet Voice) ขณะพูด หรือหลังจากกินางปาก<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
        },
        {
          classes: '4',
          videoid: 'lsI3pfA6-Ik',
          icon: 'mdi-video-high-definition',
          title: ' 4. Chin Tuck Against Resistance (C.T.A.R.)',
          subtitle:
            'ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/><p class="font-weight-black">วิธีการ</p><br/>1. เตรียมอุปกรณ์ที่มีแรงต้าน เช่น ลูกบอลฟองน้ำ ลูกบอลยาง<br/>2. วางอุปกรณ์นั้นบริเวณใต้คาง<br/>3. ก้มหัว คางชิดอก ต้านแรงกับอุปกรณ์ค้างไว้ 30 วินาที หรือก้มหัวบีบอุปกรณ์นั้นแล้วปล่อย 30 ครั้ง<br/>4. ทำซ้ำ 3- 4  เซท<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้<br/>- การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา<br/>- การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง<br/>- สำลักระหว่างกลืน<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
        },
        {
          classes: '5',
          videoid: 'RYL_TBY5OSw',
          icon: 'mdi-video-high-definition',
          title:
            " 5. Shaker's Exercise ท่าออกกำลังกายกล้ามเนื้อที่ช่วยในการกลืน",
          subtitle:
            'ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/> <p class="font-weight-black">วิธีการ</p><br/>1. นอนราบกับเตียง<br/>2. มือวางข้างลำตัว หัวราบกับเตียง<br/>3. ยกหัวมองปลายเท้า (ให้ไหล่วาบราบกับเตียง) ค้างไว้ 30 วินาที หรือยกหัวขึ้นมองปลายเท้า - วางหัวลง 30 ครั้ง<br/>4. ทำซ้ำ 3- 4  เซท<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้<br/>- การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา<br/>- การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง<br/>- สำลักระหว่างกลืน<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
        },
        {
          classes: '6',
          videoid: 'RjorFPINfCc',
          icon: 'mdi-video-high-definition',
          title:
            ' 6. Oral Hygiene การทำความสะอาดช่องปากผู้ป่วยโรคหลอดเลือดสมอง',
          subtitle:
            'ความสะอาดในช่องปากเป็นสิ่งสำคัญลำดับต้น ๆ สำหรับผู้ป่วยโรคหลอดเลือดสมองในระยะแรก ๆ โดยเฉพาะผู้ป่วยที่ยังไม่สามารถรับประทานทางปาก หรือมีภาวะกลืนลำบากได้<br/> <p class="font-weight-black">วัตถุประสงค์ของการทำความสะอาดในช่องปาก</p><br/> - ป้องกันภาวะแทรกซ้อน ภาวะติดเชื้อในปอดจากการสำลักแบคทีเรียในช่องปาก<br/> - สร้างสุขลักษณะที่ดี - ส่งเสริมคุณภาพชีวิตที่ดี <br/> - เพิ่มโอกาสการฟื้นฟูภาวะกลืนลำบาก',
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
.header-color {
  color: #be5683;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
</style>
