<template>
  <div>
    <MyHeader />
       <Planet v-if="type === 'planet'"  />
      <Character v-if="type === 'character'"  />
       <Starships v-if="type === 'Starships'"  />
  
   
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content";
import Planet from "./Info";

export default {
  name: "Detail",
  data: function() {
    return {
      type: '',
    };
  },
  components: {
    MyHeader,
    Content,
    Info,
    Starships

  },
    created: function() {
    if (this.$route.params.type) {
       this.type = this.$route.params.type;
    }
  }

};
</script>

<style scoped></style>
