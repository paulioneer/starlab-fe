<template>
  <div id="main-bg">
    <section id="banner">
      <h1>Welcome to S.T.A.R LAB</h1>
    </section>
    <v-carousel show-arrows="hover" hide-delimiter style="height: 100px">
      <v-carousel-item>
        <div>장준규, 박사과정 CES 논문 Accept</div>
      </v-carousel-item>
      <v-carousel-item>
        <div>장준규, 박사과정 CES 논문 Accept</div>
      </v-carousel-item>
      <v-carousel-item>
        <div>장준규, 박사과정 CES 논문 Accept</div>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script setup></script>

<style scoped>
#main-bg {
  background: linear-gradient(rgba(10, 10, 10, 0.5), rgba(29, 29, 29, 0.5)),
    url(../assets/real_main.jpg);
  /* background-position: 0% 20%; */
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  min-height: 100vh;
}

#banner {
  color: white;
  padding: 20em 0 0 0;
  /* background-color: #0c0c0c; */
  text-align: center;
  position: relative;
}

#banner h1 {
  font-size: 2.5em;
  margin: 0 0 1em 0;
  padding: 0;
  letter-spacing: 2px;
  font-weight: 600;
}

#notice {
  height: 100px;
}
</style>
