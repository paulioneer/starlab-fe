<template>
  <v-card :loading="loading" class="mx-auto my-1" max-width="374">
    <template v-slot:loader="{ isActive }">
      <v-progress-linear
        :active="isActive"
        color="deep-purple"
        height="4"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img fill height="200" :src="getSrc"></v-img>

    <v-card-item>
      <v-card-title>{{ this.card.name }}</v-card-title>
      <v-card-subtitle>
        <span class="me-1">{{ getRank }}</span>
      </v-card-subtitle>
    </v-card-item>

    <v-card-text class="p-card-text">
      <div class="text-subtitle-2">Education</div>
      <div class="text-subtitle-1">
        <div class="edu-item" v-for="item in this.card.edu" :key="item">
          {{ item }}
        </div>
      </div>
    </v-card-text>

    <v-card-text class="p-card-text">
      <div class="text-subtitle-2">Research Interests</div>
      <div class="text-subtitle-1">
        {{ getInterest }}
      </div>
    </v-card-text>

    <v-card-actions></v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: 'CardInfo',
  data: () => ({
    loading: false,
    selection: 1,
  }),

  props: {
    card: Object,
  },

  methods: {
    reserve() {
      this.loading = true
      setTimeout(() => (this.loading = false), 2000)
    },
  },

  computed: {
    getRank: function () {
      if (this.card.rank == 2) {
        return "Master's Student"
      } else {
        return 'Ph.D Student'
      }
    },

    getSrc: function () {
      return this.card.src
        ? new URL(this.card.src, import.meta.url).href
        : new URL('../../assets/people/anonymous.jpg', import.meta.url).href
    },

    getInterest: function () {
      return this.card.research.join(', ')
    },

    getEdu: function () {
      return this.card.edu
    },
  },
}
</script>

<style>
.p-card-text {
  height: 80px !important;
}

.v-card--variant-elevated {
  box-shadow: 0px 5px 1px -1px var(--v-shadow-key-umbra-opacity, rgba(0, 0, 0, 0.2)),
    0px 1px 1px 0px var(--v-shadow-key-penumbra-opacity, rgba(0, 0, 0, 0.14)),
    0px 1px 3px 0px var(--v-shadow-key-penumbra-opacity, rgba(0, 0, 0, 0.12)) !important;
}

.v-img__img--contain {
  object-fit: fill !important;
}

.text-subtitle-1 {
  line-height: 1.2rem !important;
  font-size: 13px !important;
  word-break: keep-all !important;
}
</style>
