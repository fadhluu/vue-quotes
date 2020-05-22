<template>
  <div class="row">
    <div class="col-12 mx-auto">
      <form>
        <h2>New Quote</h2>
        <div class="form-group">
          <textarea class="form-control" rows="3" v-model="quote"></textarea>
        </div>
        <div class="form-group">
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
      quote: '',
    };
  },
  methods: {
    createNewQuote() {
      if (this.quote === '') {
        return alert("Quote can't be empty");
      }
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
      return true;
    },
  },
};
</script>

<style></style>
