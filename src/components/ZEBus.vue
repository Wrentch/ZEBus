<template>
    
    <div class="container-fluid">
        <div class="row">
            <div class="col-12">
                <h1 class="text-center text-info">Lista linija</h1>
            </div>
            <!-- /.col-12 -->






            <div class="row">
                <div class="col-4 lista-linija">
                    <div class="card" style="width: 18rem">
                        <ul
                            class="list-group list-group-flush"
                            id="listaLinija"
                        >
                            <li
                                v-for="linija in linije" :key="linija.ime"
                                class="list-group-item"
                            >
                                {{ linija.ime }}
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- /.col6 -->
                <div class="col-8">
                    <karta/>
                </div>
                <!-- /.col6 -->
            </div>








        </div>
        <!-- /.row -->
        <div class="row"></div>
    </div>
    <!-- /.container -->
</template>

<script>
import karta from './karta.vue'




export default {
  components: { karta },
  name: 'ZEBus',
  props: {
    msg: String
  },
  data: () =>{
      return{
          linije: [
              {ime : "prva linija"},
              {ime : "druga linija"},
              {ime : "treca linija"}
          ]
      }
  }
}





</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.lista-linija {
    overflow-y: scroll;
    height: 95vh;

    li {
        &:hover {
            background-color: darkgrey;
        }
    }
}
</style>
