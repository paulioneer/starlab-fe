<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <v-footer color="black">
    <v-spacer></v-spacer>
    <div class="footer-content">
      <v-col>STAR LAB</v-col>
      <v-col>Room S293 SUPEX KAIST College of Business</v-col>
      <v-col>85 Hoegiro Dongdaemun-gu Seoul Korea 02455</v-col>
      <div class="v-col">psh@kaist.ac.kr</div>
    </div>
    <v-spacer></v-spacer>
    <div class="footer-content">
      <div class="v-col">Sites</div>
      <div class="v-col">Family</div>
      <div class="v-col">Publication</div>
      <div class="v-col">Researcch</div>
      <div class="v-col">Lecture</div>
      <div class="v-col">Contact</div>
    </div>
    <v-spacer></v-spacer>
    <div class="footer-content">
      <div class="v-col">LINKS</div>
      <div class="v-col">KCB</div>
      <div class="v-col">KAIST</div>
      <div class="v-col">Youtube</div>
      <div class="v-col">Facebook</div>
    </div>
    <v-spacer></v-spacer>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin'],
  }),
}
</script>

<style></style>
