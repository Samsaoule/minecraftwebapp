<template>
  <v-row justify="center" align="center">
    <v-col>
      <ObjectivesSection></ObjectivesSection>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import ObjectivesSection from "~/components/objectives/ObjectivesSection.vue";
@Component({
  components: {ObjectivesSection}
})
export default class Objectives extends Vue {

}
</script>
