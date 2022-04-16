<template>
  <v-app dark>
    <v-main>
      <v-card
        v-if="!$vuetify.breakpoint.smAndDown"
        color="23272A"
        class="mx-auto overflow-hidden"
      >
        <v-app-bar
          color="#161616"
          dark
        >
          <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

          <v-tabs align-with-title :value="$route.name">
            <v-tab to="/" value="" nuxt>
              <v-icon class="mr-2">mdi-home</v-icon> Accueil
            </v-tab>
            <v-tab to="/map" value="map" nuxt>
              <v-icon class="mr-2">mdi-map</v-icon> Carte
            </v-tab>
            <v-tab to="/rules" value="rules" nuxt>
              <v-icon class="mr-2">mdi-ruler</v-icon> Règles
            </v-tab>
            <v-tab to="/objectives" value="objectives" nuxt>
              <v-icon class="mr-2">mdi-flag</v-icon> Objectifs
            </v-tab>
            <v-tab to="/mods" value="mods" nuxt>
              <v-icon class="mr-2">mdi-playlist-star</v-icon> Mods
            </v-tab>
            <v-tab to="/about" value="about" nuxt>
              <v-icon class="mr-2">mdi-information-outline</v-icon> À propos
            </v-tab>
          </v-tabs>
          <v-spacer></v-spacer>
          <v-btn
            color="blue-grey"
            class="mx-4 white--text"
            fab
            text
            @click="redirectDiscord"
          >
            <v-icon color="#738ADB" large dark>
              mdi-discord
            </v-icon>
          </v-btn>
          <v-btn color="primary" @click="goToDownload">
            <v-icon class="mr-2">mdi-download</v-icon> Télécharger le launcher
          </v-btn>
        </v-app-bar>

        <v-navigation-drawer
          v-model="drawer"
          absolute
          temporary
        >
          <v-list
            nav
            dense
          >
            <v-list-item-group
              v-model="group"
              active-class="primary--text text--accent-4"
            >
              <v-list-item to="/" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Accueil</v-list-item-title>
              </v-list-item>
              <v-list-item to="map" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-map</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Carte</v-list-item-title>
              </v-list-item>
              <v-list-item to="rules" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-ruler</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Règles</v-list-item-title>
              </v-list-item>
              <v-list-item to="objectives" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-flag</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Objectifs</v-list-item-title>
              </v-list-item>
              <v-list-item to="mods" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-playlist-star</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Mods</v-list-item-title>
              </v-list-item>
              <v-list-item to="about" nuxt>
                <v-list-item-icon>
                  <v-icon>mdi-information-outline</v-icon>
                </v-list-item-icon>
                <v-list-item-title>À propos</v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
        <Nuxt />
      </v-card>
      <v-card
        v-else
        color="23272A"
        class="mx-auto overflow-hidden fill-height d-flex align-center justify-center"
      >
        <div class="text-center">
          🚧 Mode mobile en cours de construction 🚧 <br> Allez sur PC pour profiter du site
        </div>
      </v-card>
    </v-main>
    <v-footer
      dark
      padless
    >
      <v-card
        class="flex"
        flat
        tile
      >
        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} — <strong>Valandir</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Default extends Vue {
  drawer = false
  group = null
  activate = true

  goToDownload () {
    this.$router.push('download')
  }

  redirectDiscord () {
    window.open('https://discord.gg/hGjxxRcG6Y', '_blank')
  }
}
</script>
