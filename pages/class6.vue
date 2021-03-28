<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-toolbar color="#efbbcf" class="main-header-color">
        <v-card-title class="headline font-weight-bold">
          <v-icon class="text--darken-2 main-header-color" medium>
            mdi-hospital-building
          </v-icon>
          &nbsp; ติดต่อเรา
        </v-card-title>
      </v-toolbar>
    </v-col>

    <v-col cols="12" class="text-center">
      <v-card class="mx-auto" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-list-item-title class="headline mb-1">
              ติดต่อสอบถามเพิ่มเติม </br>กลุ่มงานเวชกรรมฟื้นฟู โรงพยาบาลหาดใหญ่</br>
              182 ถ.รัถการ ต.หาดใหญ่ อ.หาดใหญ่ จ. สงขลา</br>
              โทร 074-273100 ต่อ 8207
            </v-list-item-title>
            <!-- <v-list-item-subtitle>ติดต่อเรา</v-list-item-subtitle> -->
            <div class="d-flex flex-column justify-space-between align-center">
          <img src="@/assets/hy/hy10682.jpg">
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'class6',

  data() {
    return {
      
    }
  },
  methods: {},
}
</script>
<style scoped>
.main-header-color {
  color: #ef4f4f;
}

</style>
