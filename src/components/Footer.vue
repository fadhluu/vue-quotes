<template>
  <div class="row mb-4">
    <div class="col-12">
      <h3>Quotes:</h3>
      <div class="progress" style="height: 30px">
        <div
          class="progress-bar"
          role="progressbar"
          :style="{ width: (quoteCount / maxQuotes) * 100 + '%' }"
          aria-valuenow="25"
          aria-valuemin="0"
          aria-valuemax="100"
        >
          {{ quoteCount }}/{{ maxQuotes }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['quoteCount', 'maxQuotes'],
};
</script>

<style></style>
