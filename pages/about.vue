<template>
  <v-row class="ma-12" justify="end">
    <v-col v-for="(partner, i) in partners" :key="i" cols="4">
      <v-card color="#141414" min-height="100px" width="225px">
        <v-avatar width="150px" height="150px" class="ma-9">
          <v-img :src="partner.imageSrc"></v-img>
        </v-avatar>
      </v-card>
    </v-col>
    <v-spacer></v-spacer>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class About extends Vue {
  get partners () {
    return [
      {
        imageSrc: `${this.profileSrc}haechi.jpg`,
        pseudo: 'Haechi_co',
        quote: 'La pression je ne la subis pas, je la bois',
        socialsUrl: [
          {
            tiktok: 'https://www.tiktok.com/@haechi.co',
          }
        ]
      },
      {
        imageSrc: `${this.profileSrc}haechi.jpg`,
        pseudo: 'Haechi_co',
        quote: 'La pression je ne la subis pas, je la bois',
        socialsUrl: [
          {
            tiktok: 'https://www.tiktok.com/@haechi.co',
          }
        ]
      },
      {
        imageSrc: `${this.profileSrc}haechi.jpg`,
        pseudo: 'Haechi_co',
        quote: 'La pression je ne la subis pas, je la bois',
        socialsUrl: [
          {
            tiktok: 'https://www.tiktok.com/@haechi.co',
          }
        ]
      },
    ]
  }

  get profileSrc () {
    return './profile/'
  }
}
</script>
