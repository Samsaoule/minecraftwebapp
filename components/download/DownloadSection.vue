<template>
  <v-card color="#141414" class="section-2">
    <v-parallax height="200" class="section-1" src="./download-banner.png">
      <div class="minecrafter-section-title text-center mx-2">
        Telechargement
      </div>
    </v-parallax>

    <div class="my-8">
      <div class="minecrafter-section-subtitle text-center mx-2">
        Ressources
      </div>
      <div class="d-flex justify-center">
        <v-checkbox
          v-model="rulesReaded"
          label="J'ai bien pris connaissance des règles"
        ></v-checkbox>
      </div>
      <div class="d-flex justify-center">
        <v-btn :disabled="!rulesReaded" class="mx-4" x-large color="primary" @click="downloadLauncher">
          <v-icon class="mr-2">mdi-download</v-icon> Launcher
        </v-btn>
        <v-btn class="mx-4" x-large color="primary" @click="downloadJava">
          <v-icon class="mr-2">mdi-download</v-icon> Java
        </v-btn>
      </div>
    </div>

    <v-divider></v-divider>

    <v-container class="mt-5">
      <div class="minecrafter-section-subtitle text-center mx-2 mb-4">
        Comment jouer
      </div>
      <div class="mx-16 my-6" v-for="(article, i) in articles" :key="i">
        <v-expansion-panels accordion>
          <v-expansion-panel>
            <v-expansion-panel-header class="minecrafter-expansion-panel">{{ article.title }}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-divider class="mb-2"></v-divider>
              <div class="mt-2">
                <NuxtContent :document="article.contentPage"></NuxtContent>
              </div>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </div>
    </v-container>

    <v-parallax height="100" class="section-1" src="./download-banner.png"></v-parallax>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class DownloadSection extends Vue {

  launcherArticleContent = {}
  teamArticleContent = {}
  microArticleContent = {}
  rulesReaded = false

  async mounted () {
    await this.getLauncherArticle()
    await this.getTeamArticle()
    await this.getMicroArticle()
  }

  async getLauncherArticle () {
    this.launcherArticleContent = await this.$content('articles/launcher').fetch()
  }
  async getTeamArticle () {
    this.teamArticleContent = await this.$content('articles/team').fetch()
  }
  async getMicroArticle () {
    this.microArticleContent = await this.$content('articles/micro').fetch()
  }

  downloadLauncher () {
    window.open('https://valandirmc.s3.fr-par.scw.cloud/launcher-bootstrap-1.0.2.jar')
  }

  downloadJava () {
    window.open('https://download.oracle.com/java/17/latest/jdk-17_windows-x64_bin.exe')
  }

  get articles () {
    return [
      {
        title: 'Installation et lancement',
        contentPage : this.launcherArticleContent,
      },
      {
        title: 'Creer sa team et reserver ses terres',
        contentPage : this.teamArticleContent,
      },
      {
        title: 'Configuration micro ingame',
        contentPage : this.microArticleContent,
      },
    ]
  }

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
