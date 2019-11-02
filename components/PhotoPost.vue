<template>
  <v-card>
    <v-img
      class="white--text align-end"
      width="100%"
      :src="original ? originalUrl : creativeUrl"
    >
    </v-img>
    <v-card-actions>
      <v-spacer />
      <v-btn
        @click="toggleOriginal"
        outlined
      >
        {{original ? 'See creative post' : 'See original'}}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
  export default {
    props: ['originalUrl', 'creativeUrl'],
    data () {
      return {
        original: true
      }
    },
    methods: {
      toggleOriginal () {
        this.original = !this.original
      }
    }
  }
</script>
