<template>
  <v-row justify="center" align="center">
    <v-col>
      <RulesSection></RulesSection>
    </v-col>
  </v-row>
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
