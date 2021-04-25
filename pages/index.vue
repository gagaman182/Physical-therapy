<template>
  <v-container grid-list-xlfluid>
    <v-layout row wrap>
      <v-col cols="12">
        <v-toolbar color="#ce1f6a" class="white--text">
          <v-card-title class="headline font-weight-bold">
            ภาวะกลืนลำบาก
          </v-card-title>
        </v-toolbar>

        <v-card height="100%">
          <v-alert
            border="bottom"
            colored-border
            class="header-color text-center display-1"
            color="#ce1f6a"
            elevation="2"
            ><h4>กลืนลำบาก บำบัดไม่ยาก หากรู้วิธี.</h4>
          </v-alert>
          <v-row align="center" class="mx-2">
            <v-col cols="12" md="4">
              <v-card
                class="mx-auto"
                outlined
                color="#ff9a8c"
                style="height: 220px"
              >
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      ความรู้ทั่วไป
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace">mdi-jabber </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class1"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card
                class="mx-auto"
                outlined
                color="#ff9a8c"
                style="height: 220px"
              >
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การบำบัดฟื้นฟูการกลืน (1-4)
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace"
                    >mdi-calendar-heart
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class2"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#ff9a8c">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      อาหารฝึกกลืน
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace">mdi-food </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class3"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#ff9a8c">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การฝึกหายใจและการฝึกไอ (6)
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace">mdi-airballoon </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class4"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#ff9a8c">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      การทำความสะอาดช่องปาก (5)
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace"
                    >mdi-toothbrush-paste
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class5"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" outlined color="#ff9a8c">
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="headline mb-1 header-color">
                      ติดต่อเรา
                    </v-list-item-title>
                  </v-list-item-content>
                  <v-icon size="150px" color="#c67ace"
                    >mdi-hospital-building
                  </v-icon>
                </v-list-item>

                <v-card-actions>
                  <v-btn
                    outlined
                    color="#d8f8b7"
                    to="/class6"
                    target="_blank"
                    nuxt
                    x-large
                  >
                    <v-icon size="40px">mdi-cursor-default-click </v-icon>
                    <p class="headline text-decoration-underline">คลิก</p>
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
  color: #ce1f6a;
}

.main-header-color {
  color: #c67ace;
}
</style>
