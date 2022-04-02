<template>
  <div>
    <v-card class="section-2">
      <div class="minecrafter-subtitle text-center my-8 mx-2">
        Pourquoi
      </div>
      <v-container class="mx-12">
        <div class="d-flex justify-end">
          <v-img class="flex-grow-0" contain src="./zombie.webp"></v-img>
        </div>
      </v-container>
    </v-card>
  </div>
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
  height: 65vh;
}

.minecrafter-subtitle {
  font-family: "Minecrafter",serif;
  font-size: 35px;
  -webkit-text-stroke: 2px #000000;
}
</style>
