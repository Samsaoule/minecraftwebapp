<template>
  <v-card>
    <v-parallax height="800" src="./nightbg.png">
      <div class="minecrafter-section-title text-center mx-2 mb-12">
        Mais aussi
      </div>
      <div class="d-flex justify-space-around mt-8">
        <v-card min-width="250px" min-height="100px">
          <div class="minecrafter-butalso-title-card mt-6">PLEINS</div>
          <div class="minecrafter-butalso-subtitle-card mb-8">de mods actifs</div>
        </v-card>

        <v-card min-width="250px" min-height="100px">
          <div class="minecrafter-butalso-title-card mt-6">2</div>
          <div class="minecrafter-butalso-subtitle-card mb-8">maps uniques</div>
        </v-card>

        <v-card min-width="250px" min-height="100px">
          <div class="minecrafter-butalso-title-card mt-6">Events</div>
          <div class="minecrafter-butalso-subtitle-card mb-8">a la pelle</div>
        </v-card>
      </div>
    </v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ButAlsoSection extends Vue {

}
</script>

<style lang="scss">

.minecrafter-butalso-title-card {
  font-family: "Minecrafter",serif;
  color: #4F81CF;
  font-size: 50px;
  text-align: center;
}
.minecrafter-butalso-subtitle-card {
  font-family: "Minecrafter",serif;
  font-size: 20px;
  text-align: center;
}

</style>
