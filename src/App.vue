<template>
  <div class="container mt-4">
    <new-quote @quoteAdded="addNewQuote"></new-quote>
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
    <app-footer :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-footer>
    <div class="row">
      <div class="col-lg-4 mx-auto">
        <div class="alert alert-danger">
          Click on quotes to delete.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Footer from './components/Footer';
import NewQuote from './components/NewQuote';
import QuoteGrid from './components/QuoteGrid';

export default {
  data() {
    return {
      maxQuotes: 10,
      quotes: [
        { quote: 'Aku sayang kamu', quoteBy: 'Sasa' },
        { quote: 'Aku juga', quoteBy: 'Fadhlu' },
      ],
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
    appFooter: Footer,
  },
};
</script>

<style></style>
