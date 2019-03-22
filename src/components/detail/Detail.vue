<template>
  <div>
    <MyHeader />
    <h1>Detail</h1>
    <p>Search query is: {{searchQuery}}</p>
    
    <Content v-bind:contentdata="contentdata"/>
    <Info v-bind:contentdata="contentdata"/>
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content"
import Info from "./Info"

export default {
  name: "Detail",
  components: {
    MyHeader,
    Content,
    Info
  },
  data: function() {
    return {
      searchQuery: "",
      contentdata: { msg: "" }
    };
  },
    created: function() {
      console.log(this.$route.params);
    if (this.$route.params.searchQuery) {
        this.searchQuery = this.$route.params.searchQuery;
        this.$http
        .get("https://swapi.co/api/" + this.searchQuery)
        .then(function(contentdata) {
          this.contentdata = contentdata;          
        });
    }
  }
};
</script>

<style scoped></style>
