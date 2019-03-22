<template>
  <div>
    <div>Content</div>
    <p>Content data msg:{{contentdata.msg}}</p>
  </div>
</template>

<script>
export default {
  name: "Content",
  props: ["contentdata"]
};
</script>

<style scoped></style>