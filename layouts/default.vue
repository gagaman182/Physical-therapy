<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      color="#ce1f6a"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon class="white--text font-weight-bold">{{
              item.icon
            }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title
              class="white--text font-weight-bold"
              v-text="item.title"
            />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app color="#ff9a8c" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <!-- <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn> -->
      <!-- <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn> -->
      <v-avatar> <img src="@/assets/hy/logo.jpg" alt="John" /> </v-avatar>&nbsp;
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <!-- <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <!-- <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <v-footer :absolute="!fixed" app color="#ff9a8c" dark>
      <span
        >&copy; {{ new Date().getFullYear() }}
        กลุ่มงานเวชกรรมฟื้นฟู โรงพยาบาลหาดใหญ่ โทร 074-273100 ต่อ 8207
      </span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: true,
      items: [
        {
          icon: 'mdi-face-recognition ',
          title: 'บุคคลทั่วไป',
          to: '/',
        },
        {
          icon: 'mdi-account-settings ',
          title: 'ผู้รับบริการ',
          to: '/patient',
        },
        {
          icon: 'mdi-doctor ',
          title: 'บันทึกการให้บริการ',
          to: '/doctor',
        },
      ],
      miniVariant: false,
      right: false,
      rightDrawer: false,
      title: 'กลุ่มงานเวชกรรมฟื้นฟู โรงพยาบาลหาดใหญ่',
    }
  },
}
</script>
<style scoped>
/* .main-header-color {
  color: #ef4f4f;
} */
</style>
