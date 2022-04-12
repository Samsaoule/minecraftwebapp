<template>
  <v-row justify="center" align="center">
    <v-col>
      <DownloadSection></DownloadSection>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import DownloadSection from "~/components/download/DownloadSection.vue";
@Component({
  components: {DownloadSection}
})
export default class Download extends Vue {

}
</script>
