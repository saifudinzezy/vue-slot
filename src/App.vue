<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <app-quote>
          <!-- //kirim ke anak untuk di render. -->
          <h2 slot="title">{{quoteTitle}}</h2>
          <p slot="content">A wonderfull Quote</p>
        </app-quote>
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";

export default {
  data() {
    return {
      quoteTitle: "ini dari app.vue"
    };
  },
  components: {
    appQuote: Quote
  }
};
</script>

<style>
</style>
