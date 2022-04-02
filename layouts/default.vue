<template>
  <v-app dark>
    <v-main>
      <v-card
        color="23272A"
        class="mx-auto overflow-hidden"
      >
        <v-app-bar
          color="343434"
          dark
        >
          <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

          <v-tabs align-with-title>
            <v-tab @click="goTo('')">
              <v-icon class="mr-2">mdi-home</v-icon> Accueil
            </v-tab>
            <v-tab @click="goTo('mods')">
              <v-icon class="mr-2">mdi-playlist-star</v-icon> Mods
            </v-tab>
            <v-tab @click="goTo('about')">
              <v-icon class="mr-2">mdi-information-outline</v-icon> À propos
            </v-tab>
          </v-tabs>
          <v-spacer></v-spacer>
          <v-btn
            color="blue-grey"
            class="mx-4 white--text"
            fab
            text
          >
            <v-icon color="#738ADB" large dark>
              mdi-discord
            </v-icon>
          </v-btn>
          <v-btn color="primary" @click="goTo('download')">
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
              <v-list-item @click="goTo('')">
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Accueil</v-list-item-title>
              </v-list-item>
              <v-list-item @click="goTo('mods')">
                <v-list-item-icon>
                  <v-icon>mdi-playlist-star</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Mods</v-list-item-title>
              </v-list-item>
              <v-list-item @click="goTo('about')">
                <v-list-item-icon>
                  <v-icon>mdi-information-outline</v-icon>
                </v-list-item-icon>
                <v-list-item-title>À propos</v-list-item-title>
              </v-list-item>
              <v-list-item @click="goTo('download')">
                <v-list-item-icon>
                  <v-icon>mdi-download</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Télécharger</v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
        <Nuxt />
      </v-card>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Default extends Vue {
  drawer = false
  group = null

  goTo (route: string) {
    this.$router.push(`/${route}`)
  }

}
</script>
