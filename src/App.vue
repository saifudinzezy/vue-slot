<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent = 'appNew'">New</button>
        <hr />
        <p>{{selectedComponent}}</p>
        <!-- supaya slot tetap hidup walaupun direfresh -->
        <keep-alive>
          <component :is="selectedComponent">
            <p>Default Component</p>
          </component>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "@/components/Quote.vue";
import New from "@/components/New.vue";
import Author from "@/components/Author.vue";

export default {
  data() {
    return {
      quoteTitle: "ini dari app.vue",
      selectedComponent: "appQuote"
    };
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
};
</script>

<style>
</style>
