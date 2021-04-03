
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
              <!-- video1 -->
              <v-col cols="12">
                <v-card class="mx-auto" outlined>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-row>
                        <v-col cols="10"
                          ><v-list-item-title class="headline mb-1">
                            1. Pre Speech Training ท่าฝึกออกเสียง
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                            ท่าออกกำลังกายและบริหารอวัยวะที่ช่วยในการออกเสียง (Pre Speech Training) สำหรับผู้ป่วย "กลืนลำบาก" (Dysphagia) และ "บกพร่องการสื่อสาร" (Aphasia)<br/>
                            <p class="font-weight-black">ข้อบ่งชี้</p>
                            **เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะบกพร่องการสื่อสาร  ภาวะกลืนลำบากระยะปาก (Oral Dysphagia)<br/>
                            - มีน้ำลายไหลมุมปาก (Drooling)<br/>
                            - มุมปากตกข้างหนึ่งหรือสองข้าง (Asymmetry of Lips)<br/>
                            - ไม่สามารถสื่อสารเป็นคำได้ นึกคำออกแต่สื่อสารออกมาไม่ได้ หรือสื่อสารไม่ได้
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
                          video-id="JzRMxbTf-bc"
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
                            2. Tongue Exercise ท่าออกกำลังกล้ามเนื้อลิ้น
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                            ท่าออกกำลังกายและบริหารกล้ามเนื้อลิ้น (Tongue Exercise) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/>
                            <p class="font-weight-black">ข้อบ่งชี้</p>
                            **เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะปาก (Oral Dysphagia) ที่มีปัญหาดังนี้<br/>
                            - การเคลื่อนไหวลิ้นไม่ดี (Poor Tongue Control)<br/>
                            - มีอาหารค้างบริเวณกระพุ้งแก้ม (Pocketing)<br/>
                            - อาหารไม่ค่อยลงไปในหลอดอาหาร กลืนเบาที่เกิดจากการดันอาหารได้เบา (Base of Tongue Weakness)<br/>
                            **แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating))
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
                          video-id="RYL_TBY5OSw"
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
              <!-- video3 -->
              <v-col cols="12">
                <v-card class="mx-auto" outlined>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-row>
                        <v-col cols="10"
                          ><v-list-item-title class="headline mb-1">
                            3. Vocal Cord Adduction ท่าบริหารเส้นเสียง
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                           ท่าออกกำลังกายและบริหารเส้นเสียง (Vocal Cord Adduction) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) หรือเส้นเสียงออกแรง (Vocal Fold Weakness)<br/>
                             <p class="font-weight-black">วิธีการ</p>
                            1. ประสานมือ หรือดันเบาะเก้าอี้ หรือดันมือกับผู้ช่วย<br/>
                            2. ออกแรงดัน ต้านแรง พร้อมออกเสียง "อะ" ดัง ๆ 
                            (ให้เสียงออกมาจากช่องท้อง)<br/>
                            <p class="font-weight-black">ข้อบ่งชี้</p>
                            **เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากที่มีภาวะเส้นเสียงอ่อนแรง (Vocal Fold Paralysis) ที่มีปัญหาดังนี้<br/>
                             - มีเสียงแหบพร่า (Hoarseness Voice) หรือ เสียงเครือ (Wet Voice) ขณะพูด หรือหลังจากกินางปาก<br/>
                            **แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating))
                          </div></v-col
                        >

                        <v-col cols="2">
                          <v-icon size="85px" color="#ffe78f"
                            >mdi-video-high-definition
                          </v-icon>
                          <v-checkbox
                            v-model="seevideo3"
                            @change="noblur3"
                            label="ดูคลิปวีดีโอ"
                            color="#efbbcf"
                          ></v-checkbox>
                        </v-col>
                      </v-row>

                      <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

                      <div v-blur="blurConfig3" class="text-center">
                        <youtube
                          video-id="zSjjmLNH-Qg"
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
              <!-- video4 -->
              <v-col cols="12">
                <v-card class="mx-auto" outlined>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-row>
                        <v-col cols="10"
                          ><v-list-item-title class="headline mb-1">
                            4. Chin Tuck Against Resistance (C.T.A.R.)<br/>
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                            ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) <br/>
                                <p class="font-weight-black">วิธีการ</p>
                              1. เตรียมอุปกรณ์ที่มีแรงต้าน เช่น ลูกบอลฟองน้ำ ลูกบอลยาง<br/>
                              2. วางอุปกรณ์นั้นบริเวณใต้คาง<br/>
                              3. ก้มหัว คางชิดอก ต้านแรงกับอุปกรณ์ค้างไว้ 30 วินาที หรือก้มหัวบีบอุปกรณ์นั้นแล้วปล่อย 30 ครั้ง<br/>
                              4. ทำซ้ำ 3- 4  เซท<br/>

                              <p class="font-weight-black">ข้อบ่งชี้</p>
                              **เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้<br/>
                              - การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา<br/>
                              - การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง<br/>
                              - สำลักระหว่างกลืน<br/>
                              **แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating))
                          </div></v-col
                        >

                        <v-col cols="2">
                          <v-icon size="85px" color="#ffe78f"
                            >mdi-video-high-definition
                          </v-icon>
                          <v-checkbox
                            v-model="seevideo4"
                            @change="noblur4"
                            label="ดูคลิปวีดีโอ"
                            color="#efbbcf"
                          ></v-checkbox>
                        </v-col>
                      </v-row>

                      <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

                      <div v-blur="blurConfig4" class="text-center">
                        <youtube
                          video-id="lsI3pfA6-Ik"
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
              <!-- video5 -->
              <v-col cols="12">
                <v-card class="mx-auto" outlined>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-row>
                        <v-col cols="10"
                          ><v-list-item-title class="headline mb-1">
                            5. Shaker's Exercise ท่าออกกำลังกายกล้ามเนื้อที่ช่วยในการกลืน
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                            ท่าออกกำลังกายและบริหารกล้ามเนื้อบริเวณช่วงคอ (Pharyngeal Region) สำหรับผู้ป่วย "ภาวะกลืนลำบาก"  (Dysphagia) 
                              <p class="font-weight-black">วิธีการ</p>
                              1. นอนราบกับเตียง
                              2. มือวางข้างลำตัว หัวราบกับเตียง
                              3. ยกหัวมองปลายเท้า (ให้ไหล่วาบราบกับเตียง) ค้างไว้ 30 วินาที หรือยกหัวขึ้นมองปลายเท้า - วางหัวลง 30 ครั้ง
                              4. ทำซ้ำ 3- 4  เซท

                              <p class="font-weight-black">ข้อบ่งชี้</p>
                              **เหมาะสำหรับผู้ป่วยหรือผู้รับบริการที่มีภาวะกลืนลำบากในระยะคอหอย (Pharyngeal Dysphagia) ที่มีปัญหาดังนี้
                              - การยกตัวของกล่องเสียงบกพร่อง/อ่อนแรง/ยกตัวได้เบา
                              - การบีบตัวของหลอดอาหารบกพร่อง/ อ่อนแรงข้างใดข้างหนึ่งหรือสองข้าง
                              - สำลักระหว่างกลืน
                              **แนะนำให้ทำก่อนรับประทานอาหารทุกมื้อ (ก่อนให้อาหารทางสาย (feeding), ทานอาหารทางปาก (eating))
                          </div></v-col
                        >

                        <v-col cols="2">
                          <v-icon size="85px" color="#ffe78f"
                            >mdi-video-high-definition
                          </v-icon>
                          <v-checkbox
                            v-model="seevideo5"
                            @change="noblur5"
                            label="ดูคลิปวีดีโอ"
                            color="#efbbcf"
                          ></v-checkbox>
                        </v-col>
                      </v-row>

                      <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

                      <div v-blur="blurConfig5" class="text-center">
                        <youtube
                          video-id="JQXaAZeQn2o&t=45s"
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
              <!-- video6 -->
              <v-col cols="12">
                <v-card class="mx-auto" outlined>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-row>
                        <v-col cols="10"
                          ><v-list-item-title class="headline mb-1">
                            6. Oral Hygiene การทำความสะอาดช่องปากผู้ป่วยโรคหลอดเลือดสมอง
                          </v-list-item-title>
                          <div class="my-4 subtitle-1">
                            ความสะอาดในช่องปากเป็นสิ่งสำคัญลำดับต้น ๆ สำหรับผู้ป่วยโรคหลอดเลือดสมอง
                            ในระยะแรก ๆ โดยเฉพาะผู้ป่วยที่ยังไม่สามารถรับประทานทางปาก หรือมีภาวะกลืนลำบากได้<br/>
                            <p class="font-weight-black">วัตถุประสงค์ของการทำความสะอาดในช่องปาก</p>
                            - ป้องกันภาวะแทรกซ้อน ภาวะติดเชื้อในปอดจากการสำลักแบคทีเรียในช่องปาก<br/>
                            - สร้างสุขลักษณะที่ดี<br/>
                            - ส่งเสริมคุณภาพชีวิตที่ดี<br/>
                            - เพิ่มโอกาสการฟื้นฟูภาวะกลืนลำบาก
                          </div></v-col
                        >

                        <v-col cols="2">
                          <v-icon size="85px" color="#ffe78f"
                            >mdi-video-high-definition
                          </v-icon>
                          <v-checkbox
                            v-model="seevideo6"
                            @change="noblur6"
                            label="ดูคลิปวีดีโอ"
                            color="#efbbcf"
                          ></v-checkbox>
                        </v-col>
                      </v-row>

                      <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

                      <div v-blur="blurConfig6" class="text-center">
                        <youtube
                          video-id="RjorFPINfCc"
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
              name: 'class3',

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
                  blurConfig3: {
                    isBlurred: true,
                    opacity: 0.1,
                    filter: 'blur(1.8px)',
                    transition: 'all .3s linear',
                  },
                  blurConfig4: {
                    isBlurred: true,
                    opacity: 0.1,
                    filter: 'blur(1.8px)',
                    transition: 'all .3s linear',
                  },
                  blurConfig5: {
                    isBlurred: true,
                    opacity: 0.1,
                    filter: 'blur(1.8px)',
                    transition: 'all .3s linear',
                  },
                  blurConfig6: {
                    isBlurred: true,
                    opacity: 0.1,
                    filter: 'blur(1.8px)',
                    transition: 'all .3s linear',
                  },
                 
                  seevideo1: false,
                  seevideo2: false,
                  seevideo3: false,
                  seevideo4: false,
                  seevideo5: false,
                  seevideo6: false,
                 
                }
              },
              methods: {
                noblur1() {
                  this.blurConfig1.isBlurred = !this.blurConfig1.isBlurred
                },
                noblur2() {
                  this.blurConfig2.isBlurred = !this.blurConfig2.isBlurred
                },
                noblur3() {
                  this.blurConfig3.isBlurred = !this.blurConfig3.isBlurred
                },
                noblur4() {
                  this.blurConfig4.isBlurred = !this.blurConfig4.isBlurred
                },
                noblur5() {
                  this.blurConfig5.isBlurred = !this.blurConfig5.isBlurred
                },
                noblur6() {
                  this.blurConfig6.isBlurred = !this.blurConfig6.isBlurred
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
        </v-card-title></v-toolbar
      ></v-col
    ></v-row
  >
</template>
