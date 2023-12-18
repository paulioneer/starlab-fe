<template>
  <v-app-bar
    color="transparent"
    app
    class="custom-app-bar"
    style="margin-bottom: 0px"
  >
    <v-spacer />
    <!-- 왼쪽에 네비게이션 아이콘 -->

    <!-- 가운데에 제목 -->
    <v-app-bar-title class="custom-title nav-button" @click="toPage('/')">
      S.T.A.R LAB
    </v-app-bar-title>
    <!-- 오른쪽에 메뉴 아이템들 -->
    <v-spacer></v-spacer>
    <!-- 중앙으로 정렬하기 위한 빈 공간 -->
    <v-btn class="nav-button" text @click="toPage('/')"> Home </v-btn>
    <v-btn class="nav-button" text @click="toPage('/people')"> People </v-btn>
    <v-btn class="nav-button" text @click="toPage('/publication')">
      Publication
    </v-btn>
    <v-btn class="nav-button" text> Projects </v-btn>
    <v-spacer />
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    }
  },

  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer
    },

    toPage(page) {
      this.$router.push(page)
    },
  },
}
</script>
<style scoped>
.custom-title {
  margin-inline-start: 8px !important;
}

.custom {
  margin-right: 0px;
}

.nav-button {
  color: white;
}
</style>
