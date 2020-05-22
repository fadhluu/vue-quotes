<template>
  <div class="col-lg-4 col-md-6 col-sm-12">
    <div class="card mb-4">
      <div class="card-body">
        <blockquote class="blockquote mb-0">
          <slot name="quote"></slot>
          <footer class="blockquote-footer">
            <slot name="quoteBy"></slot>
          </footer>
        </blockquote>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.blockquote {
  font-family: 'Satisfy', cursive;
  font-size: 24px;
  color: #222f3e;
}
.blockquote-footer {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px;
  color: #2d3436;
}
.card {
  background-color: #55efc4;
  transition: 0.3s;
  cursor: pointer;
}
.card:hover {
  background-color: #ff7675;
}
</style>
