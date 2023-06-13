<script setup>
import HeaderNavComponent from '@/components/HeaderNavComponent.vue'
import CardsContentComponent from '@/components/CardsContentComponent.vue'
import ClientsComponent from '@/components/ClientsComponent.vue'
import DetailDesignComponent from '@/components/DetailDesignComponent.vue'
import TextComponent from '@/components/TextComponent.vue'
</script>

<template>
  <header>
    <HeaderNavComponent />
    <div class="header-content">
      <TextComponent class="header-submission" />
      <ClientsComponent class="header-clients" />
      <CalculatorComponent class="header-calculator" />
    </div>
  </header>
  <DetailDesignComponent />
  <CardsContentComponent />
</template>

<style scoped>
header {
  background: linear-gradient(
    293.29deg,
    #0a2756 1.86%,
    #1f1f1f 31.03%,
    #1f1f1f 53.19%,
    #1f1f1f 77.76%,
    #0a2756 107.16%
  );
}

@media (max-width: 1770px) {
  header {
    padding-left: 60px;
    padding-right: 60px;
  }
}

@media (max-width: 1085px) {
  header {
    padding-left: 83px;
    padding-right: 83px;
  }
}

.header-content {
  display: grid;
  grid-template-areas:
    'submission gallery'
    'clients gallery';
  grid-template-columns: 1fr 1fr;
  column-gap: 49px;
  max-width: 1170px;
  margin: 0 auto;
}

.header-submission {
  grid-area: submission;
}

.header-clients {
  grid-area: clients;
}

.header-calculator {
  grid-area: gallery;
  height: 100%;
  width: 100%;
}

.header-left {
  padding-right: 49px;
}

@media (max-width: 1085px) {
  .header-content {
    grid-template-areas:
      'submission'
      'gallery'
      'clients';
    row-gap: 20px;
    grid-template-columns: 1fr;
  }

  .header-left {
    padding: 0;
  }
}
</style>
