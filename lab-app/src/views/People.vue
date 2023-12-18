<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <v-container class="content-wrap">
    <!-- Professor -->

    <v-card class="mx-auto p-group">
      <v-toolbar color="black" dark>
        <v-toolbar-title>Professor</v-toolbar-title>
      </v-toolbar>
      <professor-info :professor="professor" />
    </v-card>

    <!-- PhD -->
    <v-card class="mx-auto p-group">
      <v-toolbar color="black" dark>
        <v-toolbar-title>Ph.D Student</v-toolbar-title>
      </v-toolbar>

      <v-container fluid>
        <v-row dense>
          <v-col v-for="card in cards" :key="card.title" cols="4">
            <card-info :card="card" />
          </v-col>
        </v-row>
      </v-container>
    </v-card>
    <!-- MsC -->
    <v-card class="mx-auto p-group">
      <v-toolbar color="black" dark>
        <v-toolbar-title>Master Student</v-toolbar-title>
      </v-toolbar>

      <v-container fluid>
        <v-row dense>
          <v-col v-for="card in cards" :key="card.title" cols="4">
            <card-info :card="card" />
          </v-col>
        </v-row>
      </v-container>
    </v-card>
    <!-- Alumni -->
    <v-card class="mx-auto p-group">
      <v-toolbar color="black" dark>
        <v-toolbar-title>Alumni</v-toolbar-title>
      </v-toolbar>

      <v-container fluid>
        <v-row dense>
          <v-col v-for="card in cards" :key="card.title" cols="4">
            <card-info :card="card" />
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-container>
</template>
<script>
import CardInfo from '../components/People/CardInfo.vue'
import ProfessorInfo from '../components/People/ProfessorInfo.vue'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'People',
  components: {
    CardInfo,
    ProfessorInfo,
  },
  data: () => ({
    professor: {
      name: 'Sunghyuk Park',
      rank: '0',
      src: '../assets/people/sunghyuck.png',
      edu: [
        'B.A. Applied Mathematics, KAIST(2005)',
        'Ph.D Management Engineering, KAIST(2013)',
      ],
      publications: [
        {
          title:
            'Intraoperative Hypotension Prediction Based on Features Automatically Generated Within an Interpretable Deep Learning Model.',
          year: '2023',
        },
        {
          title:
            'Shin, H., Han, I., and Park, S. "A Case Study on the Success and Failure of Yello Mobile.',
          year: '2021',
        },
      ],
      careers: [
        { title: '한국경영정보학회 이사/정회원', year: '2021' },
        { title: '지능정보연구 편집부위원장', year: '2021' },
        { title: 'CEO at Impact AI, Seoul, Korea', year: '2022' },
        { title: 'CTO at Wconcept Korea Seoul', year: '2019' },
        { title: 'Venture Partner at Dunamu & Partners', year: '2018-2019' },
        { title: 'CEO and Founder at Recobell Co., Ltd.', year: '2013-2018' },
        { title: 'CEO at YelloExchange Co., Ltd.', year: '2016-2018' },
        { title: 'Technical Advisor at Ridi', year: '2012' },
      ],
      industry: [
        '아난티 사외이사 (2023~)',
        '효성ITX 사외이사 (2021~)',
        'LG CNS 자문교수 (2021)',
        '와이즈버즈 자문교수(2020)',
        '아이겐코리아 연구자문',
      ],
    },

    cards: [
      {
        name: 'Daesan Oh',
        rank: 3,
        src: '',
        edu: ['B.A. Industrial Engineering, KAIST(2023)'],
        research: [
          'Recommendation System',
          'Artificial Intelligence',
          'Blockchain',
        ],
        link: {},
      },
      {
        name: 'Junkyu Jang',
        rank: 3,
        src: '',
        edu: ['B.A. Applied Mathematics, KAIST(2023)'],
        research: [
          'Recommendation System',
          'Artificial Intelligence',
          'Blockchain',
        ],
        link: {},
      },
      {
        name: 'Kitae Kim',
        rank: 3,
        src: '',
        edu: ['B.A. Civil Engineering, Korea University(2023)'],
        research: [
          'Recommendation System',
          'Artificial Intelligence',
          'Blockchain',
        ],
        link: {},
      },
      {
        name: 'Jungwoo Kim',
        rank: 2,
        src: '../../assets/people/jungwoo.png',
        edu: ['B.A. Business Management, Chungang University(2023)'],
        research: [
          'Recommendation System',
          'Artificial Intelligence',
          'Blockchain',
        ],
        link: {},
      },
      {
        name: 'Yeoseul Yoon',
        rank: 2,
        src: '../../assets/people/yeoseul.png',
        edu: [
          'B.A. Education, Yonsei University (2023)',
          'M.S. Managment Engineering, KAIST (2026)',
        ],
        research: [
          'Artificial Intelligence',
          'Platform Business',
          'Startup business',
        ],
        link: {},
      },
      {
        name: 'Jinwoo Kim',
        rank: 2,
        src: '../../assets/people/jinwoo.png',
        edu: [
          'B.A. Computer Science and Engineering, Sungkyunkwan University (2023)',
        ],
        research: ['Artificial Intelligence', 'Blockchain', 'Entrepreneurship'],
        link: {},
      },
      {
        name: 'Soonjae Kwon',
        rank: 3,
        src: '',
        edu: ['B.A. Chemical Engineering, KAIST(2023)'],
        research: ['Artificial Intelligence', 'Blockchain', 'Entrepreneurship'],
        link: {},
      },
    ],
    loading: false,
    selection: 1,
  }),

  methods: {
    reserve() {
      this.loading = true

      setTimeout(() => (this.loading = false), 2000)
    },
  },
}
</script>
<style scoped>
.v-toolbar__content > .v-toolbar-title {
  margin-inline-start: 25px !important;
}

.v-card-text {
  padding: 0px 1rem !important;
}

.p-group {
  margin-bottom: 40px;
  box-shadow: none !important;
}

.content-wrap {
  padding-right: var(--v-layout-right);
  padding-left: var(--v-layout-left);
  padding-top: var(--v-layout-top);
}
</style>
