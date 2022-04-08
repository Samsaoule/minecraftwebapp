<template>
  <v-card color="#141414" class="section-2">
    <v-parallax height="200" class="section-1" src="./mods-banner.png">
      <div class="minecrafter-section-title text-center mx-2">
        Mods
      </div>
    </v-parallax>
    <div v-for="(mod, i) in mods" :key="i">
      <div class="d-flex justify-space-between align-center">
        <div v-if="isEven(i)" class="ma-auto">
          <div class="minecrafter-section-subtitle text-center mx-2">
            {{ mod.title }}
          </div>
          <v-card width="625px" class="pa-6 mt-6 objective-description" v-html="mod.description"></v-card>
        </div>
        <v-img class="flex-grow-0" style="width: 50%;" height="435" :src="mod.imageSrc"></v-img>
        <div v-if="!isEven(i)" class="ma-auto">
          <div class="minecrafter-section-subtitle text-center mx-2">
            {{ mod.title }}
          </div>
          <v-card width="625px" class="pa-6 mt-6 objective-description" v-html="mod.description"></v-card>
        </div>
      </div>
    </div>
    <v-divider class="mt-8 mb-6"></v-divider>

    <div class="minecrafter-section-subtitle text-center mx-2">
      Autres mods
    </div>

    <v-slide-group
      v-model="model"
      class="pa-4"
      show-arrows
    >
      <v-slide-item
        v-for="(otherMod, j) in otherMods"
        :key="j"
        :value="otherMod"
      >
        <v-card
          class="ma-4 d-flex align-center"
          height="120"
          width="260"
          :color="isEven(j) ? '#060606' : '#f7f7f7'"
        >
          <div class="text-center ma-auto">
            <div class="text-h6 font-weight-bold" :class="{'black--text': !isEven(j)}">
              {{ otherMod.title }}
            </div>
            <div class="text-body-2 font-italic font-weight-bold" :class="{'black--text': !isEven(j)}">
              {{ otherMod.description }}
            </div>
          </div>
        </v-card>
      </v-slide-item>
    </v-slide-group>

    <v-parallax height="100" class="section-1" src="./mods-banner.png"></v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class ModsSection extends Vue {
  model = null
  get mods () {
    return [
      {
        title: 'Immersive Engineering',
        description: `<div class="text-center"><a href="https://ftb.fandom.com/wiki/Immersive_Engineering">Lien vers le wiki</a></div><br>
        Ce mod ajoute tout une <span class="yellow--text">mécanique d'électricité et de machineries</span> permettant d'industrialiser tout un tas de tâches
        le tout dans une ambiance rétro-futuriste.<br>
        Elles fonctionnent chacunes selon des règles et des voltages bien précis, aussi faudra-il trouver un moyen de générer votre propre électricité !
        Parmis ces systèmes, on peut notamment retrouver des machines pour <span class="yellow--text">augmenter ses rendements en lingots de minerais</span>, des moulins à eau,
        des presses mécaniques...`,
        imageSrc: this.profileSrc('immersive-engineering.png'),
      },
      {
        title: 'Alex\'Mobs',
        description: `<div class="text-center"><a href="https://alexs-mobs-bestiary.fandom.com/wiki/Alex%27s_Mobs_Bestiary_Wiki">Lien vers le wiki</a></div><br>
        Ajoute beaucoup de <span class="green--text">créatures et monstres uniques</span> dans le monde réel, le Nether et l'End.<br>
        De la pieuvre à l'éléphant en passant par des corbeaux, des insectes géants et des gorilles, jamais votre expérience n'aura jamais été aussi <span class="green--text">diversifié</span> !`,
        imageSrc: this.profileSrc('alexmobs.png'),
      },
      {
        title: 'Create',
        description: `<div class="text-center"><a href="https://create.fandom.com/fr/wiki/Wiki_Create">Lien vers le wiki</a></div><br>
        Permet de créer des <span class="brown--text">engins et d'automatiser les processus</span> à l'aide de la puissance de rotation grace à la force mécanique !<br>
        Créez du mouvement dans vos blocs, <span class="brown--text">créez de vrais moulins et autre systèmes pour alimenter de nombreuses machines</span> permettant d'augmenter vos rendements.
        Peut être couplé avec Immersive Engineering.`,
        imageSrc: this.profileSrc('create.png'),
      },
      {
        title: 'Biome O Plenty',
        description: `<div class="text-center"><a href="https://biomesoplenty.fandom.com/wiki/Biomes_O%27_Plenty_Wiki">Lien vers le wiki</a></div><br>
        Ajoute pas moins de <span class="cyan--text">60 nouveaux biomes au monde Minecraft</span>.<br>
        Entre des Alpes, des plages, de grandes forêts de l'Amérique du Nord, des chaines de montagnes et de belles forêts magiques...
        Vous allez être servi !`,
        imageSrc: this.profileSrc('biomeoplenty.webp'),
      },
      {
        title: 'Tinkers Construct',
        description: `<div class="text-center"><a href="https://tinkers-construct.fandom.com/wiki/Tinkers%27_Construct_Wiki">Lien vers le wiki</a></div><br>
        Créez de <span class="orange--text">nouveaux outils et armes puissantes</span> avec Tinkers Construct !<br>
        Fondez vos minerais dans une forge, créez de puissants alliages et combinez des matériaux pour devenir le maitre des outils !`,
        imageSrc: this.profileSrc('tinker.png'),
      },
      {
        title: 'Farmers Delight',
        description: `<div class="text-center"><a href="https://www.minecraft-france.fr/mod-farmers-delight/">Lien vers le wiki</a></div><br>
        Farmer’s Delight est un mod qui <span class="green--text">développe l’agriculture et la cuisine dans Minecraft</span> qui reste assez pauvre à ce jour.
        À l’aide d’une collection d’outils et de postes de travail, vous pourrez améliorer les fondations de vos parcelles de ferme, préparer une myriade de repas copieux,
        et même vous préparer un peu mieux pour l’aventure!`,
        imageSrc: this.profileSrc('farmersdelight.png'),
      },
    ]
  }

  get otherMods () {
    return [
      {
        title: 'Refined Storage',
        description: `Serveurs de stockage d'objets`,
      },
      {
        title: 'Corpse',
        description: `Garde votre stuff à votre mort`,
      },
      {
        title: 'Yungs',
        description: `Nouvelles structures générées`,
      },
      {
        title: 'Dungeon Crawl',
        description: `Nouveaux donjons difficiles`,
      },
      {
        title: 'Redstone Open',
        description: `Redstone sur les murs !`,
      },
      {
        title: 'Voicechat',
        description: `Chat vocal in-game`,
      },
      {
        title: 'Appleskin',
        description: `Détail sur le niveau de faim`,
      },
      {
        title: 'More Minecarts',
        description: `Nouveaux rails et wagons`,
      },
      {
        title: 'Construction Wand',
        description: `Construire grand et vite`,
      },
      {
        title: 'Better Mineshaft',
        description: `Amélioration des mines`,
      },
      {
        title: 'DecorativeBlock',
        description: `Pleins de blocs déco`,
      },
      {
        title: 'Better Dungeon',
        description: `Amélioration des donjons`,
      },
      {
        title: 'Sophisticated Backpacks',
        description: `Sacs à dos`,
      },
    ]
  }

  isEven (n: number) {
    return n % 2 == 0;
  }

  profileSrc (imageName: string) {
    return `./mods/${imageName}`
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
