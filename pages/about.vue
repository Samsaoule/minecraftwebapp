<template>
  <div>
    <v-parallax height="200" class="section-1" src="/about-banner.png">
      <div class="minecrafter-section-title text-center mx-2">
        A propos
      </div>
    </v-parallax>
    <v-row class="mt-6 mb-6" justify="center">
      <v-col v-for="(partner, i) in partners" :key="i" cols="4">
        <v-card color="#141414" min-width="350px" min-height="100px">
          <div class="d-flex justify-center">
            <v-avatar width="125px" height="125px" class="ma-4">
              <v-img :src="partner.imageSrc"></v-img>
            </v-avatar>
          </div>
          <div class="d-flex justify-center">
            <v-btn
              v-if="partner.socialsUrl.twitch"
              color="blue-grey"
              class="white--text text-center"
              fab
              text
              @click="redirectTo(partner.socialsUrl.twitch)"
            >
              <v-icon color="#9147FF" x-large dark>
                mdi-twitch
              </v-icon>
            </v-btn>
            <v-btn
              v-if="partner.socialsUrl.tiktok"
              color="blue-grey"
              class="white--text text-center"
              fab
              text
              @click="redirectTo(partner.socialsUrl.tiktok)"
            >
              <v-img class="ml-2 mb-1" contain width="45" height="45" src="./tiktok-logo.svg"></v-img>
            </v-btn>
            <v-btn
              v-if="partner.socialsUrl.discord"
              color="blue-grey"
              class="white--text text-center"
              fab
              text
              @click="redirectTo(partner.socialsUrl.discord)"
            >
              <v-icon color="#738ADB" x-large dark>
                mdi-discord
              </v-icon>
            </v-btn>
            <v-btn
              v-if="partner.socialsUrl.insta"
              color="blue-grey"
              class="white--text text-center"
              fab
              text
              @click="redirectTo(partner.socialsUrl.insta)"
            >
              <v-icon color="#C32AA3" x-large dark>
                mdi-instagram
              </v-icon>
            </v-btn>
          </div>
          <div class="minecrafter-proposed-by-title-card mb-0.5">{{ partner.name }}</div>
          <div class="text-h6 pb-6 text-center">{{ partner.quote }}</div>
        </v-card>
      </v-col>
    </v-row>
    <v-parallax height="100" class="section-1" src="/about-banner.png"></v-parallax>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class About extends Vue {
  get partners () {
    return [
      {
        imageSrc: `${this.profileSrc}tacx.png`,
        name: 'TacxTV',
        quote: 'Coucou ! Je suis là ! Viens manger mes fesses !',
        socialsUrl: {
          twitch: 'https://www.twitch.tv/tacxtv',
          tiktok: 'https://www.tiktok.com/@tacxtv',
          discord: 'https://discord.gg/NURBhQhY3f',
          insta: 'https://www.instagram.com/tacxtv/',
        }
      },
      {
        imageSrc: `${this.profileSrc}samsaoule.png`,
        name: 'Samsaouule',
        quote: 'Grosse ambiance de fête dans son cul !',
        socialsUrl: {
          twitch: 'https://www.twitch.tv/samsaouule',
          tiktok: 'https://www.tiktok.com/@samsaaoule',
          discord: 'https://discord.gg/SYRs7mxqK4',
          insta: 'https://www.instagram.com/samsaouule/',
        },
      },
      {
        imageSrc: `${this.profileSrc}haechi.jpg`,
        name: 'Haechi_co',
        quote: 'La pression je ne la subis pas, je la bois !',
        socialsUrl: {
          twitch: 'https://www.twitch.tv/haechi_co',
          tiktok: 'https://www.tiktok.com/@haechi.co',
          discord: 'https://discord.gg/ZsZ4cY58mn',
          insta: 'https://www.instagram.com/haechi.co/',
        },
      },
      {
        imageSrc: `${this.profileSrc}tarpin.png`,
        name: 'Tarpin',
        quote: 'Toujours rester concentré',
        socialsUrl: {},
      },
      {
        imageSrc: `${this.profileSrc}sadako.png`,
        name: 'Sadako Kohaku',
        quote: 'Gloire à la grande déesse Haechi !',
        socialsUrl: {},
      },
      {
        imageSrc: `${this.profileSrc}kazimor.png`,
        name: 'Kazimor',
        quote: 'Euuuh xD',
        socialsUrl: {},
      },
      {
        imageSrc: `${this.profileSrc}pazuzu.png`,
        name: 'Pazuzu',
        quote: 'On ne nait pas Homme, on le devient',
        socialsUrl: {},
      },
    ]
  }

  redirectTo (url : string) {
    return window.open(url, '_blank')
  }

  get profileSrc () {
    return './profile/'
  }
}
</script>
