<template>
  <v-row justify="center" align="center">
    <v-col>
      <TitleSection></TitleSection>
      <ForWhatSection class="py-8"></ForWhatSection>
      <ProposedBySection></ProposedBySection>
      <ButAlsoSection></ButAlsoSection>
      <HowSection class="py-8"></HowSection>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import TitleSection from "~/components/index/TitleSection.vue";
import ForWhatSection from "~/components/index/ForWhatSection.vue";
import ButAlsoSection from "~/components/index/ButAlsoSection.vue";
import HowSection from "~/components/index/HowSection.vue";
import ProposedBySection from "~/components/index/ProposedBySection.vue";
@Component({
  components: {ProposedBySection, HowSection, ButAlsoSection, ForWhatSection, TitleSection}
})
export default class Index extends Vue {

}
</script>
