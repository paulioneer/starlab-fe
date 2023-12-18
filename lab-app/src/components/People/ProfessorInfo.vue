<template>
  <v-container>
    Professor Info
    <v-container fluid>
      <v-row class="professor-row">
        <v-col cols="5">
          <v-card>
            <v-img
              src="../../assets/people//sunghyuck.png"
              style="object-fit: fill !important; width: 100%; height: auto%"
            ></v-img>
          </v-card>
          <v-card>
            <v-card-title class="headline">{{
              this.professor.name
            }}</v-card-title>
          </v-card>
        </v-col>
        <v-col>
          <v-card>
            <v-card-text>
              <v-row>
                <!-- <v-col>
                    <v-subheader>Publications</v-subheader>
                    <v-list dense>
                      <v-list-item
                        v-for="(publication, index) in professor.publications"
                        :key="index"
                      >
                        <v-list-item-content>
                          <v-list-item-title style="white-space: pre-wrap">{{
                            publication.title
                          }}</v-list-item-title>
                          <v-list-item-subtitle>{{
                            publication.year
                          }}</v-list-item-subtitle>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list>
                  </v-col> -->

                <v-col>
                  <v-subheader>Careers</v-subheader>
                  <v-list dense>
                    <v-list-item
                      v-for="(career, index) in professor.careers"
                      :key="index"
                    >
                      <v-list-item-content>
                        <v-list-item-title>{{
                          career.title
                        }}</v-list-item-title>
                        <v-list-item-subtitle>{{
                          career.year
                        }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: 'ProfessorInfo',
  props: {
    professor: Object,
  },

  created() {
    console.log(this.professor)
  },
}
</script>

<style></style>
