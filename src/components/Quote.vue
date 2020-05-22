<template>
  <div class="col-lg-3 col-md-6 col-sm-12">
    <div class="card mb-4">
      <div class="card-body">
        <h5 class="card-text">
          <slot></slot>
        </h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.card-text {
  font-family: 'Satisfy', cursive;
  font-size: 24px;
  color: #222f3e;
}
.card {
  background-color: #badc58;
}
.card:hover {
  background-color: #ffbe76;
}
</style>
