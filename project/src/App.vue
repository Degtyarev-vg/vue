<template>
  <div class="container">
    <appHeader></appHeader>
    <appNewQuote></appNewQuote>
    <appQuoteGrid></appQuoteGrid>
  </div>
</template>

<script>
	import QuoteGrid from './components/QuoteGrid.vue';
	import NewQuote from './components/NewQuote.vue';
	import Header from './components/Header.vue';

  export default {
		components: {
			appQuoteGrid: QuoteGrid,
			appNewQuote: NewQuote,
			appHeader: Header
		}
  }
</script>

<style lang="scss">

</style>
