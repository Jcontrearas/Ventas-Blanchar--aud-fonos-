<template>
    <div>
        <v-badge color="error" :content="productos.length">
            <v-btn icon @click="detalle()">
                <v-icon class="carrito" >mdi-cart</v-icon>
              </v-btn>
          </v-badge>
       <factura 
        :show="show"
        @cerrar="cerrar"
        :compras="productos"
       ></factura>
    </div>
</template>
<script>

export default {
    props: {
    productos: {
        type: Array,
        default: []
        
    },
   
   },
    data() {
        return {
            show : false          
          }
    },
    methods : {
        detalle(){
            this.show = true
        },

        cerrar(){
            this.show = false
        }
    }
    
}
</script>
<style>
.carrito {
    color: #fff
}</style>