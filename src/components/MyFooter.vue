<template>
<div class="footer">
  <i class="fas fa-jedi"></i>
  <p>
    Copyright Disclaimer under section 107 of the Copyright Act 1976, allowance is made for “fair use” for purposes such as criticism, comment, news reporting, teaching, scholarship, education and research. Fair use is a use permitted by copyright statute
    that might otherwise be infringing.
  </p>
  </div>
</template>

<script>
  export default {
    name: "MyFooter"
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  p{
    width: 60%;
    margin: 0 auto;
    padding: 20px;
  }
  .footer{
    background-color: #222222;
    color: white;
  }
  i{
    font-size: 20px;
    padding-top: 20px;
  }
</style>
