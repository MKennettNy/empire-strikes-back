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
    sourceChanged: function(evt) {
      this.$emit("$sourceChanged", evt.target.value);
    }
  },
  created: function() {
    this.$http
      .get(
        "https://swapi.co/api/?search=" + searchQuery
      )
      .then(function(data) {
        this.searchQuery = data.body.searchQuery;
      });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
