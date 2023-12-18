<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <v-container>
    <v-row>
      <v-col>
        <v-card>
          <v-img
            :src="professor.image"
            alt="Professor Image"
            class="white--text align-end"
          >
            <v-container>
              <v-row>
                <v-col>
                  <v-btn icon @click="goBack">
                    <v-icon>mdi-arrow-left</v-icon>
                  </v-btn>
                </v-col>
              </v-row>
            </v-container>
          </v-img>

          <v-card-title class="headline">{{ professor.name }}</v-card-title>

          <v-card-subtitle>{{ professor.position }}</v-card-subtitle>

          <v-card-text>
            <v-row>
              <v-col>
                <v-subheader>Publications</v-subheader>
                <v-list dense>
                  <v-list-item
                    v-for="(publication, index) in professor.publications"
                    :key="index"
                  >
                    <v-list-item-content>
                      <v-list-item-title>{{
                        publication.title
                      }}</v-list-item-title>
                      <v-list-item-subtitle>{{
                        publication.year
                      }}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-col>

              <v-col>
                <v-subheader>Careers</v-subheader>
                <v-list dense>
                  <v-list-item
                    v-for="(career, index) in professor.careers"
                    :key="index"
                  >
                    <v-list-item-content>
                      <v-list-item-title>{{ career.title }}</v-list-item-title>
                      <v-list-item-subtitle>{{
                        career.year
                      }}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-col>
            </v-row>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-actions>
            <v-btn @click="showGreetings">Show Greetings</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>

    <v-dialog v-model="greetingsDialog" max-width="500">
      <v-card>
        <v-card-title class="headline"
          >Greetings from {{ professor.name }}</v-card-title
        >
        <v-card-text>{{ professor.greetings }}</v-card-text>
        <v-card-actions>
          <v-btn @click="closeGreetingsDialog">Close</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>

  <!-- <v-container>
    <v-container fluid>
      <v-row dense>
        <v-col cols="6">
          <v-avatar size="150">
            <v-img
              src="../assets/people/sunghyuck.png"
              alt="Image"
              class="rounded-image"
            ></v-img>
          </v-avatar>

          <v-chip variant="outlined"> Chip </v-chip>
        </v-col>
        <v-col cols="6"> 정보 </v-col>
      </v-row>
    </v-container>
  </v-container> -->
</template>

<script>
export default {
  data() {
    return {
      professor: {
        name: 'Prof. John Doe',
        position: 'Associate Professor',
        image: 'https://placekitten.com/600/300', // Replace with actual image URL
        publications: [
          { title: 'Publication 1', year: 2022 },
          { title: 'Publication 2', year: 2021 },
        ],
        careers: [
          { title: 'Career 1', year: 2010 },
          { title: 'Career 2', year: 2015 },
        ],
        greetings:
          'Hello, welcome to my profile! Feel free to explore the information.',
      },
      greetingsDialog: false,
    }
  },
  methods: {
    showGreetings() {
      this.greetingsDialog = true
    },
    closeGreetingsDialog() {
      this.greetingsDialog = false
    },
    goBack() {
      this.$router.go(-1) // Assuming you're using Vue Router
    },
  },
}
</script>

<style>
.diagonal-container {
  position: relative;
  width: 100%;
  height: 400px; /* 원하는 높이로 조정하세요. */
  overflow: hidden;
}

.diagonal-left,
.diagonal-right {
  position: absolute;
  height: 100%;
  width: 50%;
  transition: transform 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #007bff; /* 왼쪽 부분 배경색 */
  color: #fff; /* 글자 색상 */
}
</style>
