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
    <!-- video1 -->
    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                  Food Modification อาหารระดับที่ 1
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  No oral intake งดอาหารทางปาก
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
                video-id="4kb2E-8OeHw"
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
                  Food Modification อาหารระดับที่ 2
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Tube dependence with minimal/inconsistent oral intake
                  รับประทานอาการทางสายยางและรับประทานอาหารทางปากได้เล็กน้อย
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
                video-id="5LQAxhq7Vsc"
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
                  Food Modification อาหารระดับที่ 3
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Tube supplement with consistence oral intake
                  รับประทานอาการทางสายเสริมจากอาหารทางปาก
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
                video-id="j-12oXZ6ZQE"
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
                  Food Modification อาหารระดับที่ 4
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Total oral intake a single consistency
                  รับประทานอาการทางปากด้วยอาหารอ่อนเนื้อเดียว
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
                video-id="8LcY_nalfs0"
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
                  Food Modification อาหารระดับที่ 5
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Total oral intake of multiple consistencies requiring special
                  preparation
                  รับประทานอาการทางปากด้วยอาหารหลายประเภทที่ต้องบด/สับก่อน
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
                video-id="_UX4ZlRxA_o"
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
                  Food Modification อาหารระดับที่ 6
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Total oral intake with no special preparation but must avoid
                  specific food or liquid items
                  รับประทานอาการทางปากปกติแต่หลีกเลี่ยงอาหารแข็งและน้ำ
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
                video-id="G0YBxl5W35Y"
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
    <!-- video7 -->
    <v-col cols="12">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-row>
              <v-col cols="10"
                ><v-list-item-title class="headline mb-1">
                  Food Modification อาหารระดับที่ 7
                </v-list-item-title>
                <div class="my-4 subtitle-1">
                  Total oral intake with no restriction
                  รับประทานอาการทางปากได้ตามปกติ
                </div></v-col
              >

              <v-col cols="2">
                <v-icon size="85px" color="#ffe78f"
                  >mdi-video-high-definition
                </v-icon>
                <v-checkbox
                  v-model="seevideo7"
                  @change="noblur7"
                  label="ดูคลิปวีดีโอ"
                  color="#efbbcf"
                ></v-checkbox>
              </v-col>
            </v-row>

            <!-- <v-list-item-subtitle>ภาวะกลืนลำบาก</v-list-item-subtitle> -->

            <div v-blur="blurConfig7" class="text-center">
              <youtube
                video-id="_tt-MCVhQnw"
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
      blurConfig7: {
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
      seevideo7: false,
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
    noblur7() {
      this.blurConfig7.isBlurred = !this.blurConfig7.isBlurred
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
