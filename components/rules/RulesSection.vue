<template>
  <v-card color="#141414" class="section-2">
    <v-parallax height="200" class="section-1" src="./rules-banner.jpg">
      <div class="minecrafter-section-title text-center mx-2">
        Regles
      </div>
    </v-parallax>

    <div class="minecrafter-section-subtitle text-center mx-2 my-4">
      General
    </div>

    <v-container class="d-flex justify-center my-4">
      <v-list
        width="600px"
        rounded
        two-line
        subheader
      >
        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Respect</v-list-item-title>
            Le respect et la tolérance envers chaque joueur est primordiale.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Politesse</v-list-item-title>
            La politesse est de mise pour que l'expérience de chacun soit la meilleure possible que ce soit en jeu ou au sein du Discord.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Pas de discrimination</v-list-item-title>
            Toutes remarques ou symbole à caractère raciste, homophobe, sexiste, apologie du terrorisme sont interdites.
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-container>

    <v-divider></v-divider>

    <div class="minecrafter-section-subtitle text-center mx-2 my-4">
      Minecraft
    </div>

    <v-container class="d-flex justify-center my-4">
      <v-list
        width="600px"
        rounded
        two-line
        subheader
      >
        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Construction</v-list-item-title>
            Tout comme la planète, la map de build (map principale où vous construisez) doit être préservée. Vous avez carte blanche sur vos constructions, cependant essayez de garder la nature aussi naturelle que possible (ex. les arbres ne volent pas, soyez donc rigoureux, enlevez-les).
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Claims</v-list-item-title>
            Pour plus de sûreté, vous disposez de 25 claims que vous pouvez utiliser à titre personnel ou cumuler en team. Il est interdit d’entourer d’autres joueurs avec les claims.
            Vous devez également supprimer vos claims si vous partez de votre équipe ou changez de team.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Demande de unclaim</v-list-item-title>
            Les chemins de fer, les routes et les bâtiments du serveur sont claims. Toutefois, si un claim route pose problème pour votre construction personnelle, vous pouvez faire une demande de unclaim à un administrateur ou support pour que la zone puisse être débloquée. (ATTENTION : les bâtiments ne seront pas acceptés)
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Map de farm</v-list-item-title>
            Il est inutile de construire dans la map de farm des constructions durables, la map est éphémère et sera donc régénérée dans son entièreté de façon régulière. Tout est permis sur cette map, vous pouvez détruire / miner ce que vous voulez.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">PVP</v-list-item-title>
            Le PVP est autorisé, cependant veillez à ne pas harceler les joueurs. Si vous êtes victime ou que vous vous sentez concerné par ce genre de comportement, n’hésitez pas à en faire part au support. Ceci sera traité dans les plus brefs délais.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Triche</v-list-item-title>
            Toute forme de triche telle quelle soit (Usebug, plugins...) est formellement interdite.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Streamhack</v-list-item-title>
            Le streamhack est interdit chez tous les streamers tels qu'ils soient sur le serveur.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
              <v-list-item-title class="text-h5 font-weight-bold">Fermes à mobs</v-list-item-title>
            Il est formellement interdit de faire des fermes à mobs sur la map de build.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Villageois et animaux</v-list-item-title>
            Il est formellement interdit de ramener des villageois et animaux de la capitale et du village de PNJ de la map de build chez soi. Les villageois trouvés sur la map de farm sont cependant autorisés.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Portails</v-list-item-title>
            Il est formellement interdit de craft les blocs de portail du mod Cosmos.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Commandes</v-list-item-title>
            Il est formellement interdit d'utiliser quelconque commande que ce soit qui n'est pas cité dans la documentation.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Donjons</v-list-item-title>
            Vous devez parcourir les donjons de manière normale et ne pas utiliser quelconque manière de sauter des étapes du donjon.
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-container>

    <v-divider></v-divider>

    <div class="minecrafter-section-subtitle text-center mx-2 my-4">
      Conclusion
    </div>

    <v-container class="d-flex justify-center my-4">
      <v-list
        width="600px"
        rounded
        two-line
        subheader
      >
        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Sanctions</v-list-item-title>
            Tout dépassement ou infraction à ces règles peut entraîner une sanction allant de la réprimande au bannissement du jeu et du Discord selon la communauté.
          </v-list-item-content>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon class="my-auto">
            <v-icon color="pink">mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-h5 font-weight-bold">Mise au point</v-list-item-title>
            Les règles et sanctions peuvent changer. Les joueurs se doivent de se mettre au courant de chaque changement.
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-container>


    <v-parallax height="100" class="section-1" src="./rules-banner.jpg"></v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class RulesSection extends Vue {

}
</script>

<style lang="scss">
  .minecrafter-expansion-panel {
    font-family: "Minecrafter",serif;
    font-size: 20px;
    margin-top: 5px;
    -webkit-text-stroke: 1px #000000;
  }
</style>
