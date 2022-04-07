<template>
  <v-card color="#141414" class="section-2">
    <div class="minecrafter-section-title text-center mx-2">
      Comment
    </div>
    <div class="minecrafter-section-subtitle text-center mb-8 mx-2">
      Suis juste les instructions
    </div>
    <div class="d-flex justify-center">
      <v-btn disabled="true" x-large color="primary" @click="goTo('download')">
        <v-icon class="mr-2">mdi-download</v-icon> A venir
      </v-btn>
    </div>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ButAlsoSection extends Vue {
  goTo (route: string) {
    this.$router.push(`/${route}`)
  }
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
