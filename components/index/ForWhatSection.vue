<template>
  <v-card color="#141414" class="section-2">
    <div class="minecrafter-section-title text-center mx-2">
      Pourquoi
    </div>
    <div class="minecrafter-section-subtitle text-center mb-8 mx-2">
      Pour nous montrer...
    </div>
    <v-container>
      <div class="d-flex justify-space-around align-center">
        <div class="what-text-section text-center">
          ...de quoi tu es capable <br><span class="cyan--text border-section-text font-weight-bold">toi et ta pioche</span> !
        </div>
        <v-img class="flex-grow-0" width="275px" contain src="./humanpioche.png"></v-img>
      </div>

      <div class="d-flex justify-space-around align-center">
        <v-img class="flex-grow-0" width="400px" contain src="./spider.png"></v-img>
        <div class="what-text-section text-center">
          ...ton courage face à <br><span class="red--text border-section-text font-weight-bold">des ennemis inconnus !</span>
        </div>
      </div>

      <div class="d-flex justify-space-around align-center">
        <div class="what-text-section text-center">
          ...ainsi que ta créativité dans la construction<br><span class="green--text border-section-text font-weight-bold">de maisons ou d’usines !</span>
        </div>
        <v-img class="flex-grow-0" width="400px" contain src="./build.png"></v-img>
      </div>
    </v-container>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ForWhatSection extends Vue {

}
</script>

<style lang="scss">
.section-2 {
  width: 100vw;
}

.minecrafter-section-title {
  font-family: "Minecrafter",serif;
  font-size: 55px;
  -webkit-text-stroke: 2px #000000;
}

.minecrafter-section-subtitle {
  font-family: "Minecrafter",serif;
  font-size: 30px;
  -webkit-text-stroke: 2px #000000;
}

.what-text-section {
  font-size: 35px;
}

.border-section-text {
  -webkit-text-stroke: 2px #000000;
}

.bg-color-section {
  background-color: black;
}
</style>
