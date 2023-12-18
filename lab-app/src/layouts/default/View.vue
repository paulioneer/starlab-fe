<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <v-main id="custom-main">
    <router-view />
  </v-main>
</template>

<script setup>
//
</script>
<style>
.v-main {
  padding-top: 0px !important;
  padding-left: 0px !important;
  padding-right: 0px !important;
  --v-layout-left: calc((100% - 1544px) / 2) !important;
  --v-layout-right: calc((100% - 1544px) / 2) !important;
}


</style>
