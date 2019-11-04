<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <app-quote quote="is value from app.vue"></app-quote>
        <h2>The quote</h2>
        <p>A wonderfull Quote</p>
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "@/components/Quote.vue";

export default {
  components: {
    appQuote: Quote
  }
};
</script>

<style>
</style>
