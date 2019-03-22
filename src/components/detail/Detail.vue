<template>
  <div>
    <MyHeader />
    <Content v-bind:contentdata="contentdata" />
    <info v-bind:contentdata="contentdata" />
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content"
// import Info from "./Info"
export default {
  name: "Detail",
  components: {
    MyHeader,
    Content
    // Info 


  },
  data: function() {
    return {
      contentdata: {},
      searchQuery: ""
    };
  },
  created: function() {
    if (this.$route.params.searchQuery) {
      console.log(this.$route.params);
      this.searchQuery = this.$route.params.searchQuery;
        this.$http
        .get("https://swapi.co/api/" + this.searchQuery)
        .then(function(contentdata) {
          this.contentdata = contentdata.body;
          console.log(this.contentdata)
        });
    }
  }
};
</script>

<style scoped></style>
