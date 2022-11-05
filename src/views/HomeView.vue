<template>
  <div class="home">
    <header-section />
    <top-creator />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import TopCreator from "@/components/TopCreator.vue";
import HeaderSection from "@/components/HeaderSection.vue";

@Options({
  components: {
    TopCreator,
    HeaderSection,
  },
})
export default class HomeView extends Vue {}
</script>
