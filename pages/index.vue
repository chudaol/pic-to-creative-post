<template>
  <v-layout
    row
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm6
      md4
      v-for="(pic, i) in pics" :key="i"
      class="pa-1"
    >
      <photo-post :originalUrl="pic.originalUrl" :creativeUrl="pic.creativeUrl" />
    </v-flex>
  </v-layout>
</template>

<script>
import PhotoPost from '~/components/PhotoPost.vue'
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState(['pics'])
  },
  components: {
    PhotoPost
  }
}
</script>
