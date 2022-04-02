<template>
  <v-row justify="center" align="center">
    <v-col>
      <TitleSection></TitleSection>
      <ForWhatSection></ForWhatSection>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import TitleSection from "~/components/index/TitleSection.vue";
import ForWhatSection from "~/components/index/ForWhatSection.vue";
@Component({
  components: {ForWhatSection, TitleSection}
})
export default class Index extends Vue {

}
</script>
