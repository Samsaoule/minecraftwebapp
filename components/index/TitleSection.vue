<template>
  <v-card>
    <v-parallax height="700" class="section-1" src="./title-section-bg.png">
      <div class="d-flex justify-center mt-8">
        <v-img class="flex-grow-0" width="250px" contain src="./logo-valandir.png"></v-img>
      </div>
      <div class="minecrafter-title text-center mt-2 mx-2">
        Valandir
      </div>
      <div class="catch-phrase text-center mx-2">
        Venez faire partie de ce monde moddé à nos côtés !
      </div>
    </v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class TitleSection extends Vue {

}
</script>

<style lang="scss">
.section-1 {
  width: 100vw;
  height: 65vh;
}

.minecrafter-title {
  font-family: "Minecrafter",serif;
  font-size: 90px;
  -webkit-text-stroke: 2px #000000;
}

.catch-phrase {
  font-size: 34px ;
  font-weight: 400;
  letter-spacing: 0.0333333333em;
  line-height: 1.25rem;
  font-family: "Roboto", sans-serif;
}
</style>
