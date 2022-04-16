<template>
  <div>
    <v-parallax height="200" class="section-1" src="./streamers-banner.jpg">
      <div class="minecrafter-section-title text-center mx-2 mt-10">
        De qui
      </div>
      <div class="minecrafter-section-subtitle text-center mb-8 mx-2">
        D'une collaboration de 3 streamers
      </div>
    </v-parallax>
    <div class="d-flex justify-space-around my-12">
      <v-card color="#141414" v-for="(streamer, i) in streamers" :key="i" min-width="350px" min-height="100px">
        <div class="d-flex justify-center">
          <v-avatar width="125px" height="125px" class="ma-4">
            <v-img :src="streamer.imageSrc"></v-img>
          </v-avatar>
        </div>
        <div class="d-flex justify-center">
          <v-btn
            color="blue-grey"
            class="white--text text-center"
            fab
            text
            @click="redirectToTwitch(streamer.twitchUrl)"
          >
            <v-icon color="#9147FF" x-large dark>
              mdi-twitch
            </v-icon>
          </v-btn>
        </div>
        <div class="minecrafter-proposed-by-title-card mb-0.5">{{ streamer.name }}</div>
        <div class="text-h6 mb-4 text-center">{{ streamer.description }}</div>
      </v-card>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ProposedBySection extends Vue {
  get streamers () {
    return [
      {
        name: 'TacxTV',
        imageSrc: './profile/tacx.png',
        description: 'et sa communauté de félins',
        twitchUrl: 'https://www.twitch.tv/tacxtv',
      },
      {
        name: 'Samsaoule',
        imageSrc: './profile/samsaoule.png',
        description: 'et de son pays Homelecia',
        twitchUrl: 'https://www.twitch.tv/samsaouule',
      },
      {
        name: 'Haechi_co',
        imageSrc: './profile/haechi.jpg',
        description: 'et son monde coloré et magique',
        twitchUrl: 'https://www.twitch.tv/haechi_co',
      },
    ]
  }

  redirectToTwitch (url : string) {
    return window.open(url, '_blank')
  }
}
</script>

<style lang="scss">

.minecrafter-proposed-by-title-card {
  font-family: "Minecrafter",serif;
  color: #4F81CF;
  font-size: 30px;
  text-align: center;
}

</style>
