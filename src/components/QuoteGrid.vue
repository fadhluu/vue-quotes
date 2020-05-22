<template>
  <div class="row">
    <app-quote
      v-for="(quote, index) in quotes"
      @click.native="deleteQuote(index)"
    >
      <div slot="quote">{{ quote.quote }}</div>
      <span slot="quoteBy"> {{ quote.quoteBy }}</span>
    </app-quote>
  </div>
</template>

<script>
import Quote from './Quote';

export default {
  props: ['quotes'],
  components: {
    appQuote: Quote,
  },
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDeleted', index);
    },
  },
};
</script>

<style></style>
