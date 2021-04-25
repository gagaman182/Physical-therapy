<template>
  <v-row>
    <v-col cols="12" class="text-center" dark>
      <v-toolbar color="#ce1f6a" class="white--text">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 white--text" medium
            >mdi-account-settings
          </v-icon>
          &nbsp; ผู้รับบริการ
        </v-card-title>
      </v-toolbar>
      <v-alert
        border="bottom"
        colored-border
        class="header-color text-center display-1"
        color="#ce1f6a"
        elevation="2"
        ><h3>การบำบัดฟื้นฟู</h3>
      </v-alert>
    </v-col>
    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="12">
                <v-toolbar flat color="#c67ace" dark>
                  <v-toolbar-title
                    >กรุณาเลือกอาการของท่าน (เลือกได้มากกว่า 1
                    ข้อ)</v-toolbar-title
                  >
                  <v-spacer></v-spacer>
                  <v-btn
                    :loading="loading"
                    x-large
                    class="ma-1"
                    color="#ff79cd"
                    @click="refresh"
                    align="end"
                    dark
                  >
                    <v-icon medium>mdi-refresh </v-icon>
                  </v-btn>
                </v-toolbar>
              </v-col>
              <v-col cols="12"
                ><v-alert
                  color="#d8f8b7"
                  dense
                  class="header-color font-weight-bold"
                >
                  <v-icon size="25px" color="#ce1f6a">mdi-bullhorn </v-icon>
                  เมื่อผู้รับบริการเลือกระบบจะลิงค์ไปยังวิธีการบำบัดฟื้นฟูที่ต้องฝึกตามตัวเลขด้านหลัง
                </v-alert>
              </v-col>
              <v-col cols="12" v-if="showcheck">
                <v-row class="light--text">
                  <v-col cols="6" class="text-center">
                    <h4>เลือกอาการ</h4>
                  </v-col>
                  <v-col cols="6">
                    <h4>รายละเอียดอาการ</h4>
                  </v-col>
                </v-row>
                <v-row class="light--text">
                  <v-col cols="3"> </v-col>
                  <v-col cols="3" class="text-center">
                    <v-checkbox
                      v-model="checkclass1"
                      color="#c67ace"
                      value="class1"
                    ></v-checkbox>
                  </v-col>
                  <v-col cols="6"
                    ><p class="my-4 subtitle-1">
                      -น้ำลายไหล<br />
                      -น้ำหกออกจากมุมุปาก<br />
                      -ปากเบี้ยว<br />
                      -มุมปากตก<br />
                      -อ้าปากได้ไม่กว้าง<br />
                      -ลิ้นเคลื่อนไหวได้ดี
                    </p>
                    <v-divider></v-divider>
                  </v-col>
                  <v-col cols="3"> </v-col>
                  <v-col cols="3">
                    <v-checkbox
                      v-model="checkclass2"
                      color="#c67ace"
                      value="class2"
                    ></v-checkbox>
                  </v-col>
                  <v-col cols="6"
                    ><p class="my-4 subtitle-1">
                      -สำลัก,ไอ,จาม ขณะรับประทานอาการ/หลังรับประทานอาหาร<br />
                      -เสียงพล่าเครือ<br />
                      -มีเสียงหลังรับประทานอาหาร
                    </p>
                    <v-divider></v-divider>
                  </v-col>
                  <v-col cols="3"> </v-col>
                  <v-col cols="3" class="text-center">
                    <v-checkbox
                      v-model="checkclass3"
                      color="#c67ace"
                      value="class3"
                    ></v-checkbox>
                  </v-col>
                  <v-col cols="6"
                    ><p class="my-4 subtitle-1">
                      -กลืนน้ำลายไม่ได้<br />
                      -กลืนติด<br />
                      -กลืนไม่ลง
                    </p>
                  </v-col>
                  <v-col cols="12" class="button" align="center">
                    <v-btn
                      class="ma-2"
                      color="#ce1f6a"
                      @click="runvideo"
                      x-large
                      dark
                    >
                      <div class="font-weight-bold">ประมวลผล</div>
                    </v-btn>
                  </v-col>
                  <!-- <v-col cols="3"> </v-col>
                  <v-col cols="8"> </v-col> -->
                </v-row>
              </v-col>
            </v-row>
          </v-list-item-content>
        </v-list-item>
      </v-card>
    </v-col>
    <v-col cols="12">
      <div class="columns is-mobile" v-for="item in items" :key="item.videoid1">
        <video_patient
          v-if="item.videoselect"
          :videoid="item.videoid"
          :title="item.title"
          :subtitle="item.subtitle"
          :content="item.content"
          :icon="item.icon"
          :classes="item.classes"
        ></video_patient>
      </div>
    </v-col>
  </v-row>
