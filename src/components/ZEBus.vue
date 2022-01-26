<template>
  
  <div class="container">
    <div class="row">

      <div class="col-12">
        <h1>Lista linija</h1>
      </div>
      <!-- /.col-12 -->

    </div>
    <!-- /.row -->
  </div>
  <!-- /.container -->

</template>

<script>
export default {
  name: 'ZEBus',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
