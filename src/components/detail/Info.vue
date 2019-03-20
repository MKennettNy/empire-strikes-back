<template>
  <div class="container">
    <div>
      <h2></h2>
      <option value="">Please select news source...</option>
        <option
          v-for="searchQuery in SearchQuerys"
          v-bind:key="searchQuery.id"
          v-bind:value="searchQuery.id"
          >{{ searchQuery.name }}</option>
    </div>
  </div>
</template>

<script>
export default {
  name: "SourceSelection",
  data: function() {
    return {
      searchQuery: []
    };
  },
  methods: {
    SearchQuery: function(source) {
      if (source) {
        this.$http
          .get(
            "https://newsapi.org/v2/top-headlines?sources=" +
              source
          )
          .then(function(data) {
            this.articles = data.body.articles;
          });
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
