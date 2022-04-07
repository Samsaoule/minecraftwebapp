<template>
  <v-card color="#141414" class="section-2">
    <v-parallax height="200" class="section-1" src="./objectives-banner.png">
      <div class="minecrafter-section-title text-center mx-2">
        Objectifs
      </div>
      <div class="text-h6 text-center mb-8 mx-2">
        Bien evidemment, on ne vous lâche pas comme ça dans la nature...
      </div>
    </v-parallax>
    <v-container>
      <div class="mt-16" v-for="(objective, i) in objectives" :key="i">
        <div class="minecrafter-section-subtitle text-center mx-2">
          {{ objective.title }}
        </div>
        <div class="d-flex justify-space-around align-center">
          <v-card v-if="isEven(i)" width="625px" class="pa-6 objective-description" v-html="objective.description"></v-card>
          <v-img class="flex-grow-0" width="350px" height="350px" contain :src="objective.imageSrc"></v-img>
          <v-card v-if="!isEven(i)" width="625px" class="pa-6 objective-description" v-html="objective.description"></v-card>
        </div>
        <v-divider v-if="objectives.length - 1 !== i" class="mt-12"></v-divider>
      </div>
    </v-container>
    <v-parallax height="100" class="section-1" src="./objectives-banner.png"></v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ObjectivesSection extends Vue {
  get objectives () {
    return [
      {
        title: 'Developpons l\'ile tous ensemble',
        description: `Qui sommes-nous ? De valeureuses personnes venues de tous horizons pour explorer et s'installer sur une île aux milles couleurs ! <br>
        Vous devrez vous installer pour permettre à vous et à d'autres colons de prospérer.<br><span class="cyan--text">Développez l'île et son économie !</span> Ce sera crucial pour garantir votre survie. 😈`,
        imageSrc: './objective-develop.png',
      },
      {
        title: 'Explorer et combattre',
        description: `Un village a été établi par les premiers colons, entouré de grands murs en pierre car ce monde est certes très intéressant, il n'en reste pas moins
          hostile.<br>
          En effet, certaines zones renferme des <span class="red--text">monstres divers et variés</span>, des <span class="red--text">donjons</span> gardés par de terribles
          ennemis à abattre mais également certaines zones reculées où
          <span class="red--text">explorer vous en apprendra plus</span> sur ce qu'il est arrivé aux premiers voyageurs. 🏹`,
        imageSrc: './objective-monsters.png',
      },
      {
        title: 'Accumuler un max de ressources',
        description: `Un portail a été découvert sur l'île. Son utilité ? Permettre de <span class="green--text">rejoindre une dimension parralèle pour aller y piller toutes les ressources</span> !<br>
        Faites-vous plaisir, parce que sa particularité, c'est de se régénérer à intervalles réguliers. 😇`,
        imageSrc: './objective-resources.png',
      },
      {
        title: 'De nombreux events',
        description: `Un <span class="orange--text">concours de construction</span>, des <span class="orange--text">combats d'arènes</span>, une <span class="orange--text">chasse aux oeufs de Pâques</span>... De nombreux évènements vous attendent dans ce monde.<br>
        Et pour les grands gagnants, <span class="orange--text">de belles récompenses</span> ! 🎉`,
        imageSrc: './objective-event.webp',
      },
    ]
  }

  isEven (n: number) {
    return n % 2 == 0;
  }
}
</script>

<style lang="scss">
.objective-description {
  font-size: 1.075rem;
  font-weight: 500;
  letter-spacing: .009375em;
}
</style>
