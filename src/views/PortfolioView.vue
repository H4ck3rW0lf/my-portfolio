<template>
  <div>
    <h1>Portfolio</h1>
    <PortfolioList />
  </div>
</template>

<script>
import PortfolioList from '@/components/PortfolioList.vue';

export default {
  name: 'PortfolioView',
  components: {
    PortfolioList
  }
};
</script>

<style scoped>
h1 {
  text-align: center;
}
</style>