<template>
  <div class="d-flex justify-center">
    <v-sheet>
      <v-img contain src="./map-valandir.png"/>
    </v-sheet>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import DownloadSection from "~/components/download/DownloadSection.vue";
import RulesSection from "~/components/rules/RulesSection.vue";
@Component({
  components: {RulesSection, DownloadSection}
})
export default class Download extends Vue {

}
</script>
