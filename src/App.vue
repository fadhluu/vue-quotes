<template>
  <div class="container mt-4">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <new-quote @quoteAdded="addNewQuote"></new-quote>
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  </div>
</template>

<script>
import Header from './components/Header';
import NewQuote from './components/NewQuote';
import QuoteGrid from './components/QuoteGrid';

export default {
  data() {
    return {
      maxQuotes: 10,
      quotes: ['First Quote', 'Second quote'],
    };
  },
  methods: {
    addNewQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Please delete some quote');
      }
      return this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    },
  },
  components: {
    quoteGrid: QuoteGrid,
    newQuote: NewQuote,
    appHeader: Header,
  },
};
</script>

<style></style>
