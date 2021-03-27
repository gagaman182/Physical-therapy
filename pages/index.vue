<template>
  <v-container grid-list-xlfluid>
    <v-layout row wrap>
      <v-col cols="12">
        <v-toolbar color="#c3aed6" class="main-header-color">
          <v-card-title class="headline font-weight-bold">
            ภาวะกลืนลำบาก
          </v-card-title>
        </v-toolbar>

        <v-card height="100%">
          <v-alert
            border="bottom"
            colored-border
            class="header-color"
            color="#ffe78f"
            elevation="2"
            ><h4>กลืนลำบาก บำบัดไม่ยาก หากรู้วิธี.</h4>
          </v-alert>
          <v-row align="center" class="mx-2">
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      ความรู้ทั่วไป
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f">mdi-jabber </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class1"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การบำบัดฟื้นฟู
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f"
                    >mdi-calendar-heart
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class2"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      อาหารฝึกกลืน
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f">mdi-food </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class3"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การฝึกหายใจและการฝึกกลืน
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f">mdi-airballoon </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class4"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การทำความสะอาดช่องปาก
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f"
                    >mdi-toothbrush-paste
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class5"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#c3aed6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      ติดต่อเรา
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="85px" color="#ffe78f"
                    >mdi-hospital-building
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    rounded
                    color="#ffe78f"
                    to="/class6"
                    target="_blank"
                    nuxt
                  >
                    <v-icon size="30px">mdi-cursor-default-click </v-icon>
                    <h3>เลือก</h3>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  components: {},
}
</script>
<style scoped>
.header-color {
  color: #be5683;
}

.main-header-color {
  color: #ffe78f;
}
</style>
