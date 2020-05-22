<template>
  <div class="row">
    <div class="col-12 mx-auto">
      <form>
        <div class="form-group">
          <h2>New Quote</h2>
          <textarea
            class="form-control"
            rows="3"
            v-model="quote.quote"
          ></textarea>
        </div>
        <div class="form-group">
          <label for="quoteBy">Author</label>
          <input
            type="text"
            class="form-control"
            id="quoteBy"
            v-model="quote.quoteBy"
          />
        </div>
        <div class="form-group text-center">
          <button class="btn btn-primary" @click.prevent="createNewQuote">
            Add Quote
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quote: {
        quote: '',
        quoteBy: '',
      },
    };
  },
  methods: {
    createNewQuote() {
      if (this.quote.quote === '') {
        return alert("Quote can't be empty");
      } else if (this.quote.quoteBy === '') {
        return alert("Author can't be empty");
      }
      this.$emit('quoteAdded', this.quote);
      this.quote = { quote: '', quoteBy: '' };
      return true;
    },
  },
};
</script>

<style></style>
