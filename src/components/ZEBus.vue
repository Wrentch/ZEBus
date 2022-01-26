<template>
  
  <div class="container-fluid">
    <div class="row">

      <div class="col-12">
        <h1 class="text-center text-info">Lista linija</h1>
      </div>
      <!-- /.col-12 -->

      <div class="row">

        <div class="col-4 lista-linija">

          <div class="card" style="width: 18rem;">
            <ul class="list-group list-group-flush" id="listaLinija">
              <li v-for="linija in linije" class="list-group-item" >{{linija.ime}}</li>

            </ul>
          </div>
          
        </div>
        <!-- /.col6 -->
        <div class="col-8">

          <h2 class="text-center">desno</h2>

        </div>
        <!-- /.col6 -->

      </div>



    </div>
    <!-- /.row -->
    <div class="row">

    </div>

    




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

  data: {
  linije:[
    { ime: "prva linija"},
    { ime: "druga linija"}
  ]
}






</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped >

  .lista-linija {
    overflow-y: scroll;
    height: 95vh;

    li {
      &:hover {
        background-color:darkgrey;
      }
    }

  }

</style>