</template>
<script>
import video_patient from '@/components/video_patient'
export default {
  name: 'patient',
  components: {
    video_patient,
  },
  data() {
    return {
      showvideo: false,
      showcheck: true,
      checkclass1: '',
      checkclass2: '',
      checkclass3: '',
      items: [
        {
          videoselect: false,
          classes: '1',
          videoid: 'JzRMxbTf-bc',
          icon: 'mdi-video-high-definition',
          title:
            ' 1. การบริหารกล้ามเนื้อปาก ขากรรไกร Pre Speech Training ท่าฝึกออกเสียง',
          subtitle:
            'ท่าออกกำลังกายและบริหารอวัยวะที่ช่วยในการออกเสียง (Pre Speech Training) สำหรับผู้ป่วย "กลืนลำบาก" (Dysphagia) และ "บกพร่องการสื่อสาร" (Aphasia)<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะบกพร่องการสื่อสาร  ภาวะกลืนลำบากระยะปาก (Oral Dysphagia)<br/>- มีน้ำลายไหลมุมปาก (Drooling)<br/>- มุมปากตกข้างหนึ่งหรือสองข้าง (Asymmetry of Lips)<br/>- ไม่สามารถสื่อสารเป็นคำได้ นึกคำออกแต่สื่อสารออกมาไม่ได้ หรือสื่อสารไม่ได้',
          show: false,
        },
        {
          videoselect: false,
          classes: '2',
          videoid: 'RYL_TBY5OSw',
          icon: 'mdi-video-high-definition',
          title: ' 2. Tongue Exercise ท่าออกกำลังกล้ามเนื้อลิ้น',
          subtitle:
            '   ท่าออกกำลังกายและบริหารกล้ามเนื้อลิ้น (Tongue Exercise) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะปาก (Oral Dysphagia) ที่มีปัญหาดังนี้<br/>- การเคลื่อนไหวลิ้นไม่ดี (Poor Tongue Control)<br/>- มีอาหารค้างบริเวณกระพุ้งแก้ม (Pocketing)<br/>- อาหารไม่ค่อยลงไปในหลอดอาหาร กลืนเบาที่เกิดจากการดันอาหารได้เบา (Base of Tongue Weakness)<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
          show: false,
        },
        {
          videoselect: false,
          classes: '3',
          videoid: 'zSjjmLNH-Qg',
          icon: 'mdi-video-high-definition',
          title: ' 3. Vocal Cord Adduction ท่าบริหารเส้นเสียง',
          subtitle:
            'ท่าออกกำลังกายและบริหารเส้นเสียง (Vocal Cord Adduction) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) หรือเส้นเสียงออกแรง (Vocal Fold Weakness)<br/><p class="font-weight-black">วิธีการ</p><br/>1. ประสานมือ หรือดันเบาะเก้าอี้ หรือดันมือกับผู้ช่วย<br/>2. ออกแรงดัน ต้านแรง พร้อมออกเสียง "อะ" ดัง ๆ <br/>(ให้เสียงออกมาจากช่องท้อง)<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากที่มีภาวะเส้นเสียงอ่อนแรง (Vocal Fold Paralysis) ที่มีปัญหาดังนี้<br/>- มีเสียงแหบพร่า (Hoarseness Voice) หรือ เสียงเครือ (Wet Voice) ขณะพูด หรือหลังจากกินางปาก<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
          show: false,
        },
        {
          videoselect: false,
          classes: '4.1',
          videoid: 'lsI3pfA6-Ik',
          icon: 'mdi-video-high-definition',
          title: ' 4.1 Chin Tuck Against Resistance (C.T.A.R.)',
          subtitle:
            'ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/><p class="font-weight-black">วิธีการ</p><br/>1. เตรียมอุปกรณ์ที่มีแรงต้าน เช่น ลูกบอลฟองน้ำ ลูกบอลยาง<br/>2. วางอุปกรณ์นั้นบริเวณใต้คาง<br/>3. ก้มหัว คางชิดอก ต้านแรงกับอุปกรณ์ค้างไว้ 30 วินาที หรือก้มหัวบีบอุปกรณ์นั้นแล้วปล่อย 30 ครั้ง<br/>4. ทำซ้ำ 3- 4  เซท<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้<br/>- การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา<br/>- การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง<br/>- สำลักระหว่างกลืน<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
          show: false,
        },
        {
          videoselect: false,
          classes: '4.2',
          videoid: 'RYL_TBY5OSw',
          icon: 'mdi-video-high-definition',
          title:
            " 4.2 Shaker's Exercise ท่าออกกำลังกายกล้ามเนื้อที่ช่วยในการกลืน",
          subtitle:
            'ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/> <p class="font-weight-black">วิธีการ</p><br/>1. นอนราบกับเตียง<br/>2. มือวางข้างลำตัว หัวราบกับเตียง<br/>3. ยกหัวมองปลายเท้า (ให้ไหล่วาบราบกับเตียง) ค้างไว้ 30 วินาที หรือยกหัวขึ้นมองปลายเท้า - วางหัวลง 30 ครั้ง<br/>4. ทำซ้ำ 3- 4  เซท<br/><p class="font-weight-black">ข้อบ่งชี้</p><br/>**เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้<br/>- การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา<br/>- การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง<br/>- สำลักระหว่างกลืน<br/>**แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating)) ',
          show: false,
        },
        {
          videoselect: false,
          classes: '5',
          videoid: 'RjorFPINfCc',
          icon: 'mdi-video-high-definition',
          title: ' 5 Oral Hygiene การทำความสะอาดช่องปากผู้ป่วยโรคหลอดเลือดสมอง',
          subtitle:
            'ความสะอาดในช่องปากเป็นสิ่งสำคัญลำดับต้น ๆ สำหรับผู้ป่วยโรคหลอดเลือดสมอง ในระยะแรก ๆ โดยเฉพาะผู้ป่วยที่ยังไม่สามารถรับประทานทางปาก หรือมีภาวะกลืนลำบากได้ <br/> <p class="font-weight-black">วัตถุประสงค์ของการทำความสะอาดในช่องปาก</p><br/>- ป้องกันภาวะแทรกซ้อน ภาวะติดเชื้อในปอดจากการสำลักแบคทีเรียในช่องปาก<br /> - สร้างสุขลักษณะที่ดี<br/>- ส่งเสริมคุณภาพชีวิตที่ดี<br/>- เพิ่มโอกาสการฟื้นฟูภาวะกลืนลำบาก',
          show: false,
        },
        {
          videoselect: false,
          classes: '6.1',
          videoid: 'Drz3xtM_MMc',
          icon: 'mdi-video-high-definition',
          title: ' 6.1 Cough Training (ท่าฝึกการไอสำหรับผู้ป่วยกลืนลำบาก)',
          subtitle: 'ระบบหายใจที่ดี สัมพันธ์กับการกลืนที่ดีเช่นเดียวกัน',
          show: false,
        },
        {
          videoselect: false,
          classes: '6.2',
          videoid: 'HsOzr8sIxHs',
          icon: 'mdi-video-high-definition',
          title: ' 6.2 Breathing Exercise2 การฝึกการหายใจท่าที่ 2',
          subtitle:
            '    การหายใจกับการกลืนมีความสัมพันธ์กัน การฝึกหายใจเป็นจังหวะที่ดีจะช่วยให้การกลืนปลอดภัยเช่นเดียวกัน',
          show: false,
        },
      ],
    }
  },
  methods: {
    runvideo() {
      if (!this.checkclass1 && !this.checkclass2 && !this.checkclass3) {
        this.$swal({
          title: 'แจ้งเตือน',
          text: 'ท่านยังไม่ได้เลือกอาการ',
          icon: 'error',
          confirmButtonText: 'ตกลง',
        })
      } else {
        if (this.checkclass1 && this.checkclass2 && this.checkclass3) {
          this.items[0].videoselect = true
          this.items[1].videoselect = true
          this.items[2].videoselect = true
          this.items[3].videoselect = true
          this.items[4].videoselect = true
          this.items[5].videoselect = true
          this.items[6].videoselect = true
          this.items[7].videoselect = true
          this.showcheck = false
        } else if (this.checkclass1 && this.checkclass2) {
          this.items[0].videoselect = true
          this.items[1].videoselect = true
          this.items[2].videoselect = true
          this.items[3].videoselect = false
          this.items[4].videoselect = false
          this.items[5].videoselect = true
          this.items[6].videoselect = true
          this.items[7].videoselect = true
          this.showcheck = false
        } else if (this.checkclass1 && this.checkclass3) {
          this.items[0].videoselect = true
          this.items[1].videoselect = true
          this.items[2].videoselect = false
          this.items[3].videoselect = true
          this.items[4].videoselect = true
          this.items[5].videoselect = true
          this.items[6].videoselect = false
          this.items[7].videoselect = false
          this.showcheck = false
        } else if (this.checkclass2 && this.checkclass3) {
          this.items[0].videoselect = false
          this.items[1].videoselect = false
          this.items[2].videoselect = true
          this.items[3].videoselect = true
          this.items[4].videoselect = true
          this.items[5].videoselect = true
          this.items[6].videoselect = true
          this.items[7].videoselect = true
          this.showcheck = false
        } else if (this.checkclass1) {
          this.items[0].videoselect = true
          this.items[1].videoselect = true
          this.items[2].videoselect = false
          this.items[3].videoselect = false
          this.items[4].videoselect = false
          this.items[5].videoselect = true
          this.items[6].videoselect = false
          this.items[7].videoselect = false
          this.showcheck = false
        } else if (this.checkclass2) {
          this.items[0].videoselect = false
          this.items[1].videoselect = false
          this.items[2].videoselect = true
          this.items[3].videoselect = false
          this.items[4].videoselect = false
          this.items[5].videoselect = true
          this.items[6].videoselect = true
          this.items[7].videoselect = true
          this.showcheck = false
        } else if (this.checkclass3) {
          this.items[0].videoselect = false
          this.items[1].videoselect = false
          this.items[2].videoselect = false
          this.items[3].videoselect = true
          this.items[4].videoselect = true
          this.items[5].videoselect = true
          this.items[6].videoselect = false
          this.items[7].videoselect = false
          this.showcheck = false
        }
      }
    },
    refresh() {
      this.$swal({
        title: 'แจ้งเตือน',
        text: 'อ่านรายละเอียดและระบุอาการของท่านใหม่ ',
        icon: 'success',
        confirmButtonText: 'ตกลง',
      })
      this.showcheck = true
      this.items[0].videoselect = false
      this.items[1].videoselect = false
      this.items[2].videoselect = false
      this.items[3].videoselect = false
      this.items[4].videoselect = false
      this.items[5].videoselect = false
      this.items[6].videoselect = false
      this.items[7].videoselect = false
      this.checkclass1 = ''
      this.checkclass2 = ''
      this.checkclass3 = ''
    },
  },

  mounted() {},
}
</script>

<style scoped>
.header-color {
  color: #ce1f6a;
}
iframe {
  width: 100%;
  max-width: 650px; /* Also helpful. Optional. */
}
</style>
