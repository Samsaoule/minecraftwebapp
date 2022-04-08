<template>
  <v-row justify="center" align="center">
    <v-col>
      <ModsSection></ModsSection>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import ModsSection from "~/components/mods/ModsSection.vue";
@Component({
  components: { ModsSection }
})
export default class Mods extends Vue {

}
</script>
