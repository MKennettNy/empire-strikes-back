<template>
  <div>
    <MyHeader />
      <Content />
      <Info/>
    <MyFooter />
   
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content";
import Info from "./Info";
import MyFooter from "../MyFooter";

export default {
  name: "Detail",
  data: function() {
    return {
      searchQuery: '',
    };
  },
  components: {
    MyHeader,
    Content,
    Info,
    MyFooter

  },
    created: function() {
    if (this.$route.params.searchQuery) {
       this.searchQuery = this.params.searchQuery;

    }
  }

};
</script>

<style scoped>

</style>
